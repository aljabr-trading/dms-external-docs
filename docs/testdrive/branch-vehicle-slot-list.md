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
companyId: integer
brandId: integer
businessAreaId: integer
branchId: integer
vehicleId: integer
bookingDate: string (Date must be between today and the next 10 days)
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **branchId:** `10`
    - **vehicleId:** `211`
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
      "modelFamilyId": 12,
      "familyText": null,
      "familyTextAr": "كارنڤال",
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
            {
              "startTime": "09:00:00",
              "endTime": "09:20:00",
              "slotMasterId": 21
            },
            {
              "startTime": "09:30:00",
              "endTime": "09:50:00",
              "slotMasterId": 22
            },
            {
              "startTime": "10:00:00",
              "endTime": "10:20:00",
              "slotMasterId": 23
            },
            {
              "startTime": "10:30:00",
              "endTime": "10:50:00",
              "slotMasterId": 24
            },
            {
              "startTime": "11:00:00",
              "endTime": "11:20:00",
              "slotMasterId": 25
            },
            {
              "startTime": "11:30:00",
              "endTime": "11:50:00",
              "slotMasterId": 26
            },
            {
              "startTime": "12:00:00",
              "endTime": "12:20:00",
              "slotMasterId": 27
            },
            {
              "startTime": "12:30:00",
              "endTime": "12:50:00",
              "slotMasterId": 28
            },
            {
              "startTime": "13:00:00",
              "endTime": "13:20:00",
              "slotMasterId": 29
            },
            {
              "startTime": "13:30:00",
              "endTime": "13:50:00",
              "slotMasterId": 30
            },
            {
              "startTime": "14:00:00",
              "endTime": "14:20:00",
              "slotMasterId": 31
            },
            {
              "startTime": "14:30:00",
              "endTime": "14:50:00",
              "slotMasterId": 32
            },
            {
              "startTime": "15:00:00",
              "endTime": "15:20:00",
              "slotMasterId": 33
            },
            {
              "startTime": "15:30:00",
              "endTime": "15:50:00",
              "slotMasterId": 34
            },
            {
              "startTime": "16:00:00",
              "endTime": "16:20:00",
              "slotMasterId": 35
            },
            {
              "startTime": "16:30:00",
              "endTime": "16:50:00",
              "slotMasterId": 36
            },
            {
              "startTime": "17:00:00",
              "endTime": "17:20:00",
              "slotMasterId": 37
            },
            {
              "startTime": "17:30:00",
              "endTime": "17:50:00",
              "slotMasterId": 38
            },
            {
              "startTime": "18:00:00",
              "endTime": "18:20:00",
              "slotMasterId": 39
            },
            {
              "startTime": "18:30:00",
              "endTime": "18:50:00",
              "slotMasterId": 40
            },
            {
              "startTime": "19:00:00",
              "endTime": "19:20:00",
              "slotMasterId": 41
            },
            {
              "startTime": "19:30:00",
              "endTime": "19:50:00",
              "slotMasterId": 42
            },
            {
              "startTime": "20:00:00",
              "endTime": "20:20:00",
              "slotMasterId": 43
            },
            {
              "startTime": "20:30:00",
              "endTime": "20:50:00",
              "slotMasterId": 44
            }
          ],
          "aptVehicleId": 211,
          "name": "KA4 CARNIVAL HEV",
          "nameAr": "KA4 CARNIVAL HEV",
          "modelFamilyId": 12,
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
    }
  ]
}
```
