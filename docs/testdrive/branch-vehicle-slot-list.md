---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<span class="http-get">GET</span> `/v1/testdrive/branch-vehicle-slot-list`

### Query Parameters

```
companyId: integer                            // Mandatory (default:1)
brandId: integer                              // Mandatory (listId:2)
businessAreaId: integer                       // Mandatory (default:2)
branchId: integer                             // Mandatory (/v1/core/branchlist -> branchId) 
vehicleId: long                               // Mandatory
fromDate: string                              // Mandatory (yyyy-mm-dd,eg:2026-06-20 , fromDate and toDate should be 7 days range) 
toDate: string                                // Mandatory (yyyy-mm-dd,eg:2026-06-20) 
lang: string                                  // Mandatory (default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **branchId:** `10`
    - **vehicleId:** `211`
    - **fromDate:** `2026-06-19`
    - **toDate:** `2026-06-21`

### Response

```json
{
  "dates": [
    {
      "date": "2026-06-19",
      "isWorkingDay": false,
      "errorMessage": "branch-not-working-on-selected-day",
      "shifts": [],
      "nonWorkingDays": [],
      "modelFamilies": []
    },
    {
      "date": "2026-06-20",
      "isWorkingDay": true,
      "shifts": [
        {
          "startTime": "08:00:00",
          "endTime": "21:30:00"
        }
      ],
      "nonWorkingDays": [],
      "modelFamilies": [
        {
          "modelFamilyId": 12,
          "familyText": "Carnival",
          "vehicles": [
            {
              "slots": [
                {
                  "startTime": "08:30:00",
                  "endTime": "08:50:00",
                  "slotMasterId": 20
                },
                {
                  "startTime": "09:00:00",
                  "endTime": "09:20:00",
                  "slotMasterId": 21
                },
                ...
              ],
              "aptVehicleId": 211,
              "name": "KA4 CARNIVAL HEV",
              "modelFamilyId": 12,
              "familyText": "Carnival",
              "plateNoEn": "AVR 2700",
              "vinCode": "KNANC81A9S6056275",
              "variantSummary": "KA4 CARNIVAL HEV 1.6T EX FWD 6A/T 5 DR 8/S/ L1 (PE)",
              "exteriorColor": "SNOW WHITE PEARL",
              "interiorColor": "TUSCAN + UMBER 2TONE",
              "slotType": "Slot",
              "slotCount": 26
            }
          ]
        }
      ]
    },
    {
      "date": "2026-06-21",
      "isWorkingDay": true,
      "shifts": [
        {
          "startTime": "08:00:00",
          "endTime": "21:30:00"
        }
      ],
      "nonWorkingDays": [],
      "modelFamilies": [
        {
          "modelFamilyId": 12,
          "familyText": "Carnival",
          "vehicles": [
            {
              "slots": [
                {
                  "startTime": "08:00:00",
                  "endTime": "08:20:00",
                  "slotMasterId": 19
                },
                {
                  "startTime": "08:30:00",
                  "endTime": "08:50:00",
                  "slotMasterId": 20
                },
                ...
              ],
              "aptVehicleId": 211,
              "name": "KA4 CARNIVAL HEV",
              "modelFamilyId": 12,
              "familyText": "Carnival",
              "plateNoEn": "AVR 2700",
              "vinCode": "KNANC81A9S6056275",
              "variantSummary": "KA4 CARNIVAL HEV 1.6T EX FWD 6A/T 5 DR 8/S/ L1 (PE)",
              "exteriorColor": "SNOW WHITE PEARL",
              "interiorColor": "TUSCAN + UMBER 2TONE",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        }
      ]
    },
  ]
}
```
