---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get the full service category hierarchy
### Returns all parent service categories with nested children.

<span class="http-get">GET</span> `/v1/service-apt/category-hierarchy`

### Query Parameters

```
lang: string                            // Optional (default: en) "en" | "ar"
```

### Response

```json
[
  {
    "id": 10,
    "parentId": null,
    "name": "Periodic Maintenance",
    "nameAr": "صيانة دورية",
    "description": "Scheduled service",
    "defaultLimit": 8,
    "isActive": true,
    "icon": "data:image/svg+xml;base64,PHN2Zy8+",
    "createDate": "2026-01-01T10:00:00",
    "modifiedDate": "2026-06-01T10:00:00",
    "createBy": 1001,
    "modifiedBy": 1001,
    "children": [
      {
        "id": 20,
        "parentId": 10,
        "name": "Oil Change",
        "nameAr": "تغيير زيت",
        "description": "Oil and filter",
        "defaultLimit": 4,
        "isActive": true,
        "icon": "data:image/svg+xml;base64,PHN2Zy8+",
        "createDate": "2026-01-01T10:00:00",
        "modifiedDate": "2026-06-01T10:00:00",
        "createBy": 1001,
        "modifiedBy": 1001,
        "children": []
      }
    ]
  }
]
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
