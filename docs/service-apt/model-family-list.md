---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get brand model families with images
### Returns the brand's model families (core lookup list) with their active images. lang localizes the family text.

<span class="http-get">GET</span> `/v1/service-apt/model-family-list`

### Query Parameters

```
companyId: integer                      // Optional (default: 1)
brandId: integer                        // Optional
lang: string                            // Optional (default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **lang:** `en`

### Response

```json
{
  "modelFamilies": [
    {
      "modelFamilyId": 1001,
      "familyText": "Sportage",
      "images": [
        "models/kia/sportage/front.jpg"
      ]
    }
  ]
}
```

### Response (400)

```json
{
  "message": "no-data-found"
}
```
