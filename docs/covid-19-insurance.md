---
id: covid-19-insurance
title: Covid 19 Insurance
sidebar_label: Covid 19 Insurance
---



## Introduction

As part of Covid Insurance, we are exposing two APIs.

1. Get Quote API
2. Buy Policy API

## Get Quote API

This API provides you the quote for the covid insurance



<table>
<tr>
<td> STAGE URL </td>
<td> https://stageapi.lemoninsurance.in/api/v1/covid-insurance/get-quote/ </td>
</tr>

<tr>
    <td>Request Type</td>
    <td>POST</td>
</tr>


</table>

Headers

<table>
<tr>
<td> api-key </td>
<td> to be shared in email </td>
</tr>

<tr>
    <td>api-secret</td>
    <td>to be shared in email</td>
</tr>
<tr>
    <td>Content-type:</td>
    <td>application/json</td>
</tr>

</table>

Request Params

<table>
    <tr><th>Param</th><th>Type</th>
    </tr>
    <tr><td>sum_insured</td> <td>float</td>
    </tr>
    <tr> <td>primary_add_on</td> <td>String</td>
    </tr>
    
    
</table>

Response Params

<table>
    <tr><th>Param</th><th>Type</th>
    </tr>
    <tr><td>amount</td> <td>float</td>
    </tr>
    <tr> <td>gst</td> <td>float</td>
    </tr>
    <tr> <td>premium</td> <td>float</td>
    </tr>
    <tr> <td>ref_id</td> <td>String</td>
    </tr>
    
    
    
    
</table>

## Sample Request

```
{
“sum_insured”: “25000”,
“primary_add_on”: "false"
}
```

## Sample Response

```
{
  "amount": 300.9,
  "gst": 45.9,
  "premium": 255.0,
  "ref_id": “e0ea2fe63c044efea5b35d041cb01f20”,
}

```

    



## Buy Policy API

For buying policy, this api can be used. When you call this api, we deduct the amount from the balance that you maintain with us. For test, we will add the balance to your account. When test balance is less, you can ask us so we can add. 


<table>
<tr>
<td> STAGE URL </td>
<td> https://stage.linq.store/api/v1/covid-insurance/buy-policy/ </td>
</tr>

<tr>
    <td>Request Type</td>
    <td>POST</td>
</tr>
<tr>
    <td>Content-type:</td>
    <td>application/json</td>
</tr>

</table>


Request Params

<table>
    <tr><th>Param</th><th>Type</th>
    </tr>
    <tr><td>ref_id(this we have sent you earlier as part of get quote response)</td> <td>String</td>
    </tr>
    <tr> <td>sum_insured</td> <td>String</td>
    </tr>
    <tr> <td>primary_add_on</td> <td>String</td>
    </tr>
    <tr> <td>txn_source_id</td> <td>String</td>
    </tr>
    <tr> <td>name</td> <td>String</td>
    </tr>
    <tr> <td>email</td> <td>String</td>
    </tr>
    <tr> <td>mobile_number</td> <td>String</td>
    </tr>
    <tr> <td>dob</td> <td>String</td>
    </tr>
    
    
    
    
</table>

Response Params


<table>
    <tr><th>Param</th><th>Type</th>
    </tr>
    <tr> <td>ref_id</td> <td>String</td>
    </tr>
    <tr><td>amount</td> <td>float</td>
    </tr>
    <tr><td>message</td> <td>String</td>
    </tr>
    <tr><td>premium</td> <td>float</td>
    </tr>
    <tr><td>ref_id</td> <td>String</td>
    </tr>
    <tr><td>txn_source_id</td> <td>String</td>
    </tr>

</table>


## Sample Request

```
{
    “ref_id”: “ref_id that we sent you for get_quote”,
    "sum_insured": "25000",
    "primary_add_on": false,
    "txn_source_id": "abcdef",
    "name": "Bhaskar",
    "email": "bhaskar.r@tech.linq.store",
    "mobile_number": "9441105900",
    "dob": "01-01-1990"
}

```
## Sample Response

```
{
  "amount": 300.9,
  "gst": 45.9,
  "message": "success",
  "premium": 255.0,
  "ref_id": "404f129f5988467ca4a1f66b653fe5ee",
  "txn_source_id": "abcdef"
}

```

Error response:

When there is any error in server like “validation error”, then errors are returned in the below format

Status code - 400

First Error response format:

{
  "error": true,
  "message": "Duplicate transaction"
}

 
Second error response format:

{
  "error": true,
  "errors": [
    {
      "sum_insured": "Invalid sum insured"
    }
  ]
}

How to show errors in your system:

Check if the “error” key is present and if it’s true. If true, then check for the “errors” key. If present, loop over it as its always a list and display errors. 

If the “error” key is present and if its true but “errors” key is not present, then check for error message in “message” key. Error message in “message” key is always single message. Generally a generic message.
