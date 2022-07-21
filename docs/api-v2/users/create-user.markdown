---
layout: default
title: Create User
grand_parent: Api V2
parent: Users
nav_order: 2
---

# Create User (wip)

Crea un usuario en Clever By BICE

## Endpoint

```bash
POST /api/v2/users
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
    "email": "email@example.com",
    "utm": "utm_source=null&utm_medium=null&utm_campaign=null&utm_term=null&utm_content=null"
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
$ curl -X POST https://app.clever.cl/api/v2/users \
   -H 'Content-Type: application/json' \
   -H 'Accept: application/json' \
   -d '{ "user": { "email": "email@example.com", "utm": "utm_source=null&utm_medium=null&utm_campaign=null&utm_term=null&utm_content=null" } }' 
```
