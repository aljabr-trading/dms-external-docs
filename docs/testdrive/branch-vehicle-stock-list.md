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
companyId: integer (default:1)// Mandatory
brandId: integer (listId:2)// Mandatory
businessAreaId: integer (default:2)// Mandatory
branchId: integer (optional) (/v1/core/branchlist -> branchId)// Mandatory
fromDate: string (yyyy-mm-dd, eg:2026-06-20, fromDate and toDate should be 7 days range)// Mandatory
toDate: string (yyyy-mm-dd, eg:2026-06-20)// Mandatory
lang: string (default: en)// Mandatory
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **branchId:** `10`
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
        },
        {
          "modelFamilyId": 24,
          "familyText": "EV9",
          "vehicles": [
            {
              "aptVehicleId": 210,
              "name": "EV9",
              "modelFamilyId": 24,
              "familyText": "EV9",
              "plateNoEn": "HER 3049",
              "vinCode": "KNAAD8152R6008481",
              "variantSummary": "EV9 ZH EX FWD Z 5 DR 7/S/ M1 (Earth)",
              "exteriorColor": "ICE GREEN",
              "interiorColor": "OSLO GRAY",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        },
        {
          "modelFamilyId": 27,
          "familyText": "K4",
          "vehicles": [
            {
              "aptVehicleId": 208,
              "name": "CL4M K4",
              "modelFamilyId": 27,
              "familyText": "K4",
              "plateNoEn": "UHR 7591",
              "vinCode": "3KPFT41A2SE070710",
              "variantSummary": "CL4M K4 1.6L LX FWD 6A/T 4 DR 5/S/ B1 ((16 INCH ALLOY ))",
              "exteriorColor": "SNOW WHITE PEARL",
              "interiorColor": "MEDIUM GRAY & ONYX BLACK",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        },
        {
          "modelFamilyId": 88,
          "familyText": "OVC",
          "vehicles": [
            {
              "aptVehicleId": 216,
              "name": "OVC",
              "modelFamilyId": 88,
              "familyText": "OVC",
              "plateNoEn": "TNR 7625",
              "vinCode": "LJD2BA1F2P0000957",
              "variantSummary": "OVC ZH LX 2WD Z 5 DR 5/S/ GLS ( (Air Long Range ))",
              "exteriorColor": "ICEBERG GREEN",
              "interiorColor": "HUMAN GRAY",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        },
        {
          "modelFamilyId": 8,
          "familyText": "Sportage",
          "vehicles": [
            {
              "aptVehicleId": 219,
              "name": "NQ5C SPORTAGE L",
              "modelFamilyId": 8,
              "familyText": "Sportage",
              "plateNoEn": "TNR 8208",
              "vinCode": "LJD7AA1D9S0220872",
              "variantSummary": "NQ5C SPORTAGE 1.5T T-GDI LX 2WD 8A/T 5 DR 5/S/ B1",
              "exteriorColor": "URBAN GRAY",
              "interiorColor": "SATURN BLACK",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        },
        {
          "modelFamilyId": 28,
          "familyText": "Tasman",
          "vehicles": [
            {
              "aptVehicleId": 214,
              "name": "TK TASMAN",
              "modelFamilyId": 28,
              "familyText": "Tasman",
              "plateNoEn": "TGB 8210",
              "vinCode": "KNCSEY7B8T5005622",
              "variantSummary": "TK TASMAN 2.5T T-GDI SX 4WD 8A/T 4 DR 5/S/ L3 (Canopy Double Decker PKG (GASOLINE - X-PRO+))",
              "exteriorColor": "TAN BEIGE",
              "interiorColor": "TERRACOTTA BROWN",
              "slotType": "Slot",
              "slotCount": 27
            },
            {
              "aptVehicleId": 212,
              "name": "TK TASMAN",
              "modelFamilyId": 28,
              "familyText": "Tasman",
              "plateNoEn": "TGB 8214",
              "vinCode": "KNCSCY7A6T5006555",
              "variantSummary": "TK TASMAN 2.2L EX 4WD 8A/T 4 DR 5/S/ L1 (Tonneau Cover PKG  (DIESEL- TOP ))",
              "exteriorColor": "SNOW WHITE PEARL",
              "interiorColor": "DARK BROWN ONE TONE",
              "slotType": "Slot",
              "slotCount": 27
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
        },
        {
          "modelFamilyId": 24,
          "familyText": "EV9",
          "vehicles": [
            {
              "aptVehicleId": 210,
              "name": "EV9",
              "modelFamilyId": 24,
              "familyText": "EV9",
              "plateNoEn": "HER 3049",
              "vinCode": "KNAAD8152R6008481",
              "variantSummary": "EV9 ZH EX FWD Z 5 DR 7/S/ M1 (Earth)",
              "exteriorColor": "ICE GREEN",
              "interiorColor": "OSLO GRAY",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        },
        {
          "modelFamilyId": 27,
          "familyText": "K4",
          "vehicles": [
            {
              "aptVehicleId": 208,
              "name": "CL4M K4",
              "modelFamilyId": 27,
              "familyText": "K4",
              "plateNoEn": "UHR 7591",
              "vinCode": "3KPFT41A2SE070710",
              "variantSummary": "CL4M K4 1.6L LX FWD 6A/T 4 DR 5/S/ B1 ((16 INCH ALLOY ))",
              "exteriorColor": "SNOW WHITE PEARL",
              "interiorColor": "MEDIUM GRAY & ONYX BLACK",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        },
        {
          "modelFamilyId": 88,
          "familyText": "OVC",
          "vehicles": [
            {
              "aptVehicleId": 216,
              "name": "OVC",
              "modelFamilyId": 88,
              "familyText": "OVC",
              "plateNoEn": "TNR 7625",
              "vinCode": "LJD2BA1F2P0000957",
              "variantSummary": "OVC ZH LX 2WD Z 5 DR 5/S/ GLS ( (Air Long Range ))",
              "exteriorColor": "ICEBERG GREEN",
              "interiorColor": "HUMAN GRAY",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        },
        {
          "modelFamilyId": 8,
          "familyText": "Sportage",
          "vehicles": [
            {
              "aptVehicleId": 219,
              "name": "NQ5C SPORTAGE L",
              "modelFamilyId": 8,
              "familyText": "Sportage",
              "plateNoEn": "TNR 8208",
              "vinCode": "LJD7AA1D9S0220872",
              "variantSummary": "NQ5C SPORTAGE 1.5T T-GDI LX 2WD 8A/T 5 DR 5/S/ B1",
              "exteriorColor": "URBAN GRAY",
              "interiorColor": "SATURN BLACK",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        },
        {
          "modelFamilyId": 28,
          "familyText": "Tasman",
          "vehicles": [
            {
              "aptVehicleId": 214,
              "name": "TK TASMAN",
              "modelFamilyId": 28,
              "familyText": "Tasman",
              "plateNoEn": "TGB 8210",
              "vinCode": "KNCSEY7B8T5005622",
              "variantSummary": "TK TASMAN 2.5T T-GDI SX 4WD 8A/T 4 DR 5/S/ L3 (Canopy Double Decker PKG (GASOLINE - X-PRO+))",
              "exteriorColor": "TAN BEIGE",
              "interiorColor": "TERRACOTTA BROWN",
              "slotType": "Slot",
              "slotCount": 27
            },
            {
              "aptVehicleId": 212,
              "name": "TK TASMAN",
              "modelFamilyId": 28,
              "familyText": "Tasman",
              "plateNoEn": "TGB 8214",
              "vinCode": "KNCSCY7A6T5006555",
              "variantSummary": "TK TASMAN 2.2L EX 4WD 8A/T 4 DR 5/S/ L1 (Tonneau Cover PKG  (DIESEL- TOP ))",
              "exteriorColor": "SNOW WHITE PEARL",
              "interiorColor": "DARK BROWN ONE TONE",
              "slotType": "Slot",
              "slotCount": 27
            }
          ]
        }
      ]
    }
  ]
}
```
