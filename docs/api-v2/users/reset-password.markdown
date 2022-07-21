---
layout: default
title: Reset Password
grand_parent: Api V2
parent: Users
nav_order: 4
---

# Reset Password (wip)

Recuperar contraseña

## Endpoint

```bash
POST /api/v2/users/password
```

## Headers

| headers       | Value             |
|:--------------|:------------------|
| Content-Type  | application/json  |
| Accept        | application/json  |

## Body params

| Params       | value             |
|:--------------|:------------------|

### Body Example

```json
{
    "user": { 
        "email": "email@example.com" 
    }        
}
```

## Responses

<table>
   <tr>
      <td> Status </td>
      <td> Response </td>
   </tr>
   <tr>
      <td> 200 </td>
      <td>
         <pre>
Work in progress
        </pre>
      </td>
   </tr>
   <tr>
      <td> 400 </td>
      <td>
         <pre>
Work in progress
        </pre>
      </td>
   </tr>   
   <tr>
      <td> 401 </td>
      <td>
         <pre>
Work in progress
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

## Request example

```bash
$ curl -X POST https://app.clever.cl/api/v2/users/password \
   -H 'Content-Type: application/json' \
   -H 'Accept: application/json' \
   -d '{ "user": { "email": "email@example.com" } }' 
```
