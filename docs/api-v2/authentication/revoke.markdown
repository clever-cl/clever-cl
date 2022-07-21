---
layout: default
title: Revoke Token
grand_parent: Api V2
parent: Authentication
nav_order: 1
---

# Revoke Token

Este método permite revocar el `access_token` asociada al cliente.

## Endpoint

```bash
POST /api/v2/oauth/revoke
```

### Headers

| headers       | Value             |
|:--------------|:------------------|
| Content-Type  | application/json  |
| Accept        | application/json  |

### Body params

| Params       | value             |
|:--------------|:------------------|
| client_id     | `client_secret` de tu app Client App registrada en [Clever By BICE](https://clever.cl) |
| client_secret | `client_secret` de tu app Client App registrada en [Clever By BICE](https://clever.cl)   |

### Body Example

```json
{
  "client_id": "[CLIENT_ID]",
  "client_secret": "[CLIENT_SECRET]"
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
         <pre>
            {}
         </pre>
      </td>
   </tr>
   <tr>
      <td> 403 </td>
      <td>
         <pre>
{
  "error": "unauthorized_client",
  "error_description": "You are not authorized to revoke this token"
}
        </pre>
      </td>
   </tr>
   <tr>
      <td> 500 </td>
      <td>
         Internal Server Error
      </td>
   </tr>
</table>

## Request example

```bash
$ curl -X POST https://app.clever.cl/api/v2/oauth/revoke \
   -H 'Content-Type: application/json' \
   -d '{"client_id": [CLIENT_ID], "client_secret": [CLIENT_SECRET]}'
```
