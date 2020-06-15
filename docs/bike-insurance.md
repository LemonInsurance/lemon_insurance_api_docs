---
id: bike-insurance
title: Bike Insurance
sidebar_label: Bike Insurance
---



## Introduction

As part of Bike Insurance, we are exposing two APIs.

1. Get Quote API
2. Buy Policy API

## Get Quote API

This API provides you the quote for the Bike insurance



<table>
<tr>
<td> STAGE URL </td>
<td> https://stageapi.lemoninsurance.in/api/v1/bike-insurance/get-quote/ </td>
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
    <tr><th>Param Name</th><th>Param Type</th>
    </tr>
    <tr><td>provider</td> <td>String</td>
    </tr>
    <tr> <td>is_new</td> <td>String</td></tr>
    <tr> <td>variant</td> <td>String</td></tr>
    <tr> <td>registration_date</td> <td>String</td></tr>
    <tr> <td>registration_number</td> <td>String</td></tr>
    <tr> <td>is_roadside_assistance</td> <td>String</td></tr>
    <tr> <td>pa_with_valid_owner_dl</td> <td>String</td></tr>
    <tr> <td>is_fibre_glass_fuel_tank</td> <td>String</td></tr>
    <tr> <td>previous_ncb</td> <td>String</td></tr>
    <tr> <td>previous_policy_claimed</td> <td>String</td></tr>
    <tr> <td>policy_term</td> <td>String</td></tr>
    <tr><td>has_previous_policy</td><td>String</td></tr>    
<tr> <td>idv_one</td> <td>String</td></tr>
    <tr> <td>is_comprehensive</td> <td>String</td></tr>
    <tr> <td>expiry_date</td> <td>String</td></tr>
    <tr><td>previous_policy_type</td><td>String</td></tr>
    <tr><td>tppd_restricted</td><td>String</td></tr>
        
</table>

Response Params

<table>
    <tr><th>Param Name</th><th>Param Type</th>
    </tr>
    <tr><td>amount</td> <td>String</td>
    </tr>
    <tr> <td>idv</td> <td>String</td>
    </tr>
    <tr> <td>status_code</td> <td>String</td>
    </tr>
    <tr> <td>transaction_id</td> <td>String</td>
    </tr>
    
    
    
    
</table>

## Sample Request

```
{
    "provider": "dhfl",
    "is_new": "true",
    "variant": "5e9ac61b7c36e15fe2664d59",
    "registration_date": "07-10-2019",
    "registration_number": "ap28by1765",
    "is_roadside_assistance": "true",
    "pa_with_valid_owner_dl": "false",
    "is_fibre_glass_fuel_tank": "false",
    "previous_ncb": "20",
    "previous_policy_claimed": "false",
    "policy_term": "1",
    "has_previous_policy": "true",
    
    "idv_one": "45266",
    "is_comprehensive": "true",
    "expiry_date": "30-05-2020",
    "previous_policy_type": "comprehensive",
    "tppd_restricted": "false"
    
}
```

## Sample Response

```
{
  "amount": 1264.0,
  "idv": "53249",
  "status_code": 1,
  "transaction_id": "d23f898e3a7e428e92121cf8e5011eda"
}
```

    



## Buy Policy API

For buying policy, this api can be used. When you call this api, we deduct the amount from the balance that you maintain with us. For test, we will add the balance to your account. When test balance is less, you can ask us so we can add. 


<table>
<tr>
<td> STAGE URL </td>
<td> https://stage.linq.store/api/v1/bike-insurance/buy-policy/ </td>
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
    <tr><td>provider</td> <td>String</td>
    </tr>
    <tr> <td>engine_no</td> <td>String</td></tr>
    <tr> <td>chassis_no</td> <td>String</td></tr>
    <tr> <td>previous_policy_insurer_name</td> <td>String</td></tr>
    <tr> <td>previous_policy_number</td> <td>String</td></tr>
    <tr><td>puc_date</td><td>String</td></tr>
    <tr><td>puc_number</td><td>String</td></tr>
    <tr><td>puc_valid</td><td>String</td></tr>
    <tr> <td>transaction_id</td> <td>String</td></tr>
    <tr> <td>first_name</td> <td>String</td></tr>
    <tr> <td>middle_name</td> <td>String</td></tr>
    <tr> <td>last_name</td> <td>String</td></tr>
    <tr><td>is_driving_license_valid</td><td>String</td></tr>
    <tr> <td>address_line_1</td> <td>String</td></tr>
    <tr> <td>address_line_2</td> <td>String</td></tr>
    <tr><td>title</td><td>String</td></tr>
    <tr> <td>pincode</td> <td>String</td></tr>
    <tr> <td>mobile_no</td> <td>String</td></tr>
    <tr> <td>email</td> <td>String</td></tr>
    <tr> <td>registration_date</td> <td>String</td></tr>
    <tr> <td>pa_with_valid_owner_dl_nominee_name</td> <td>String</td></tr>
    <tr> <td>pa_with_valid_owner_dl_nominee_relation</td> <td>String</td></tr>
    <tr> <td>pa_with_valid_owner_dl_nominee_age</td> <td>String</td></tr>
    <tr> <td>pa_with_valid_owner_dl_appointee_name</td> <td>String</td></tr>
    <tr> <td>pa_with_valid_owner_dl_appointee_relation_to_nominee</td> <td>String</td></tr>
    
    
</table>

Response Params

<table>
    <tr><th>Param</th><th>Type</th>
    </tr>
    <tr> <td>pdf_url</td> <td>String</td>
    </tr>
    <tr><td>policy_number</td> <td>String</td>
    </tr>
    <tr><td>transaction_number</td> <td>String</td>
    </tr>
    <tr><td>status</td> <td>String</td>
    </tr>
    
</table>


## Sample Request

```
{  
	"provider": "dhfl",
    "registration_number": "ap28by5555",
    "engine_no": "kjkjkjkjk",
    "chassis_no": "hkjkhjhkkj",
    "previous_policy_insurer_name": "",
    "previous_policy_number": "sdfsdfds",
    "puc_date": "",
    "puc_number": "",
    "puc_valid": "true",
    "transaction_id": "d049fa1b45b048baaed347330ea7f232",
    "first_name": "sdf",
    "middle_name": "jkkj",
    "is_driving_license_valid": "true",
    "last_name": "sdf",
    "address_line_1": "sdf",
    "address_line_2": "sdf",
    "title": "mr",
    "pincode": "500072",
    "mobile_no": "9985402031",
    "email": "bhaskar@lemoninsurance.in",
    
    
    "pa_with_valid_owner_dl_nominee_name": "balaji p",
    "pa_with_valid_owner_dl_nominee_relation": "son",
    "pa_with_valid_owner_dl_nominee_age":"25",
    "pa_with_valid_owner_dl_appointee_name": "bhaskar p",
    "pa_with_valid_owner_dl_appointee_relation_to_nominee": "father"
    
}
```
## Sample Response

```
{
  "pdf_url": "url here",
  "policy_number": "20700069070/00/000000/0",
  "transaction_id": "d049fa1b45b048baaed347330ea7f232"
}
```


