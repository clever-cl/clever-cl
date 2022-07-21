---
layout: default
title: Users
nav_order: 2
parent: Api V2
has_children: true
permalink: /docs/api-v2/users
---


# Resource Users
El resource `Users` permite crear y actualizar usuarios de Clever By BICE.

Un usuario en Clever By BICE es cualquier persona que registre su email en alguna de las aplicaciones (web o mobile). Cada email es único por lo que si registras un email ya podrás usarlo para crear una nueva cuenta.

## Términos y Condiciones
Un usuario registrado en Clever By BICE con su email podría recibir diferentes tipos de emails informativos o promocionales. Es importante que revises atentamente los [Políticas de privacidad de Clever](https://clever.cl/politicas-de-privacidad) y los [Términos y condiciones de Clever](https://clever.cl/terminos-y-condiciones).

## Crear Cuenta

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
         <pre>
{
  "access_token": "[ACCESS_TOKEN]",
  "token_type": "Bearer",
  "expires_in": 7200,
  "refresh_token": "[REFRESH_TOKEN]",
  "created_at": 1658290998
}
         </pre>
      </td>
   </tr>
   <tr>
      <td> 400 </td>
      <td>
         <pre>
{
  "error": "invalid_grant",
  "error_description": "The provided authorization grant is invalid, expired, revoked, does not match the redirection URI used in the authorization request, or was issued to another client."
}
        </pre>
      </td>
   </tr>   
   <tr>
      <td> 401 </td>
      <td>
         <pre>
{
  "error": "invalid_client",
  "error_description": "Client authentication failed due to unknown client, no client authentication included, or unsupported authentication method."
}
        </pre>
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