# Overleaf OIDC Edition

This is a fork of Overleaf that we use on <https://tex.fachschaften.org>. The main change is that we added support for login via OpenID Connect.

Note that this currently still has some stuff that's hardcoded for our use and it enables shell-escape.

A mirror of this repo with CI that builds Docker images can be found at <https://gitlab.fachschaften.org/tudo-fsinfo/admin/overleaf>.

### Environment Variables

You need to set the following env vars:

- `OIDC_ISSUER`: `https://account.example.org/realms/fachschaften.org`
- `OIDC_AUTHORIZATION_URL`: `https://account.example.org/realms/fachschaften.org/protocol/openid-connect/auth`
- `OIDC_TOKEN_URL`: `https://account.example.org/realms/fachschaften.org/protocol/openid-connect/token`
- `OIDC_USERINFO_URL`: `https://account.example.org/realms/fachschaften.org/protocol/openid-connect/userinfo`
- `OIDC_CALLBACK_URL`: `https://tex.example.org/login/oidc/callback`
- `OIDC_CLIENT_ID`
- `OIDC_CLIENT_SECRET`

Optionally:

- `WELCOME_MESSAGE`: HTML Code to be included on the login page. For example greeting the user.
- `LOGIN_BUTTON_TEXT`: Label to use for the Login button (e.g., to brand it as "FSorg-Login")
