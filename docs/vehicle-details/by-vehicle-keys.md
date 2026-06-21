---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<span class="http-get">GET</span> `/v1/vehicle-details/by-vehicle-keys`

### Query Parameters

```
companyId: integer                    // Mandatory (default: 1)
brandId: integer                      // Mandatory
businessAreaId: integer               // Mandatory (default: 2)
modelFamilyId: integer                // Mandatory
variantCode: string                   // Mandatory
modelYear: integer                    // Mandatory
lang: string                          // Mandatory (default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **modelFamilyId:** `18`
    - **variantCode:** `H7S4K461BD/D416`
    - **modelYear:** `2026`
    - **lang:** `en`

### Response

```json
{
  "variantModelYearId": 12,
  "trimCode": "S1",
  "brandId": 1,
  "brandCode": "KIA",
  "modelName": "AB PEGAS",
  "modelYear": 2026,
  "trimName": "LX",
  "variantCode": "H7S4K461BD/D416",
  "categories": [
    {
      "specificationCategoryId": 10,
      "name": "Basic Specifications",
      "sortOrder": 1,
      "rows": [
        {
          "key": "Engine",
          "value": "MPI"
        },
        {
          "key": "Transmission",
          "value": "4-speed Automatic Transmission"
        },
        {
          "key": "Fuel Consumption",
          "value": "Fuel Consumption Rate (17.5 Km/L)"
        },
        {
          "key": "Fuel Tank Capacity",
          "value": "Fuel Tank Capacity: 43L"
        },
        {
          "key": "Dimensions",
          "value": "Dimensions: 4,300 / 1,700 / 1,460 / 2,570 mm"
        },
        {
          "key": "Displacement",
          "value": "1.4 L"
        },
        {
          "key": "Configuration",
          "value": "Inline 4-cylinder"
        }
      ]
    },
    {
      "specificationCategoryId": 11,
      "name": "Exterior Features",
      "sortOrder": 2,
      "rows": [
        {
          "key": "Wheels",
          "value": "14\" Steel Wheels"
        },
        {
          "key": "Rear Sensors",
          "value": "Rear Sensors"
        },
        {
          "key": "Keyless Entry",
          "value": "Keyless Entry"
        },
        {
          "key": "Electric Mirrors",
          "value": "Electric Outside Mirrors"
        },
        {
          "key": "Body-colored Parts",
          "value": "Body-colored Handles & Mirrors"
        },
        {
          "key": "Side Mirror Indicators",
          "value": "Outside Mirror Side Repeater"
        },
        {
          "key": "Mud Guard",
          "value": "Mud Guard"
        }
      ]
    },
    {
      "specificationCategoryId": 12,
      "name": "Interior Features",
      "sortOrder": 3,
      "rows": [
        {
          "key": "Seats",
          "value": "Cloth Seats"
        },
        {
          "key": "Air Conditioning",
          "value": "Manual A/C"
        },
        {
          "key": "USB Connection",
          "value": "USB Connection"
        },
        {
          "key": "Bluetooth",
          "value": "AUX"
        },
        {
          "key": "Steering Audio Control",
          "value": "Steering Audio Control"
        }
      ]
    },
    {
      "specificationCategoryId": 13,
      "name": "Safety Features",
      "sortOrder": 4,
      "rows": [
        {
          "key": "Parking Brake",
          "value": "Hand Parking"
        }
      ]
    }
  ]
}
```
