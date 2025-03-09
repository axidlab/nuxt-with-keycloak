Playground - Nuxt with Keycloak
===============================

This is a playground for Nuxt with Keycloak. It is a simple Nuxt application that uses Keycloak for authentication.

## Alternatives

* https://nuxt.com/modules/auth-utils
* https://nuxt.com/modules/nuxt-oidc-auth
* https://nuxt.com/modules/sidebase-auth
* https://www.npmjs.com/package/@jabardigitalservice/nuxt-module-keycloak

## Auth Utils

* Documentation: https://nuxt.com/modules/auth-utils
* Sample project: https://github.com/atinux/atidone/

### Install

Node 20.6.0+ is required.

    mvn ls-remote --lts
    nvm install 22.14.0

Add module:

    npx nuxi@latest module add auth-utils

### Configuration

We use oauth provider with name `keycloak`.

Add to `.env`:

    KEYCLOAK_URL=https://keycloak.example.com/authNUXT_SESSION_PASSWORD=password-with-at-least-32-characters
    NUXT_OAUTH_KEYCLOAK_CLIENT_ID=
    NUXT_OAUTH_KEYCLOAK_CLIENT_SECRET=
    NUXT_OAUTH_KEYCLOAK_SERVER_URL=
    NUXT_OAUTH_KEYCLOAK_REALM=

Alternatively, config can be added to `nuxt.config.js`:

    oauth: {
        keycloak: {
            clientId: '',
            clientSecret: '',
            serverUrl: '',
            realm: ''
        }
    }

## Keycloak Settings

In the `Clients -> Settings -> Access Settings` of the used realm, set:

* Root URL: `http://localhost:3000`
* Home URL: `/`

## Resources

* https://medium.com/js-dojo/how-to-integrate-keycloak-in-vuejs-nuxtjs-557cc4bcef41
