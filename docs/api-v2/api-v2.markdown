---
layout: default
title: Api V2
nav_order: 3
has_children: true
permalink: /docs/api-v2
---

# Api V2

Clever Api V2 es la versión actual de la API pública de Clever By BICE.

En esta versión se incluyen las principales APIs que te permitirán interactuar con los recursos principales de nuestra plataforma

- `Users`
- `Goals`
- `Mutual Funds`

## OAuth 2.0
## How to register my Client App ?
Para registrar tu Client App en nuestro portal puedes escribirnos a devs@clever.cl

Indicando claramente los siguientes puntos, puedes usar el mismo template:

| Client App                  | Value                                       |
|:----------------------------|:--------------------------------------------|
| Name                        | My App                                      |
| Callback URL                | https://myapp.example.com/callabck          |
| Objetivo                    | Objetivo                                    |
| Términos y condiciones  URL | https://miapp.com/terms-and-conds           |
| Email Owner                 | owner@example.com                           |
| Email Soporte               | support@example.com                         |
| RR.SS URLs  (optional)      | `discord` `slack` `twitter` `ig` `facebook` |


## Health Check

### Endpoint
```
GET /api/v2/health/check
```
### Headers

| headers       | Value             |
|:--------------|:------------------|
| Content-Type  | application/json  |
| Accept        | application/json  |

### Response

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
