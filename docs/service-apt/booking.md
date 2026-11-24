---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Create service appointment booking
### Creates a new service appointment booking from nested customer, vehicle, and slot details. When customerId > 0 uses CustomerId; when customerId is -1 and prospectId > 0 uses ProspectId; when both are -1 creates a prospect.

<span class="http-post">POST</span> `/v1/service-apt/booking`

---

Refer the comment <span class="flag-required"> //Mandatory</span> means the property is required

### Request Payload

```json
{
  "companyId": 1,                             // Mandatory
  "brandId": 1,                               // Mandatory
  "branchId": 101,                            // Mandatory
  "businessAreaId": 3,                        // Mandatory
  "regionId": 1,                              // Mandatory
  "sourceId": 1,                              // Mandatory (1 = Direct Contact)
  "subSourceId": 2,                           // Mandatory (10 = Website)
  "customer": {                               // Mandatory
    "customerId": 4001,                       // Optional (> 0 uses customer; -1 with prospectId -1 creates prospect)
    "customerVersionId": 1,                   // Optional
    "prospectId": -1,                         // Optional (used when customerId is -1)
    "firstName": "Ahmed",                     // Optional (Required if customerTypeId 1)
    "lastName": "Ali",                        // Optional (Required if customerTypeId 1)
    "customerName": "Ahmed Ali",              // Optional (used when firstName/lastName are not both provided)
    "phoneCode": "966",                       // Optional (e.g. "966" or "+966")
    "phoneNumber": "555123456",               // Optional
    "emailAddress": "ahmed.ali@example.com",  //Optional
    "customerTypeId": 1,                      // 1 = Individual, 2 = Company
    "companyName": "",                        // Optional (Required if customerTypeId 2)
    "contactName": "Ahmed Ali"                // Optional (Required if customerTypeId 2)
  },
  "vehicle": {                                // Mandatory
    "customerVehicleId": 5001,                // Optional (-1 when not yet registered)
    "prospectVehicleId": -1,                  // Optional
    "vinCode": "KNAAE12345A123456",           // Mandatory
    "plateNo": "1234-ABD",                    // Mandatory
    "plateNoAr": "د ب أ-1234",                // Optional
    "brandId": 1,                             // Mandatory
    "modelFamilyId": 1001,                    // Mandatory
    "modelYearId": 2026,                      // Mandatory
    "colorId": 1                              // Optional
  },
  "requestDate": "2026-06-23T00:00:00",       // Mandatory
  "milage": 15000,                            // Required (> 0)
  "remarks": "Periodic maintenance",          // Required
  "customerRemarks": "Please call before arrival",
  "srRequests": [                             // Mandatory
    {
      "categoryId": 10,                       // Mandatory
      "subCategoryId": 20,                    // Mandatory
      "aptSlotId": 1201,                      // Mandatory
      "aptMasterId": 500,                     // Mandatory
      "requestDate": "2026-06-23T00:00:00",   // Mandatory
      "startDate": "2026-06-23T09:00:00",     // Mandatory
      "endDate": "2026-06-23T10:00:00",       // Mandatory
      "advisorId": 3001                       // Optional (advisor claimed by block-slot)
    }
  ],
  "lang": "en",                               // Mandatory
  "sendCommunicationConfirmation": true,      // Mandatory
  "communicationType": 1                      // Mandatory (default = 1)
}
```

### Response

```json
{
  "success": true,
  "requestMasterId": 90001,
  "requestNo": "SA-2026-0001",
  "communicationId": 70001,
  "sendCommunicationConfirmation": true,
  "communicationType": 1,
  "communicationMessage": "Your service appointment has been booked."
}
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "Failed to create service request.",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```
