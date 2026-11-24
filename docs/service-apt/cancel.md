---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Cancel service appointment booking
### Cancels an existing service appointment booking. Fails with 404 when the booking is not found, or 400 when the booking is already cancelled or closed.

<span class="http-post">POST</span> `/v1/service-apt/cancel/{id}`

### Path Parameters

```
id: integer                             // Mandatory (service request id)
```

### Request Payload

```json
{
  "categoryId": 10,
  "subCategoryId": 20,
  "aptMasterId": 500,
  "aptSlotId": 1201,
  "requestDate": "2026-06-22T00:00:00",
  "statusId": 4,                        // Mandatory (4 = Cancel, 2 = No Show)
  "srDetailRequestId": 70001,           // Mandatory (claim from bookings)
  "remarks": "Customer requested cancellation",
  "cancelReasonId": 1,                  // Mandatory (Default: 1)
  "lang": "en",                         // Optional "en" | "ar"
  "sendCommunicationConfirmation": true,
  "communicationType": 1,               // 1 = SMS
}
```

### Response

```json
{
  "serviceRequestId": 90001,
  "requestNo": "SA-2026-0001",
  "companyId": 1,
  "brandId": 1,
  "branchId": 101,
  "businessAreaId": 3,
  "statusId": 4,
  "customerName": "Ahmed Ali",
  "customerNumber": "555123456",
  "categoryId": 10,
  "subCategoryId": 20,
  "advisorId": 3001,
  "startDate": "2026-06-22T09:00:00",
  "endDate": "2026-06-22T10:00:00",
  "requestDate": "2026-06-22T00:00:00",
  "remarks": "Customer requested cancellation"
}
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "Request cannot be cancelled",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```

### Response (404)

```json
{
  "applicationId": null,
  "status": 404,
  "errorCode": "DMS-Error-001",
  "operationError": "Service request not found",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```
