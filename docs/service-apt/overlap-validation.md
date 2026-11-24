---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Validate service sub-category overlap
### Checks whether a booking with the given sub-categories stays within the sub-category overlap limit for the vehicle. Existing active future bookings are matched by customerVehicleId, then prospectVehicleId, then vinCode. Pass serviceRequestId when validating a reschedule or update so that booking is not counted. Always returns 200 with isValid and message.

<span class="http-post">POST</span> `/v1/service-apt/validate-overlap`

### Request Payload

```json
{
  "companyId": 1,                       // Mandatory
  "brandId": 1,                         // Mandatory
  "businessAreaId": 3,                  // Optional
  "branchId": 101,                      // Optional
  "customerVehicleId": 5001,            // Optional (matched first)
  "prospectVehicleId": 0,               // Optional (matched when vehicle id is not supplied)
  "vinCode": "KNAAE12345A123456",       // Optional (matched when neither vehicle id is supplied)
  "subCategoryIds": [20],               // Mandatory
  "serviceRequestId": 0                 // Optional (exclude this booking when validating a reschedule or update)
}
```

### Response

```json
{
  "isValid": true,
  "message": "valid"
}
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "At least one subCategoryIds item is required.",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```
