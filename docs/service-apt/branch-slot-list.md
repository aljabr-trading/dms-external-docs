---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get nested branch service appointment availability
### Returns a date-first nested tree from ServiceRequestSlotsExternal: dates → branches (with isWorkingDay, shifts, nonWorkingDays) → categories → subcategories → slots. The range must start after today, endDate cannot exceed startDate plus 7 days, and both dates must stay within the next 7 days. Optional filters: company, brand, ou, department, region, category, subcategory, and branch. lang localizes branch/category names.

<span class="http-get">GET</span> `/v1/service-apt/branch-slot-list`

### Query Parameters

```
startDate: date-time                    // Mandatory (must be after today; within next 7 days)
endDate: date-time                      // Mandatory (cannot exceed startDate + 7 days; within next 7 days)
companyId: integer                      // Optional
brandId: integer                        // Optional
ouId: integer                           // Optional
departmentId: integer                   // Optional
regionId: array[integer]                // Optional (repeat query key per value)
categoryId: array[integer]              // Optional (repeat query key per value)
subCategoryId: array[integer]           // Optional (repeat query key per value)
branchId: array[integer]                // Optional (repeat query key per value)
lang: string                            // Optional (default: en) "en" | "ar"
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
{
  "dates": [
    {
      "date": "2026-06-22",
      "branches": [
        {
          "regionId": 1,
          "regionName": "Eastern Province",
          "branchId": 101,
          "branchName": "Dammam Service Center",
          "isWorkingDay": true,
          "shifts": [
            {
              "startTime": "08:00:00",
              "endTime": "17:00:00"
            }
          ],
          "nonWorkingDays": [],
          "categories": [
            {
              "categoryId": 10,
              "name": "Periodic Maintenance",
              "subCategories": [
                {
                  "subCategoryId": 20,
                  "name": "Periodic",
                  "slots": [
                    {
                      "startTime": "09:00:00",
                      "endTime": "10:00:00",
                      "aptSlotId": 1201,
                      "aptMasterId": 500
                    }
                  ]
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}
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
