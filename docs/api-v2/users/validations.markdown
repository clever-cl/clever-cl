---
layout: default
title: Validations
grand_parent: Api V2
parent: Users
nav_order: 5
---

# Validations (legacy)

Permite validar la cédula de un cliente [Clever By BICE](https://clever.cl)

## Endpoint

```bash
GET /api/v2/users/validations
```

## Headers

| headers       | Value             |
|:--------------|:------------------|
| Content-Type  | application/json  |
| Accept        | application/json  |
| Authorization | `Bearer [access_token]`  |

## Body params

| Params        | Value               |
|:--------------|:--------------------|
| validation    | Object `Validation` |

### Validation

| Params           | Value                     |
|:-----------------|:--------------------------|
| identity_number  | `ecrypted_identity_number` |
| serial_number    | `ecrypted_serial_number`  |

### Body Example

```json
{
    "validation": {
        "identity_number": [ENCRYPTED_IDENTITY_NUMBER],
        "serial_number": [ENCRYPTED_SERIAL_NUMBER]
    }
}
```

## Response Entities

### Validation

| Attr          | Value               |
|:--------------|:--------------------|
|  code         |                     |
|  message      |                     |
|  payload      | Object `Validation` |

### Validation

| Attr              | Value               |
|:------------------|:--------------------|
|  name             |                     |
|  last_name        |                     |
|  nationality      |                     |
|  birthday         |                     |
|  genre            |                     |
|  marital_status   |                     |
|  wedding_date     |                     |


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
$ curl https://app.clever.cl/api/v2/users/validations \
   -H 'Content-Type: application/json' \
   -H 'Accept: application/json' \
   -H 'Authorization: Bearer [access_token]' \
   -d '{ "validation": { "identity_number": [ENCRYPTED_IDENTITY_NUMBER],
        "serial_number": [ENCRYPTED_SERIAL_NUMBER] } }' 
```

