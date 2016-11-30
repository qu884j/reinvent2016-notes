# Serverless authentication

- Cognito
- Web Identity Federation

# Password

# SRP Secure Remote Password

- precomputed
- passwords never go over the wire

# Cognito User Pools

- Register » Cognito
- Respond with Verification to User
- Confirm Registration
- Success Register
- Authenticate (via SRP)
- JWT Tokens

"Define Authentication Challenge" '

# JWT Tokens

JSON Web Tokens

Compact way to send assertion to another systems

- base64
- 3 payloads, separated by `.`

  - header
  - payload
  - signature

# Cognito with AWS Resources

Amazon Cognito Federated Identities

- exchange auth tokens for temp access to AWS

Temporary Access credentials

- Access Key
- Secret Key
- Session Token

Standard SDKs can now be used

- Identity Tokens
- Access Token

  - make calls to cognito user pools to interact with cognito user pool

- Refresh Token

  - if access token has expired, you can send that bck to get a new Token

[https://jwt.io]() Has debugger tool

# Api Gateway Authorizers

## User Pools Authorizers

## AWS IAM Authorization

- API Gateway `execute-api:invoke` is the permission needed

## Custom Authorizers

- Any provider that provides a bearer token, or whatever

- tokens go to API Gateway

  - api gateway calls out to custom authorizer lambda function
  - generate and returns IAM policy
  - API Gateway validates IAM permissions to IAM
  - ...
  - invokes lambda

API Keys are not meant for API Gateway for authentication
