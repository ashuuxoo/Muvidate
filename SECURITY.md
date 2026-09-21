# Security Policy

## Supported versions

The `main` branch is the actively maintained version.

## Reporting a vulnerability

Please do not open a public issue for a suspected security vulnerability.

Contact the repository maintainer privately through GitHub and include:

- A clear description of the issue
- Affected files or components
- Reproduction steps when safe
- Potential impact
- Suggested mitigation, if known

Do not include passwords, access tokens, private user data or production secrets.

## Security notes

MuviDate uses Firebase from the client. Production security therefore depends on correct:

- Firebase Authentication configuration
- Firestore Security Rules
- Realtime Database Security Rules
- Hosting environment variables
- Validation of user-controlled room and media data

Client-side Firebase configuration must not be treated as a permission boundary.
