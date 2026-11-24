---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Reschedule service appointment booking
### Reschedules an existing service appointment booking to a new slot. Fails with 404 when the booking is not found, or 400 when the booking is already cancelled or closed.

<span class="http-post">POST</span> `/v1/service-apt/reschedule/{id}`

### Path Parameters

```
id: integer                             // Mandatory (service request id)
```

### Request Payload

```json
{
  "srDetailRequestId": 70001,           // Existing detail line id
  "branchId": 101,                      // Optional
  "regionId": 1,                        // Optional
  "categoryId": 10,
  "subCategoryId": 20,
  "aptMasterId": 500,
  "aptSlotId": 1202,
  "advisorId": 3001,
  "requestDate": "2026-06-23T00:00:00",
  "startDate": "2026-06-23T11:00:00",
  "endDate": "2026-06-23T12:00:00",
  "statusId": 1,                        // Optional enum 1 | 2 | 3
  "milage": 15100,
  "rescheduleReasonId": 1,
  "remarks": "Customer requested a later slot",
  "customerRemarks": "Please call before arrival",
  "lang": "en",                         // Optional "en" | "ar"
  "sendCommunicationConfirmation": true,
  "communicationType": 1,               // 1 = SMS, 3 = WhatsApp
  "isFromPortal": false
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
  "statusId": 1,
  "customerName": "Ahmed Ali",
  "customerNumber": "555123456",
  "categoryId": 10,
  "subCategoryId": 20,
  "advisorId": 3001,
  "startDate": "2026-06-23T11:00:00",
  "endDate": "2026-06-23T12:00:00",
  "requestDate": "2026-06-22T00:00:00",
  "remarks": "Customer requested a later slot",
  "customerRemarks": "Please call before arrival"
}
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "Request cannot be rescheduled",
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
