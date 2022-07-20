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

### Endpoint
```
POST /api/v2/oauth/token
```
### Headers

| headers       | Value             |
|:--------------|:------------------|
| Content-Type  | application/json  |
| Accept        | application/json  |

### Body
```json
{
  "client_id": [CLIENT_ID],
  "client_secret": [CLIENT_SECRET],
  "username": "example@example.com",
  "password": "encrypted_password",
  "grant_type": "password"
}
```

### Responses

<table>
   <tr>
      <td> Status </td>
      <td> Response </td>
   </tr>
   <tr>
      <td> 200 </td>
<td>

```json
{
    "access_token": [ACCESS_TOKEN],
    "token_type": "Bearer",
    "expires_in": 7200,
    "refresh_token": [REFRESH_TOKEN],
    "created_at": 1658290998
}
```

</td>
   </tr>
    <tr>
      <td> 401 </td>
<td>

```json
{
    "error": "invalid_client",
    "error_description": "Client authentication failed due to unknown client, no client authentication included, or unsupported authentication method."
}
```

</td>
   </tr>
   <tr>
      <td> 403 </td>
      <td>Forbiden</td>
   </tr>
   <tr>
      <td> 500 </td>
      <td>
         Internal Server Error    
      </td>
   </tr>
</table>

## Examples

```bash
$ curl 
```