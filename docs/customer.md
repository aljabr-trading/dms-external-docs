---
hide:
  - toc
---

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Customer   
<span class="http-get">GET</span> `/v1/core/customer`

### Query Parameters

```
companyCode: string
customerId: integer (optional)
identificationNo: string (optional)
mobileNumber: string (optional, must start with 5)
referenceNo: string (optional)
lang: string
``` 
!!! note

    **`companyCode` and `lang` are mandatory fields.**

    **Validation Rules:**

    - `mobileNumber` must start with `5`.

    **At least one of the following fields must be provided:**

    - `customerId`

    - `identificationNo`

    - `mobileNumber`

    - `referenceNo`

    **Example:**

    - **companyCode:** `jtc`
    - **customerId:** `54218`
    - **identificationNo:** `2103232123`
    - **mobileNumber:** `568617084`
    - **referenceNo:** `333215`
    - **lang:** `ar`
  
 
### Response

```json
[
  {
    "customerContacts": [
      {
        "contactId": 1,
        "customerId": 54218,
        "customer": null,
        "contactNumber": "568617083",
        "relationTypeId": 3,
        "relationType": "صديق",
        "contactName": null,
        "contactPhoneCodeId": null,
        "phoneCode": "00966",
        "primaryContact": false,
        "contactStartDate": null,
        "contactEndDate": null,
        "isActive": true,
        "contactIsEnable": null,
        "profession": "Test",
        "remarks": ""
      },
      {
        "contactId": 2,
        "customerId": 54218,
        "customer": null,
        "contactNumber": "568617086",
        "relationTypeId": 6,
        "relationType": "أخ",
        "contactName": null,
        "contactPhoneCodeId": null,
        "phoneCode": "00966",
        "primaryContact": false,
        "contactStartDate": null,
        "contactEndDate": null,
        "isActive": true,
        "contactIsEnable": null,
        "profession": "Brother Prof",
        "remarks": ""
      }
    ],
    "versionId": 103932,
    "customerId": 54218,
    "customerVersionId": 1,
    "firstName": null,
    "middleName": null,
    "lastName": null,
    "companyName": "Param IT",
    "contactName": "Parameswaran Kalidas",
    "nationalityId": null,
    "nationality": null,
    "genderId": null,
    "gender": null,
    "customerTypeId": 2,
    "customerType": "شركة",
    "companyTypeId": null,
    "companyType": null,
    "industryTypeId": 4,
    "industryType": "إنشاءات",
    "dateOfBirth": null,
    "occupation": "Company",
    "preferredContactTypeId": 1,
    "preferredContactType": "مكالمة صوتية",
    "emailAddress": "sri1@gmail.com",
    "phoneCodeId": 1,
    "phoneCode": "00966",
    "mobileNumber": "568617084",
    "additionalPhoneCodeId": null,
    "additionalPhoneCode": null,
    "additionalMobileNumber": null,
    "identificationTypeId": 5,
    "identificationType": "رقم السجل التجاري",
    "identificationNo": "2103232123",
    "countryId": 1,
    "country": "المملكة العربية السعودية",
    "regionId": 1,
    "region": "الرياض",
    "cityId": 1,
    "city": "الرياض",
    "zipCode": null,
    "address1": "Holding",
    "address2": "Company",
    "monthlyIncomeId": null,
    "monthlyIncome": null,
    "createdDate": null,
    "isActive": null,
    "preferredLanguageId": 1,
    "preferredLanguage": "العربية",
    "companyId": 1,
    "company": null,
    "nationalAddress": null,
    "commercialRecord": null,
    "plotIdentification": null,
    "buildingNo": null,
    "unitNo": null,
    "vatRegNo": null,
    "startDate": "2026-05-14T14:24:50.61",
    "endDate": null,
    "citySubDivisionName": null,
    "postalCode": "31202",
    "userActive": 1
  }
]
```
 
