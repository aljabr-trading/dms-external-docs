---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<span class="http-get">GET</span> `/v1/testdrive/branch-list`

### Query Parameters

```
companyId: integer
brandId: integer
businessAreaId: integer
regionId: integer (optional)
cityId: integer (optional)
branchId: integer (optional)
lang: string (Default: en)
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **lang:** `en`

### Response

```json
[
  {
    "companyHierarchyId": 16,
    "branchId": 10,
    "branchCode": "KIA1",
    "branchText": "Dammam - Khobar Highway",
    "countryId": 1,
    "countryText": "Saudi Arabia",
    "description": "Dammam - Khobar Highway",
    "regionId": 1,
    "regionText": "Eastern",
    "cityId": 1,
    "cityText": "Dammam",
    "addressText": "King Fahad Road, Al Khalidiyyah Al Janubiyyah, Dammam",
    "brandId": 1,
    "brandText": "KIA",
    "brandCode": "KIA",
    "departmentId": 2,
    "departmentText": "Sales",
    "location": "https://maps.app.goo.gl/cdJ6reAkeERUKh7w6",
    "notesText": "Normal shifts",
    "workingHoursText": "From Saturday to Thursday: \r\nfrom 8:00 AM to 9:00 PM\r\nFriday:\r\nfrom 4:00 PM to 8:00 PM",
    "email": "kia@aljabrauto.com",
    "unifiedNumber": "920014200",
    "longitude": null,
    "latitude": null,
    "branchCategoryText": "3S",
    "branchUsageText": "Multi Brand",
    "branchTypeText": "Operation",
    "operations": null
  },
  {
    "companyHierarchyId": 23,
    "branchId": 17,
    "branchCode": "KIA8",
    "branchText": "Riyadh - Khurais",
    "countryId": 1,
    "countryText": "Saudi Arabia",
    "description": "Riyadh - Khurais",
    "regionId": 2,
    "regionText": "Central",
    "cityId": 3,
    "cityText": "Riyadh",
    "addressText": "Kharis Branch Rd, An Nasim Ash Sharqi, Riyadh",
    "brandId": 1,
    "brandText": "KIA",
    "brandCode": "KIA",
    "departmentId": 2,
    "departmentText": "Sales",
    "location": "https://maps.app.goo.gl/CTV3CKNFU7SdTFnLA",
    "notesText": "Normal shifts",
    "workingHoursText": "From Sunday to Thursday:\r\nFrom 8:30 AM to 8:30 PM\r\nSaturday: \r\nMorning period from 9:00 AM to 12:00 PM  Eevening period from 4:00 AM to 8:00 PM\r\nFriday:\r\nFrom 4:00 PM to 8:30 PM",
    "email": "kia@aljabrauto.com",
    "unifiedNumber": "920014200",
    "longitude": null,
    "latitude": null,
    "branchCategoryText": "3S",
    "branchUsageText": "Multi Brand",
    "branchTypeText": "Operation",
    "operations": null
  }
]
```
