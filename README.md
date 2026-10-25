# wax-google-login

The Google sign-in return page of WAX. Google only sends a browser back to a public https address after sign-in, and
WAX runs on the local network, so this static page is the "Authorized redirect URI" of WAX's Google OAuth client:
it forwards the browser straight back to the WAX address the sign-in started from (`/google-callback`), on the local
network only. It stores and sends nothing. The code it passes on is useless without the WAX server's client secret
and PKCE verifier.
