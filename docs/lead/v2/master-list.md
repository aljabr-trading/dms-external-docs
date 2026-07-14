---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Master list based on lookup types (with language specific)
<span class="http-get">GET</span> `/v2/leads/list`

### Query Parameters

```
listId: integer (default: 0)
parentListId: integer (default: 0)
parentId: integer (default: 0)
lang: string (default "en") "en" | "ar"
``` 

This will provide the master list based on the language provided, default is en

### Response

```json
[
  {
    "listName": "Company",
    "id": 1,
    "text": "JTC",                                // Text based on lang passed
    "code": "JTC",
    "listId": 0,
    "parentListId": 0,
    "parentId": 0,
    "regularExpression": ""
  },
  {
    "listName": "Branch",
    "id": 1,
    "text": "الرياض - القادسية",                // Text based on lang passed
    "code": "LYK1",
    "listId": 1,
    "parentListId": 0,
    "parentId": 0,
    "regularExpression": ""
  }
]
```

## Branch list (with language specific)
<span class="http-get">GET</span> `/v2/leads/branchlist`

### Query Parameters

```
brandId: integer (default: 0)
departmentId: integer (default: 0)
regionId: integer (default: 0)
cityId: integer (default: 0)
branchId: integer (default: 0)
lang: string (default "en") "en" | "ar"
``` 

This will provide the branch list based on the language provided, default is en

### Response

```json
[
  {
    "branchId": 2,
    "branchCode": "LYK2",
    "branchText": "Dammam - Rakah Showroom",
    "countryId": 1,
    "countryText": "Saudi Arabia",
    "description": "Dammam - Rakah Showroom",
    "regionId": 1,
    "regionText": "Eastern",
    "cityId": 1,
    "cityText": "Dammam",
    "addressText": "Al Rakah Ash Shamaliyah, Dammam",
    "brandId": 3,
    "brandText": "Lynk&Co",
    "brandCode": "LYNKCO",
    "departmentId": 2,
    "departmentText": "Sales",
    "location": "https://maps.app.goo.gl/z2Cnp6N5PD5zAjiD7",
    "notesText": null
  },
  {
    "branchId": 4,
    "branchCode": "JMC1",
    "branchText": "Dammam - Rakah Showroom",
    "countryId": 1,
    "countryText": "Saudi Arabia",
    "description": "Dammam - Rakah Showroom",
    "regionId": 1,
    "regionText": "Eastern",
    "cityId": 1,
    "cityText": "Dammam",
    "addressText": "Al Rakah Ash Shamaliyah, Dammam",
    "brandId": 2,
    "brandText": "JMC",
    "brandCode": "JMC",
    "departmentId": 2,
    "departmentText": "Sales",
    "location": "https://maps.app.goo.gl/kqM6z5VAfL4kNKCa7",
    "notesText": null
  },
]
```
