---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<span class="http-get">GET</span> `/v1/vehicle-details/model-family`

### Query Parameters

```
companyId: integer
brandId: integer
businessAreaId: integer
lang: string
```

!!! note

    **`companyId` and `brandId` are mandatory fields.**

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **lang:** `en`

### Response

```json
{
  "items": [
    {
      "modelFamilyId": 18,
      "code": "PEGAS",
      "name": "Pegas",
      "description": "Pegas"
    },
    {
      "modelFamilyId": 1,
      "code": "PICANTO",
      "name": "Picanto",
      "description": "Picanto"
    }
  ]
}
```
