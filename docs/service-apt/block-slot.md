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
    "companyId": 1,                             // Mandatory
    "ouId": 1,                                  // Optional (resolved server-side when omitted)
    "brandId": 1,                               // Mandatory
    "branchId": 101,                            // Mandatory
    "businessAreaId": 3,                        // Mandatory
    "regionId": 1,                              // Mandatory
    "categoryId": 10,                           // Mandatory
    "subCategoryId": 20,                        // Mandatory
    "reqDate": "2026-06-22T00:00:00",           // Mandatory (Date of the slot)
    "aptMasterId": 500,                         // Mandatory (Appointment master id)
    "aptSlotId": 1201,                          // Mandatory (Appointment slot id)
    "advisorId": 3001,                          // Optional (resolved server-side when omitted)
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
