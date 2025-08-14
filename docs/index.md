---
hide:
  - toc
---

# DMS Aljabr lead-api-docs

## Overview

This doc will be used for API

---

## API endpoint

```
https://dms-api-test.jtc.aljabr.com.sa/swagger/index.html
```

---
This symbol <span class="flag-required">*</span>  means the field is mandatory 

### 📌 API

### Field Name <span class="flag-required">*</span>

What do we type here?

#### Request Body <span class="flag-required">*</span>

```json
{
  "leads": [
    {
      "leadType": { "value": 0, "label": "string" },
      "companyIndustryType": { "value": 0, "label": "string" },
      "contactName": "string",
      "title": { "value": 0, "label": "string" },
      "gender": { "value": 0, "label": "string" },
      "nationality": { "value": 0, "label": "string" },
      "firstName": "string",
      "middleName": "string",
      "lastName": "string",
      "dateOfBirth": "2025-08-14T06:49:50.800Z",
      "occupation": "string",
      "customerCountry": { "value": 0, "label": "string" },
      "customerRegion": { "value": 0, "label": "string" },
      "customerCity": { "value": 0, "label": "string" },
      "address1": "string",
      "address2": "string",
      "phoneCode": { "value": 0, "label": "string" },
      "phoneNumber": "5XXXXXXXX",
      "email": "info@aljabr.com.sa",
      "monthlyIncome": { "value": 0, "label": "string" },
      "preferredLanguage": { "value": 0, "label": "string" },
      "preferredContactType": { "value": 0, "label": "string" },
      "company": { "value": 0, "label": "string" },
      "ou": { "value": 0, "label": "string" },
      "businessArea": { "value": 0, "label": "string" },
      "branch": { "value": 0, "label": "string" },
      "leadDate": "2025-08-14T06:49:50.801Z",
      "leadInterest": { "value": 0, "label": "string" },
      "source": { "value": 0, "label": "string" },
      "subSource": { "value": 0, "label": "string" },
      "leadName": "string",
      "leadReference": "string",
      "leadNote": "string",
      "vehicleType": { "value": 0, "label": "string" },
      "vehicles": [
        {
          "modelFamily": { "value": 0, "label": "string" },
          "modelYear": { "value": 0, "label": "string" },
          "modelMemo": "string",
          "modelPreferences": "string",
          "totalQty": 1000
        }
      ],
      "purchasePlan": { "value": 0, "label": "string" },
      "paymentMode": { "value": 0, "label": "string" },
      "currency": { "value": 0, "label": "string" },
      "priority": { "value": 0, "label": "string" },
      "testDriveRequired": { "value": 0, "label": "string" },
      "acceptNewsLetter": { "value": 0, "label": "string" },
      "acceptMarketing": { "value": 0, "label": "string" },
      "acceptPrivatePolicy": { "value": 0, "label": "string" }
    }
  ]
}
```

#### Response  ----EDIT this

```json
{
  "id": "survey_12345",
  "status": "created"
}
```

---

### 📌 Get Survey Results

**GET** `/results/{survey_id}`

Retrieves responses for a specific survey.

#### Response

```json
{
  "survey_id": "survey_12345",
  "responses": [
    {
      "user_id": "user_001",
      "answers": [5]
    }
  ]
}
```

---

#### leadType <span class="flag-required">*</span>

<a href="lookups/#customer_type"><span class="http-get">GET</span></a> `/v1/list/{CUSTOMER_TYPE}`

!!! note "Mandatory Fields for Company Lead Type"
    When `leadType` value is Individual, the following fields are mandatory

    1. `firstName`

    When `leadType` value is Company, the following fields will be **mandatory**:
    
    1. `companyIndustryType`
    2. `contactName`
    3. `leadTypeName`


#### companyIndustryType 

<a href="lookups/#customer_industry_type"><span class="http-get">GET</span></a> `/v1/list/{CUSTOMER_INDUSTRY_TYPE}`

contactName:`string`

leadTypeName:`string`

#### title

<a href="lookups/#title"><span class="http-get">GET</span></a> `/v1/list/{TITLE}`

#### nationality

<a href="lookups/#nationality"><span class="http-get">GET</span></a> `/v1/list/{NATIONALITY}`

#### gender

<a href="lookups/#gender"><span class="http-get">GET</span></a> `/v1/list/{GENDER}`

firstName:`string`

lastName:`string`

middleName:`string`

dateOfBirth:`yyyy-mm-dd` 

occupation:`string`

#### customerCountry <span class="flag-required">*</span>

<a href="lookups/#country"><span class="http-get">GET</span></a> `/v1/list/{COUNTRY}`  

#### customerRegion <span class="flag-required">*</span>

<a href="lookups/#customer_region"><span class="http-get">GET</span></a> `/v1/list/{REGION}?parentId={customerCountry.value}`

#### customerCity <span class="flag-required">*</span>

<a href="lookups/#customer_city"><span class="http-get">GET</span></a> `/v1/list/{CITY}?parentId={customerRegion.value}`

address1:`string`

address2:`string`

#### phoneCode <span class="flag-required">*</span>

<a href="lookups/#phone_code"><span class="http-get">GET</span></a> `/v1/list/{PHONE_CODE}`

phoneNumber:`string`

!!! note "phonerNumber length should be 9 characters"

email:`string`

#### monthlyIncome

<a href="lookups/#lead_monthly_income"><span class="http-get">GET</span></a> `/v1/list/{LEAD_MONTHLY_INCOME}`

preferredLanguage <span class="flag-required">*</span>

<a href="lookups/#language"><span class="http-get">GET</span></a> `/v1/list/{LANGUAGE}`

preferredContactType

<a href="lookups/#contact_type"><span class="http-get">GET</span></a> `/v1/list/{CONTACT_TYPE}`

company:`Aljabr Trading Company`

ou <span class="flag-required">*</span>

<a href="lookups/#ou_type"><span class="http-get">GET</span></a> `/v1/list/{OU_TYPE}`

businessArea <span class="flag-required">*</span>

<a href="lookups/#business_area"><span class="http-get">GET</span></a> `/v1/list/{BUSINESS_AREA}?parentId={ou_type.value}`

branch <span class="flag-required">*</span>

<a href="lookups/#branch_type"><span class="http-get">GET</span></a> `/v1/list/{BRANCH_TYPE}?parentId={branch_type.value}`

leadDate:`string` <span class="flag-required">*</span>

leadInterest <span class="flag-required">*</span>

<a href="lookups/#lead_interest"><span class="http-get">GET</span></a> `/v1/list/{LEAD_INTEREST}`

source <span class="flag-required">*</span>

<a href="lookups/#lead_source"><span class="http-get">GET</span></a> `/v1/list/{LEAD_SOURCE}`

subSource <span class="flag-required">*</span>

<a href="lookups/#lead_sub_source"><span class="http-get">GET</span></a> `/v1/list/{LEAD_SUB_SOURCE}?parentId={lead_source.value}`

leadName:`string` <span class="flag-required">*</span>

leadReference:`string`

leadNote:`string`

#### vehicleType

<a href="lookups/#vehicle_type"><span class="http-get">GET</span></a> `/v1/list/{VEHICLE_TYPE}`

vehicles.modelFamily

<a href="lookups/#model"><span class="http-get">GET</span></a> `/v1/list/{MODEL}?parentId={ou_type.value}`

vehicles.modelYear

<a href="lookups/#model_year"><span class="http-get">GET</span></a> `/v1/list/{MODEL_YEAR}`

<!-- should I keep as not in json -->
vehicles.modelMemo:`string`

<!-- should I keep as not in json -->
vehicles.modelPreferences:`string`

<!-- should I keep as not in json -->
vehicles.totalQty:`string`


purchasePlan

<a href="lookups/#purchase_plan"><span class="http-get">GET</span></a> `/v1/list/{PURCHASE_PLAN}`

paymentMode

<a href="lookups/#payment_mode"><span class="http-get">GET</span></a> `/v1/list/{PAYMENT_MODE}`

currency

<a href="lookups/#currency"><span class="http-get">GET</span></a> `/v1/list/{CURRENCY}`

priority <span class="flag-required">*</span>

<a href="lookups/#lead_priority"><span class="http-get">GET</span></a> `/v1/list/{LEAD_PRIORITY}`

testDriveRequired

<a href="lookups/#yes_or_no"><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`


acceptNewsLetter

<a href="lookups/#yes_or_no"><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`

acceptMarketing

<a href="lookups/#yes_or_no"><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`

acceptPrivatePolicy

<a href="lookups/#yes_or_no"><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`
