---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<span class="http-get">GET</span> `/v1/vehicle-details/model-family-variants`

### Query Parameters

```
companyId: integer                      // Mandatory (default: 1)
brandId: integer                        // Mandatory
businessAreaId: integer                 // Mandatory (default: 2)
modelFamilyId: integer                  // Mandatory
lang: string                            // Mandatory (default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **modelFamilyId:** `18`
    - **lang:** `en`

### Response

```json
{
  "items": [
    {
      "modelVariantId": 2651,
      "variantCode": "H7S4K461BD/D416",
      "name": "PEGAS 1.4L LX FWD 4A/T 4 DR 5/S/ S1",
      "trimCode": "S1",
      "modelYears": [2026]
    },
    {
      "modelVariantId": 2653,
      "variantCode": "H7S4K461BD/D454",
      "name": "PEGAS 1.4L LX FWD 4A/T 4 DR 5/S/ S1",
      "trimCode": "S1",
      "modelYears": [2026]
    }
  ]
}
```
