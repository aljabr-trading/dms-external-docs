---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get service appointment slot details
### Returns availability grouped by time window (startDate/endDate) for a single aptDate. Each item includes availableStatus = 1 when at least one advisor is free, and userIds listing those available advisors. The date must be after today and within the next 7 days. Hierarchy can be supplied as companyHierarchyId or as companyId, ouId, brandId, departmentId, and branchId. Optional filters: regionIds, branchIds, statusIds, advisorIds, categoryId, and subCategoryId.

<span class="http-get">GET</span> `/v1/service-apt/slot-details`

### Query Parameters

```
aptDate: date-time                      // Mandatory (after today; within next 7 days)
companyHierarchyId: integer             // Optional (or supply companyId/ouId/brandId/departmentId/branchId)
companyId: integer                      // Optional
ouId: integer                           // Optional
brandId: integer                        // Optional
departmentId: integer                   // Optional
branchId: integer                       // Optional
regionIds: array[integer]               // Optional (repeat query key per value)
branchIds: array[integer]               // Optional (repeat query key per value)
statusIds: array[integer]               // Optional (repeat query key per value)
advisorIds: array[integer]              // Optional (repeat query key per value)
categoryId: array[integer]              // Optional (repeat query key per value)
subCategoryId: array[integer]           // Optional (repeat query key per value)
lang: string                            // Optional (default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **aptDate:** `2026-06-22T00:00:00`
    - **companyId:** `1`
    - **brandId:** `1`
    - **departmentId:** `3`
    - **branchId:** `101`
    - **lang:** `en`

### Response

```json
[
  {
    "companyId": 1,
    "ouId": 1,
    "brandId": 1,
    "businessAreaId": 3,
    "regionId": 1,
    "branchId": 101,
    "categoryId": 10,
    "subCategoryId": 20,
    "companyText": "ALJ",
    "brandText": "KIA",
    "branchText": "Dammam Service Center",
    "regionText": "Eastern Province",
    "categoryText": "Periodic Maintenance",
    "subCategoryText": "Oil Change",
    "availableStatus": 1,
    "userIds": [
      3001,
      3002,
      3003
    ],
    "aptSlotId": 1201,
    "aptMasterId": 500,
    "selectDate": "2026-06-22T00:00:00",
    "startDate": "2026-06-22T09:00:00",
    "endDate": "2026-06-22T10:00:00",
    "startTime": "09:00:00",
    "endTime": "10:00:00"
  }
]
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "company-hierarchy-incomplete",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```
