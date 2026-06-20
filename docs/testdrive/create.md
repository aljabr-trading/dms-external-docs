---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<a><span class="http-post">POST</span></a> `/v1/testdrive/create`

---

Refer the comment <span class="flag-required"> //Mandatory</span> means the property is required

### 📌 API

sample data with reference of master list mapping

#### Request Mapping

#### Request Body (Using Slot Type)

```json
{
   "companyId": 1,                    // (default: 1) // Mandatory
   "brandId": 1,                      // (listId: 2) // Mandatory
   "businessAreaId": 2,               // (default: 2) // Mandatory
   "branchId": 10,                    // (/v1/core/branchlist -> branchId) // Mandatory
   "aptVehicleId": 212,               // (branch-vehicle-slot-list -> aptVehicleId) // Mandatory
   "bookingDate": "2026-06-21",       // string (yyyy-mm-dd, eg: 2026-06-21) // Mandatory
   "slotMasterId": 31,                // (branch-vehicle-slot-list -> slotMasterId) // Mandatory
   "sourceId": 1,                     // (direct) // Mandatory
   "subSourceId": 1,                  // (unified number) // Mandatory
   "firstName": "Kirubaharan",        // Mandatory
   "lastName": "Palani",              // Mandatory 
   "sendTestDriveConfirmation": true, // Mandatory
   "communicationType": 0,            // (1->sms, 3->whatsapp) // Mandatory
   "remarks": "",
   "phoneCodeId": 1,                  // (default:1) // Mandatory
   "phoneNumber": 551883151,          // (eg:5XXXXXXXX) // Mandatory
   "countryId": 56,                   // (listId: 56) // Mandatory
   "regionId": 0,                     // optional (listId: 100)
   "cityId": 0,                       // optional (listId: 101)
   "email": "pkiruba85@gmail.com"     // optional (default: empty)
}
```

#### Request Body (Using Period)

```json
{
   "companyId": 1,                    // (default: 1) // Mandatory
   "brandId": 1,                      // (listId: 2) // Mandatory
   "businessAreaId": 2,               // (default: 2) // Mandatory
   "branchId": 10,                    // (/v1/core/branchlist -> branchId) // Mandatory
   "aptVehicleId": 212,               // (branch-vehicle-slot-list- aptVehicleId) // Mandatory
   "bookingDate": "2026-06-21",       // string(yyyy-mm-dd,eg:2026-06-20) // Mandatory
   "sourceId": 1,                     // (direct) // Mandatory
   "subSourceId": 1,                  // (unified number) // Mandatory
    "starttime": “09:00:00”,          // (HH:mm:ss, 24 hour format) // Mandatory
   "firstName": "Kirubaharan",
   "lastName": "Palani",
   "sendTestDriveConfirmation": true, // Mandatory
   "communicationType": 0,            // (1->sms,3->whatsapp) // Mandatory
   "remarks": "",
   "phoneCodeId": 1,                  // (default:1) // Mandatory
   "phoneNumber": 551883151,          // (eg:5XXXXXXXX) // Mandatory
   "countryId": 56,                   // (listId-56) // Mandatory
   "regionId": 0,                     // optional (listId-100)
   "cityId": 0,                       // optional (listId-101)
   "email": "pkiruba85@gmail.com"     // optional (default:empty)
}
```

#### Request Body <span class="flag-required"></span>

#### Response

```json
{
  "success": true,
  "requestMasterId": 2729
}
```
