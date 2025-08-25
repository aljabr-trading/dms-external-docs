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

#### Response  <!-- confirmed by mr kripa about keeping the time -->
```json
{
  "leads": [
    {
      "leadExternalId": 574,
      "leadId": 0,
      "createdDate": "2025-08-24T11:17:36.787",
      "isError": 0,
      "errorList": null,

      "leadType": "Individual",
      "title": "Mr",
      "gender": "Male",
      "nationality": "saudi",
      "firstName": "first name",
      "middleName": "middle name",
      "lastName": "last name",
      "contactName": "string",
      "companyName": "string",
      "companyIndustryType": "string",
      "dateOfBirth": "2022-08-12T00:00:00",
      "occupation": "occupation",
      "customerCountry": "Saudi Arabia",
      "customerRegion": "Riyadh",
      "customerCity": "Afif",
      "address1": "address1",
      "address2": "address2",
      "phoneCode": "00966",
      "phoneNumber": "500000005",
      "email": "john@example.com",
      "monthlyIncome": "5000-10000 SAR",
      "preferredLanguage": "Arabic",
      "preferredContactType": "Email",
      "company": "JTC",
      "brand": "KIA",
      "businessArea": "Sales",
      "branch": null,
      "leadDate": "2025-08-12T00:00:00",
      "interest": "Price Quote",
      "source": "Direct Contact",
      "subSource": "Email",
      "leadName": "leadname",
      "leadReference": "lead reference",
      "leadNote": "leadnote",
      "vehicleType": "New",
      "vehicles": [
        {
          "leadVehiclesId": 575,
          "createdDate": "2025-08-24T14:17:36.817",
          "modelFamily": "RIO",
          "modelYear": 2024,
          "modelMemo": "Model Memo",
          "modelPreferences": "Model Preferences",
          "totalQty": 1
        }
      ],
      "purchasePlan": "Within 30 Days",
      "paymentMode": "Credit",
      "currency": "SAR",
      "priority": "Warm",
      "testDriveRequired": true,
      "acceptNewsLetter": true,
      "acceptMarketing": true,
      "acceptPrivatePolicy": true
    }
  ],
  "createdDate": "2025-08-24T11:17:36.767",
  "createdBy": 1,
  "totalRecords": 1,
  "errorRecords": 0,
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