---
layout: default
title: Api V2
nav_order: 3
has_children: true
permalink: /docs/api-v2
---

# Api V2

Clever Api V2 es la versión actual de la API pública de [Clever By BICE](https://clever.cl).

En esta versión se incluyen las principales APIs que te permitirán interactuar con los recursos principales de nuestra plataforma

- `Users`
- `Goals`
- `Mutual Funds`

## Health Check

## Endpoint

```bash
GET /api/v2/health/check
```

## Headers

| headers       | Value             |
|:--------------|:------------------|
| Content-Type  | application/json  |
| Accept        | application/json  |

## Body params

| Params        | Value             |
|:--------------|:------------------|
|               |                   |

### Body Example

```json
empty
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
{
    "alive": "yes"
}
         </pre>
      </td>
   </tr>
   <tr>
      <td> 404 </td>
      <td>
        Not Found
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
$ curl https://app.clever.cl/api/v2/health/check
```
