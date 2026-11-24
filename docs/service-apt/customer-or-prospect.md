---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Search customers and prospects by company code and mobile
### Resolves companyCode to a company, then searches UnifiedCustomerProspect by partial mobileNumber. RecordType 1 = Customer, 2 = Prospect. If a customer exists for the mobile, only that customer is returned. If no customer exists, prospects are returned: pickTop=1 (default) returns the latest prospect per full mobile; pickTop=0 returns all matching prospects.

<span class="http-get">GET</span> `/v1/core/customer-or-prospect`

### Query Parameters

```
companyCode: string                     // Company code
mobileNumber: string                    // Partial mobile number
pickTop: integer                        // Optional (default: 1) 1 = latest prospect per mobile, 0 = all matching prospects
```

!!! note

    **Example:**

    - **companyCode:** `ALJ`
    - **mobileNumber:** `555123456`
    - **pickTop:** `1`

### Response

```json
[
  {
    "customerId": 4001,
    "customerVersionId": 1,
    "prospectId": null,
    "recordType": 1,
    "recordTypeName": "Customer",
    "firstName": "Ahmed",
    "middleName": null,
    "lastName": "Ali",
    "companyName": null,
    "contactName": "Ahmed Ali",
    "nationalityId": 1,
    "genderId": 1,
    "customerTypeId": 1,
    "dateOfBirth": "1990-01-15T00:00:00",
    "emailAddress": "ahmed.ali@example.com",
    "phoneCodeId": 1,
    "mobileNumber": "555123456",
    "fullMobilePhone": "966555123456",
    "preferredLanguageId": 1,
    "identificationTypeId": 1,
    "identificationNo": "1234567890",
    "countryId": 1,
    "regionId": 1,
    "cityId": 1,
    "companyId": 1,
    "ouId": 1,
    "businessAreaId": 3,
    "applicationId": 1,
    "isActive": true,
    "isEnable": true,
    "userActive": true,
    "createdBy": 1001,
    "createdDate": "2026-01-01T10:00:00",
    "modifiedBy": 1001,
    "modifiedDate": "2026-06-01T10:00:00"
  }
]
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "dms-invalid-data",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```
