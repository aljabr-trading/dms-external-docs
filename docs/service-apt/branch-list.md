---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get service appointment branch list

### Returns service-appointment enabled branches for a required company and brand. Optional filters: operating unit, business area (department), region, city, branch, and language. lang localizes branch text.

<span class="http-get">GET</span> `/v1/service-apt/branch-list`

### Query Parameters

```
companyId: integer                            // Mandatory
brandId: integer                              // Mandatory
ouId: integer                                 // Optional
businessAreaId: integer                       // Optional
regionId: integer                             // Optional
cityId: integer                               // Optional
branchId: integer                             // Optional
categoryId: integer                           // Optional
subCategoryId: integer                        // Optional
lang: string                                  // Optional (default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `3`
    - **lang:** `en`

### Response

```json
[
  {
    "companyHierarchyId": 101,
    "branchId": 101,
    "branchCode": "DMM-01",
    "branchText": "Dammam Service Center",
    "countryId": 1,
    "countryText": "Saudi Arabia",
    "description": "Service center",
    "regionId": 1,
    "regionText": "Eastern Province",
    "cityId": 1,
    "cityText": "Dammam",
    "addressText": "King Fahd Road",
    "brandId": 1,
    "brandText": "KIA",
    "brandCode": "KIA",
    "ouId": 1,
    "ouText": "ALJ Motors",
    "ouTextAr": "عبداللطيف جميل للسيارات",
    "departmentId": 3,
    "departmentText": "Service",
    "location": "Dammam",
    "notesText": "Appointments required",
    "workingHoursText": "Sun-Thu 08:00-17:00",
    "email": "service.dmm@example.com",
    "unifiedNumber": "920000000",
    "longitude": "50.0888",
    "latitude": "26.4207",
    "branchCategoryText": "Service Center",
    "branchUsageText": "Service",
    "branchTypeText": "Main",
    "contactPerson": "Ahmed Ali",
    "contactPersonNo": "555123456",
    "operations": [
      {
        "operationId": 1,
        "operationText": "Service"
      }
    ],
    "companyHierarchyVersionId": 1
  }
]
```

### Response (400)

```json
{
  "message": "Company access denied"
}
```
