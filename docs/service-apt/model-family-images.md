---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get images for specific model families
### Returns active images for the requested model family ids only (repeat modelFamilyIds per id). Families without images are omitted.

<span class="http-get">GET</span> `/v1/service-apt/model-family-images`

### Query Parameters

```
modelFamilyIds: array[integer]          // Repeat query key per id
companyId: integer                      // Optional (default: 1)
brandId: integer                        // Optional
```

!!! note

    **Example:**

    - **modelFamilyIds:** `1001`
    - **companyId:** `1`
    - **brandId:** `1`

### Response

```json
[
  {
    "modelFamilyId": 1001,
    "images": [
      "models/kia/sportage/front.jpg"
    ]
  }
]
```

### Response (400)

```json
{
  "message": "modelFamilyIds is required"
}
```
