---
hide:
  - toc
---

## API endpoint


```
PROD: https://dms-api.jtc.aljabr.com.sa/api
TEST: https://dms-api-test.jtc.aljabr.com.sa/api
``` 
<a><span class="http-get">POST</span></a> `/v1/leads/bulks`


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
      "company": "string",
      "businessArea": "string",
      "branch": "string",
      "brand": "string",
      "title": "string",
      "nationality": "string",
      "gender": "string",
      "source": "string",
      "subSource": "string",
      "phoneCode": "string",
      "phoneNumber": "string",
      "preferredLanguage": "string",
      "preferredContactType": "string",
      "purchasePlan": "string",
      "paymentMode": "string",
      "monthlyIncome": "string",
      "currency": "string",
      "testDriveRequired": true,
      "acceptNewsLetter": true,
      "acceptMarketing": true,
      "acceptPrivatePolicy": true,
      "priority": "string",
      "leadType": "string",
      "interest": "string",
      "vehicleType": "string",
      "firstName": "string",
      "middleName": "string",
      "lastName": "string",
      "dateOfBirth": "2025-08-17T06:49:41.761Z",
      "occupation": "string",
      "address1": "string",
      "address2": "string",
      "email": "string",
      "leadName": "string",
      "leadDate": "2025-08-17T06:49:41.761Z",
      "leadReference": "string",
      "leadNote": "string",
      "contactName": "string",
      "leadTypeName": "string",
      "companyIndustryType": "string",
      "customerCountry": "string",
      "customerRegion": "string",
      "customerCity": "string",
      "vehicles": [
        {
          "modelFamily": "string",
          "modelYear": 0,
          "modelMemo": "string",
          "modelPreferences": "string",
          "totalQty": 1000
        }
      ]
    }
  ],
  "isProcessed": 1
}
```

#### Response

```json
integer
```

---


#### leadType <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{CUSTOMER_TYPE}`

!!! note "Mandatory Fields for Company Lead Type"
    When `leadType` value is Individual, the following fields are mandatory

    1. `firstName`

    When `leadType` value is Company, the following fields will be **mandatory**:
    
    1. `companyIndustryType`
    2. `contactName`
    3. `leadTypeName`


#### companyIndustryType 

<a><span class="http-get">GET</span></a> `/v1/list/{CUSTOMER_INDUSTRY_TYPE}`

contactName:`string`

leadTypeName:`string`

#### title

<a><span class="http-get">GET</span></a> `/v1/list/{TITLE}`

#### nationality

<a"><span class="http-get">GET</span></a> `/v1/list/{NATIONALITY}`

#### gender

<a><span class="http-get">GET</span></a> `/v1/list/{GENDER}`

firstName:`string`

lastName:`string`

middleName:`string`

dateOfBirth:`yyyy-mm-dd` 

occupation:`string`

#### customerCountry <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{COUNTRY}`  

#### customerRegion <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{REGION}?parentId={customerCountry.value}`

#### customerCity <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{CITY}?parentId={customerRegion.value}`

address1:`string`

address2:`string`

#### phoneCode <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{PHONE_CODE}`

phoneNumber:`string`

!!! note "phoneNumber length should be 9 characters"

email:`string`

#### monthlyIncome

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_MONTHLY_INCOME}`

preferredLanguage <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LANGUAGE}`

preferredContactType

<a><span class="http-get">GET</span></a> `/v1/list/{CONTACT_TYPE}`

company:`Aljabr Trading Company`

ou <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{OU_TYPE}`

businessArea <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{BUSINESS_AREA}?parentId={ou_type.value}`

branch <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{BRANCH_TYPE}?parentId={branch_type.value}`

leadDate:`string` <span class="flag-required">*</span>

leadInterest <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_INTEREST}`

source <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_SOURCE}`

subSource <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_SUB_SOURCE}?parentId={lead_source.value}`

leadName:`string` <span class="flag-required">*</span>

leadReference:`string`

leadNote:`string`

#### vehicleType

<a><span class="http-get">GET</span></a> `/v1/list/{VEHICLE_TYPE}`

vehicles.modelFamily

<a><span class="http-get">GET</span></a> `/v1/list/{MODEL}?parentId={ou_type.value}`

vehicles.modelYear

<a><span class="http-get">GET</span></a> `/v1/list/{MODEL_YEAR}`

<!-- should I keep as not in json -->
vehicles.modelMemo:`string`

<!-- should I keep as not in json -->
vehicles.modelPreferences:`string`

<!-- should I keep as not in json -->
vehicles.totalQty:`string`


purchasePlan

<a><span class="http-get">GET</span></a> `/v1/list/{PURCHASE_PLAN}`

paymentMode

<a><span class="http-get">GET</span></a> `/v1/list/{PAYMENT_MODE}`

currency

<a><span class="http-get">GET</span></a> `/v1/list/{CURRENCY}`

priority <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_PRIORITY}`

testDriveRequired

<a><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`

acceptNewsLetter

<a><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`

acceptMarketing

<a><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`

acceptPrivatePolicy

<a><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`