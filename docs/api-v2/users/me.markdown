---
layout: default
title: Me
grand_parent: Api V2
parent: Users
nav_order: 1
---
# Me (wip)

Retorna el recurso `user`
## Endpoint

```bash
POST /api/v2/users/me
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

| Attr       | Value             |
|:--------------|:------------------|
|  token        |                   |
|  status       |                   |
|  name         |                   |
|  last_name    |                   |
|  fullname     |                   |
|  identity_number |                   |
|  full_address    |                   |
|  phone           |                   |
|  profession      |                   |
|  referrer_link   |                   |
|  ref_token       |                   |
|  confirmed       |                   |
|  email           |                   |
|  investor_profile  | Object `InvestorProfile` |
|  summary           | Object `Summary`         |
|  summary_in_clp    | Object `SummaryInClp`    |
|  goals             | Array `Goal`             |
|  pending_distributions  | Object `PendingDistribution` |
|  movement_in_process    | Object `MovementInProcess`   |

### InvestorProfile

| Attr       | Value             |
|:-----------|:------------------|
|  name      | `Agresivo`, `Balanceado`, `Conservador` |
|  slug      | `aggresive`, `balanced`, `conservative`|

### Summary

| Attr       | Value             |
|:--------------|:------------------|
|  nav          |                   |
|  balance      |                   |
|  profitability  |                   |
|  rentability    |                   |
|  rentability_in_porcentaje |        |
|  contributions  |                   |
|  withdrawals    |                   |


### SummaryInClp

| Attr          | Value             |
|:--------------|:------------------|
|  nav          |                   |
|  balance      |                   |
|  profitability  |                 |
|  rentability    |                 |
|  contributions  |                 |
|  withdrawals    |                 |


### Goal

| Attr             | Value             |
|:-----------------|:------------------|
|  id              |                   |
|  user_token      |                   |
|  name            |                   |
|  created_at      |                   |
|  updated_at      |                   |
|  category        |                   |
|  status          |                   |
|  year            |                   |
|  target_month    |                   |
|  target_year     |                   |
|  mutual_fund     | Object `MutualFund`   |
|  summary         | Object `Summary`      |
|  summary_in_clp  | Object `SummaryInClp` |


### PendingDistribution

| Attr             | Value             |
|:-----------------|:------------------|
|  quantity        |                   |
|  transaction_id  |                   |

### MovementInProcess

| Attr              | Value                    |
|:------------------|:-------------------------|
|  contribution     | Object `Contribution`    |
|  withdrawal       | Object `Withdrawal`      |
|  fund_change      | Object `FundChange`      |
|  payment_intent   | Object `PaymentIntent`   |

#### Contribution

| Attr                  | Value                    |
|:----------------------|:-------------------------|
|  amount_data          | Array `Amount`           |
|  total_amount         |                          |
|  total_amount_in_clp  |                          |
|  quantity             |                          |


#### Withdrawal

| Attr                  | Value                    |
|:----------------------|:-------------------------|
|  amount_data          | Array `Amount`           |
|  total_amount         |                          |
|  total_amount_in_clp  |                          |
|  quantity             |                          |

#### FundChange

| Attr                  | Value                    |
|:----------------------|:-------------------------|
|  amount_data          | Array `Amount`           |
|  total_amount         |                          |
|  total_amount_in_clp  |                          |
|  quantity             |                          |

#### PaymentIntent

| Attr                  | Value                    |
|:----------------------|:-------------------------|
|  amount_data          | Array `Amount`           |
|  total_amount         |                          |
|  total_amount_in_clp  |                          |
|  quantity             |                          |


#### Amount

| Attr              | Value                    |
|:------------------|:-------------------------|
|  amount           |                          |
|  created_at       |                          |
|  fund_change      |                          |
|  kind_of_movement |                          |
|  goal_name        |                          |
|  goal_category    |                          |
|  goal_id          |                          |
|  mutual_fund      |                          |
|  estimage_date    |                          |

# Responses

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
$ curl -X POST https://app.clever.cl/api/v2/users/me \
   -H 'Content-Type: application/json' \
   -H 'Accept: application/json' \
   -H 'Authorization: Bearer [ACCESS_TOKEN]' \
   -d '{}' 
```
