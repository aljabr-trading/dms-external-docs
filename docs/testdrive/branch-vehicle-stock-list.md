---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<span class="http-get">GET</span> `/v1/testdrive/branch-vehicle-stock-list`

### Query Parameters

```
companyId: integer
brandId: integer
businessAreaId: integer
branchId: integer
bookingDate: string (Date must be between today and the next 10 days)
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **branchId:** `10`
    - **bookingDate:** `2026-06-18`

### Response

```json
{
  "shifts": [
    {
      "startTime": "08:00:00",
      "endTime": "21:00:00"
    }
  ],
  "nonWorkingDays": [],
  "modelFamilies": [
    {
      "modelFamilyId": 0,
      "familyText": "Carnival",
      "familyTextAr": "كارنڤال",
      "vehicles": [
        {
          "aptVehicleId": 211,
          "name": "KA4 CARNIVAL HEV",
          "nameAr": "KA4 CARNIVAL HEV",
          "modelFamilyId": 0,
          "familyText": "Carnival",
          "familyTextAr": "كارنڤال",
          "plateNoEn": "AVR 2700",
          "plateNoAr": "2700 ر ى ا",
          "vinCode": "KNANC81A9S6056275",
          "variantSummary": null,
          "variantSummaryAr": null,
          "slotCount": 26
        }
      ]
    },
    {
      "modelFamilyId": 0,
      "familyText": "EV9",
      "familyTextAr": "EV9",
      "vehicles": [
        {
          "aptVehicleId": 210,
          "name": "EV9",
          "nameAr": "ي وى 9",
          "modelFamilyId": 0,
          "familyText": "EV9",
          "familyTextAr": "EV9",
          "plateNoEn": "HER 3049",
          "plateNoAr": "3049 ر ع ه",
          "vinCode": "KNAAD8152R6008481",
          "variantSummary": null,
          "variantSummaryAr": null,
          "slotCount": 26
        }
      ]
    }
  ]
}
```
