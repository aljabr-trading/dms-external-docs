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
companyId: integer                // Mandatory (default: 1)
brandId: integer                  // Mandatory
businessAreaId: integer           // Mandatory (default: 2)
lang: string                      // Mandatory (default: en) "en" | "ar"
```

!!! note

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
