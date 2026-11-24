---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Block or unblock service appointment slots
### Creates or clears blocked service request slots. The request body is a list of BlockServiceRequest items. Hierarchy identifiers are resolved server-side when incomplete.

<span class="http-post">POST</span> `/v1/service-apt/block-slot`

### Query Parameters

```
lang: string                            // Optional (default: en) "en" | "ar"
```

### Request Payload

```json
[
  {
    "isBlock": true,                            // true = block, false = unblock
    "companyHierarchyId": 101,                  // Optional (resolved server-side when omitted)
    "companyId": 1,                             // Optional
    "ouId": 1,                                  // Optional
    "brandId": 1,                               // Optional
    "branchId": 101,                            // Optional
    "businessAreaId": 3,                        // Optional
    "regionId": 1,                              // Optional
    "categoryId": 10,                           // Optional
    "subCategoryId": 20,                        // Optional
    "reqDate": "2026-06-22T00:00:00",           // Date of the slot
    "aptMasterId": 500,                         // Appointment master id
    "aptSlotId": 1201,                          // Appointment slot id
    "advisorId": 3001,                          // Optional
    "remarks": "Blocked for maintenance"        // Optional
  }
]
```

### Response

```json
{
  "blockId": 88001,
  "advisorId": 3001
}
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "Request body is required.",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```
