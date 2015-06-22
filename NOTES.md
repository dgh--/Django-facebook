# Updating Django-facebook to work with FB Graph API v2.x

## Various notes

    API_BASE_URL = 'https://graph.facebook.com/v2.3/'
    FACEBOOK_ME_URL = 'https://graph.facebok.com/v2.3/me?'
    ACCESS_TOKEN_URL = 'https://graph.facebook.com/v2.3/oauth/access_token?'

* FB graph API no longer returns username.
* When testing django-facebook, map yr IP address to a domain name, as Facebook checks the domain.
* Remove references to username.
* Django-facebook has South migrations in it; presumably 1.7s migrations can handle the migrations.

As far as I can recall, all I really had to do to monkey patch an older version of Django-facebook to get it to work with the v2.3 version of the API was to change the URLs, but Ive got a feeling that there must have been more to it than that.

