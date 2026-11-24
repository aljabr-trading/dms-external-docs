---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Close service appointment booking
### Closes an existing service appointment booking as attend or unattend via StatusId. Fails with 404 when the booking is not found, or 400 when the booking is already cancelled or closed.

<span class="http-post">POST</span> `/v1/service-apt/close/{id}`

### Path Parameters

```
id: integer                             // Mandatory (service request id)
```

### Request Payload

```json
{
  "statusId": 5,                        // 5 = CloseAttend, 6 = CloseUnAttend
  "remarks": "Customer attended"        // Optional
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
  "statusId": 5,
  "customerName": "Ahmed Ali",
  "customerNumber": "555123456",
  "categoryId": 10,
  "subCategoryId": 20,
  "advisorId": 3001,
  "startDate": "2026-06-22T09:00:00",
  "endDate": "2026-06-22T10:00:00",
  "requestDate": "2026-06-22T00:00:00",
  "remarks": "Customer attended"
}
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "Request cannot be closed",
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
