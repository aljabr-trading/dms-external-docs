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
companyId: integer                      // Mandatory (default: 1)
brandId: integer                        // Mandatory (listId: 2) 
businessAreaId: integer                 // Mandatory (default: 2)
branchId: integer                       // (optional) (/v1/core/branchlist -> branchId)
isOpen: boolean                         // (optional) (empty:all,true:open,false:closed)
contactNo: string                       // (contact number: eg:5686017083,format:5XXXXXXXX)
requestNo: string                       // (any text)
customerIdentificationNo: string        // (any text)
pageNumber: integer                     // Mandatory (default:1)
pageSize: integer                       // Mandatory (default:10)
lang: string                            // Mandatory (default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `2`
    - **contactNo:** `5686`
    - **pageNumber:** `1`
    - **pageSize:** `10`

### Response

```json
[
  {
    "companyId": 1,
    "brandId": 1,
    "departmentId": 2,
    "branchId": 10,
    "branchName": "Dammam - Khobar Highway",
    "branchCode": "KIA1",
    "departmentName": "Sales",
    "requestedBranchName": "Dammam - Khobar Highway",
    "requestMasterId": 2733,
    "requestNo": "TD2733",
    "customerId": -1,
    "customerFirstName": "Test",
    "customerLastName": "string",
    "customerNumber": "568617000",
    "fullContactNumber": "00966568617000",
    "customerCompanyId": 1,
    "isAllocated": true,
    "isSlotAvailable": true,
    "slotTime": "08:00 AM - 08:20 AM",
    "statusId": 1,
    "statusName": "New",
    "allocations": [
      {
        "allocationId": 2823,
        "stockId": 21565,
        "familyName": "EV9",
        "modelYear": 2024,
        "allocationTypeId": 1,
        "allocationTypeName": "Slot",
        "vinCode": "KNAAD8152R6008481",
        "exteriorColor": "ICE GREEN",
        "interiorColor": "OSLO GRAY",
        "plateNoEn": "HER 3049",
        "startDate": "2026-06-18T08:00:00",
        "endDate": "2026-06-18T08:20:00"
      }
    ]
  },
  {
    "companyId": 1,
    "brandId": 1,
    "departmentId": 2,
    "branchId": 10,
    "branchName": "Dammam - Khobar Highway",
    "branchCode": "KIA1",
    "departmentName": "Sales",
    "requestedBranchName": "Dammam - Khobar Highway",
    "requestMasterId": 2732,
    "requestNo": "TD2732",
    "customerId": -1,
    "customerFirstName": "Param",
    "customerLastName": "Kalidas",
    "customerNumber": "568617083",
    "fullContactNumber": "568617083",
    "customerCompanyId": 1,
    "isAllocated": true,
    "isSlotAvailable": true,
    "slotTime": "08:30 PM - 08:50 PM",
    "statusId": 1,
    "statusName": "New",
    "allocations": [
      {
        "allocationId": 2822,
        "stockId": 132090,
        "familyName": "Tasman",
        "modelYear": 2026,
        "allocationTypeId": 1,
        "allocationTypeName": "Slot",
        "vinCode": "KNCSEY7B8T5005622",
        "exteriorColor": "TAN BEIGE",
        "interiorColor": "TERRACOTTA BROWN",
        "plateNoEn": "TGB 8210",
        "startDate": "2026-06-18T20:30:00",
        "endDate": "2026-06-18T20:50:00"
      }
    ]
  }
]
```
