---
layout: default
title: Authentication
parent: Api V2
nav_order: 1
---

# Authentication
In order to create an access you must have an app priviously created on Clever and a valid Public cert.

To register your own app on Clever check documentation [Api V2](/docs/api-v2)

## Create Access Token

```
POST /api/v2/oauth/token
```

| headers       | Value             |
|:--------------|:------------------|
| Content-Type  | application/json  |
| Accept        | application/json  |


```json
{
  "client_id": [CLIENT_ID],
  "client_secret": [CLIENT_SECRET],
  "username": "example@example.com",
  "password": "encrypted_password",
  "grant_type": "password"
}

```

## Examples

```bash
$ curl 
```