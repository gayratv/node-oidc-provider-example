# example setup of oidc-provider

By following this example you will set up an [oidc-provider](https://github.com/panva/node-oidc-provider)
instance on Heroku.

Prerequisites

- node ^12.19.0 || ^14.15.0
- heroku cli installed (`which heroku`)
- heroku cli authenticated (`heroku whoami`)
- wget
- git


Start [here](00-oidc-minimal).

NB
---
By no means is oidc-provider limited to only run on heroku or only using the showcased options. The user-interactions are also ONLY intended to show how these are to be provided and maintained. Features such as sign-up, password resets and security measures like csrf, rate limiting, captcha - that's all on you and isn't a part of the protocol implementation provided by oidc-provider.

Supported deployments include mounting the OP to an existing nodejs application, e.g. connect, express, fastify, hapi, koa, or nest. Running those using cluster mode spread across several hosts, behind haproxy, nginx,
ELB or exposing an https server directly.

It is possible to run a completely standalone app for interactions and it's also possible to run
oidc-provider on AWS Lambda.

Adapters that have been seen include MongoDB, PostgreSQL, redis, DynamoDB, REST Api

> **HINT**: For more details consider documentation, configuration and details found in the [oidc-provider repository](https://github.com/panva/node-oidc-provider).


**************************

heroku config
=== secret-brushlands-89186 Config Vars
HEROKU_APP_ID:             a26b045e-0aca-48a3-a08d-2739b149858f
HEROKU_APP_NAME:           secret-brushlands-89186
HEROKU_RELEASE_CREATED_AT: 2022-02-06T12:02:56Z
HEROKU_RELEASE_VERSION:    v10
HEROKU_SLUG_COMMIT:        abdf85cafb2cecbc89a0f8c0ba48848c91fc63f1
HEROKU_SLUG_DESCRIPTION:   Deploy abdf85ca
REDIS_TLS_URL:             rediss://:p9d5e844f2b1e7e9bb09c95398b8557d83dbd272dadb7df7477ff9bcc3307c53c@ec2-18-205-170-108.compute-1.amazonaws.com:24700
REDIS_URL:                 redis://:p9d5e844f2b1e7e9bb09c95398b8557d83dbd272dadb7df7477ff9bcc3307c53c@ec2-18-205-170-108.compute-1.amazonaws.com:24699

heroku config | grep SECURE_KEY

The keys are formatted like <CURRENT_KEY>,<OLD_KEY>.

SECURE_KEY:                A6FCD7E79D9D49E025E600019A878EFAFDBA2D5C087DA6396B1B541814AAFA8D,F2D95F8312D4F9AF66BFA61221208481A078C2C1C3E917E06ADA2880BD214F14


