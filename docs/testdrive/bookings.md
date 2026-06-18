---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<span class="http-get">GET</span> `/v1/testdrive/bookings`

### Query Parameters

```
companyId: integer
brandId: integer
businessAreaId: integer
branchId: integer (optional)
isOpen: boolean (optional)
searchText: string
pageNumber: integer
pageSize: integer
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **searchText:** `5686`
    - **pageNumber:** `1`
    - **pageSize:** `10`

### Response

```json
[
  {
    "requestMasterId": 2725,
    "requestText": "TD2725",
    "customerId": -1,
    "customerFirstName": "Param",
    "customerLastName": "Kalidas",
    "customerNumber": "568617083",
    "contactName": null,
    "fullContactNumber": "568617083",
    "companyId": 1,
    "brandId": 1,
    "departmentId": 2,
    "branchId": 10,
    "branchName": null,
    "branchCode": "KIA1",
    "departmentName": "Sales",
    "departmentNameAr": "مبيعات",
    "requestedBranchName": null,
    "requestedBranchNameAr": null,
    "isAllocated": true,
    "isSlotAvailable": true,
    "slotTime": "09:00 AM - 09:20 AM",
    "createdDate": null,
    "assignDate": null,
    "closeDate": null,
    "statusId": 1,
    "statusName": "New",
    "statusNameAr": "جديد",
    "allocations": [
      {
        "allocationId": 2817,
        "stockId": 21565,
        "vinCode": "KNAAD8152R6008481",
        "familyName": "EV9",
        "familyNameAr": "EV9",
        "allocationTypeName": "Slot",
        "allocationTypeNameAr": "موعد",
        "modelYear": 2024,
        "exteriorColor": "ICE GREEN",
        "interiorColor": "OSLO GRAY",
        "plateNoEn": "HER 3049",
        "plateNoAr": "3049 ر ع ه",
        "allocationTypeId": 1,
        "startDate": "2026-06-22T09:00:00",
        "endDate": "2026-06-22T09:20:00"
      }
    ]
  },
  {
    "requestMasterId": 2690,
    "requestText": "TD2690",
    "customerId": 5896,
    "customerFirstName": "Eman",
    "customerLastName": "Abdullah Mohamed Al Salem",
    "customerNumber": "568699441",
    "contactName": null,
    "fullContactNumber": "00966568699441",
    "companyId": 1,
    "brandId": 1,
    "departmentId": 2,
    "branchId": 10,
    "branchName": null,
    "branchCode": "KIA1",
    "departmentName": "Sales",
    "departmentNameAr": "مبيعات",
    "requestedBranchName": null,
    "requestedBranchNameAr": null,
    "isAllocated": true,
    "isSlotAvailable": true,
    "slotTime": "02:30 PM - 02:50 PM",
    "createdDate": null,
    "assignDate": "2026-06-09T16:38:55.967",
    "closeDate": null,
    "statusId": 3,
    "statusName": "In Progress",
    "statusNameAr": "جاري العمل",
    "allocations": [
      {
        "allocationId": 2785,
        "stockId": 21565,
        "vinCode": "KNAAD8152R6008481",
        "familyName": "EV9",
        "familyNameAr": "EV9",
        "allocationTypeName": "Slot",
        "allocationTypeNameAr": "موعد",
        "modelYear": 2024,
        "exteriorColor": "ICE GREEN",
        "interiorColor": "OSLO GRAY",
        "plateNoEn": "HER 3049",
        "plateNoAr": "3049 ر ع ه",
        "allocationTypeId": 1,
        "startDate": "2026-06-11T14:30:00",
        "endDate": "2026-06-11T14:50:00"
      }
    ]
  }
]
```
