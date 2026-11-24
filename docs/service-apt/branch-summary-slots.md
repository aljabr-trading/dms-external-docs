---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get category summary availability slots
### Returns category summary availability for the date range. The range must start after today, endDate cannot exceed startDate plus 7 days, and both dates must stay within the next 7 days. Optional filters: company, brand, department, category, subcategory, and branch. lang localizes CompanyText, BrandText, BranchText, RegionText, CategoryText, and SubCategoryText.

<span class="http-get">GET</span> `/v1/service-apt/branch-summary-slots`

### Query Parameters

```
startDate: date-time                    // Mandatory (must be after today; within next 7 days)
endDate: date-time                      // Mandatory (cannot exceed startDate + 7 days; within next 7 days)
companyId: integer                      // Mandatory
brandId: integer                        // Mandatory
departmentId: integer                   // Mandatory (Default: 3)
categoryId: array[integer]              // Optional (repeat query key per value)
subCategoryId: array[integer]           // Optional (repeat query key per value)
branchId: array[integer]                // Optional (repeat query key per value)
lang: string                            // Optional (Default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **startDate:** `2026-06-22T00:00:00`
    - **endDate:** `2026-06-25T00:00:00`
    - **companyId:** `1`
    - **brandId:** `1`
    - **departmentId:** `3`
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
    "limit": 8,
    "selectDate": "2026-06-22T00:00:00",
    "aptMasterId": 500,
    "usedLimit": 3,
    "blockedLimit": 1,
    "advisorCount": 2,
    "availableLimit": 4
  }
]
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "startDate must be greater than today",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```
