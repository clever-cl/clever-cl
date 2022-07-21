---
layout: default
title: Profile
grand_parent: Api V2
parent: Users
nav_order: 5
---

# Profile (wip)

Perfil de riesgo de un cliente [Clever By BICE](https://clever.cl)

## Endpoint

```bash
GET /api/v2/users/me/profile
```

## Headers

| headers       | Value             |
|:--------------|:------------------|
| Content-Type  | application/json  |
| Accept        | application/json  |
| Authorization | `Bearer [access_token]`  |

## Body params

| Params        | Value             |
|:--------------|:------------------|
|               |                   |

### Body Example

```json
empty
```

## Response Entities

### User

| Attr              | Value             |
|:------------------|:------------------|
|  identity_number  |                   |
|  name             |                   |
|  last_name        |                   |
|  full_address     |                   |
|  phone            |                   |
|  email            |                   |
|  activated        |                   |
|  risk_profile     | Object `RiskProfile` |

### RiskProfile

| Attr              | Value             |
|:------------------|:------------------|
|  excerpt          |                   |
|  name             | `aggresive`, `balanced`, `conservative`|

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
$ curl https://app.clever.cl/api/v2/users/me/profile \
   -H 'Content-Type: application/json' \
   -H 'Accept: application/json' \
   -H 'Authorization: Bearer [access_token]' \
   -d '{}' 
```
