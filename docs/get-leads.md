---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```
<a><span class="http-get">GET</span></a> `/v1/leads/bulks/{id}`

#### Response
```json
{
  "createdDate": "2025-08-15T11:42:22.727",
  "createdBy": 1,
  "totalRecords": 1,
  "errorRecords": 1,
  "leads": [
    {
      "leadExternalId": 5,
      "leadId": 0,
      "createdDate": "2025-08-15T11:42:23.51",
      "isError": 1,
      "vehicles": null,
      "vehicleLists": [
        {
          "leadVehiclesId": 5,
          "createdDate": "2025-08-15T14:42:29.283",
          "modelFamily": "RIO",
          "modelYear": 2024,
          "modelMemo": "Model Memo",
          "modelPreferences": "Model Preferences",
          "totalQty": 1
        }
      ],
      "errorList": [
        {
          "errorId": 33,
          "createdDate": "2025-08-15T17:31:07.35",
          "errorMessage": "Lead Sub Source is Invalid",
          "errorMessageAr": "Lead Sub Source is Invalid",
          "errorCodeId": 1
        }
      ],
      "company": "JTC",
      "businessArea": "Sales",
      "branch": null,
      "brand": "KIA",
      "title": "Mr",
      "nationality": "Saudi",
      "gender": "Male",
      "source": "Direct Contact",
      "subSource": "WhatsApp",
      "phoneCode": "00966",
      "phoneNumber": "500000005",
      "preferredLanguage": "Arabic",
      "preferredContactType": "Email",
      "purchasePlan": "Within 30 Days",
      "paymentMode": "Credit",
      "monthlyIncome": "5000-10000 SAR",
      "currency": "SAR",
      "testDriveRequired": null,
      "acceptNewsLetter": true,
      "acceptMarketing": true,
      "acceptPrivatePolicy": true,
      "priority": "Low",
      "leadType": null,
      "interest": "Price Quote",
      "vehicleType": "New",
      "firstName": "fdsf sdfdsf",
      "middleName": null,
      "lastName": "dfdsf sdfdsf",
      "dateOfBirth": null,
      "occupation": null,
      "address1": null,
      "address2": null,
      "email": "john@example.com",
      "leadName": "sadsad",
      "leadDate": "2025-08-12T00:00:00",
      "leadReference": "dsfsfds",
      "companyIndustryType": "Bank",
      "customerCountry": "Saudi Arabia",
      "customerRegion": "Riyadh",
      "customerCity": "Afif"
    }
  ],
  "isProcessed": 2
}
``` 

!!!Note
    "errorRecords" states the error count
        
    "isProcessed" states the enum of

        1 - means created
        2 - means inprogress
        3 - means cancelled
        4 - means completed

    "leads" states list of leads which are sent against this Id

        "leadId" created in DMS
        "errorList" explains the error that is occuring against the leadId