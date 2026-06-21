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
   "companyId": 1,                    // Mandatory (default: 1) 
   "brandId": 1,                      // Mandatory (listId: 2) 
   "businessAreaId": 2,               // Mandatory (default: 2) 
   "branchId": 10,                    // Mandatory (/v1/core/branchlist -> branchId) 
   "aptVehicleId": 212,               // Mandatory (branch-vehicle-slot-list -> aptVehicleId) 
   "bookingDate": "2026-06-21",       // Mandatory (yyyy-mm-dd, eg: 2026-06-21) 
   "slotMasterId": 31,                // Mandatory (branch-vehicle-slot-list -> slotMasterId) 
   "sourceId": 1,                     // Mandatory (default: 1) -> direct
   "subSourceId": 1,                  // Mandatory (default: 1) -> unified number
   "firstName": "Kirubaharan",        // Mandatory
   "lastName": "Palani",              // Mandatory 
   "sendTestDriveConfirmation": true, // Mandatory
   "communicationType": 0,            // Mandatory (1->sms, 3->whatsapp)
   "remarks": "",                     // Optional
   "phoneCodeId": 1,                  // Mandatory (default:1) 
   "phoneNumber": 551883151,          // Mandatory (eg:5XXXXXXXX) 
   "countryId": 56,                   // Mandatory (listId: 56) 
   "regionId": 0,                     // Optional (listId: 100)
   "cityId": 0,                       // Optional (listId: 101)
   "email": "test@gmail.com"          // Optional (default: empty)
}
```

#### Request Body (Using Period)

```json
{
   "companyId": 1,                    // Mandatory (default: 1) 
   "brandId": 1,                      // Mandatory (listId: 2) 
   "businessAreaId": 2,               // Mandatory (default: 2) 
   "branchId": 10,                    // Mandatory (/v1/core/branchlist -> branchId) 
   "aptVehicleId": 212,               // Mandatory (branch-vehicle-slot-list- aptVehicleId) 
   "bookingDate": "2026-06-21",       // Mandatory (yyyy-mm-dd,eg:2026-06-20) 
   "sourceId": 1,                     // Mandatory (default: 1) -> direct
   "subSourceId": 1,                  // Mandatory (default: 1) -> unified number
   "starttime": “09:00:00”,           // (HH:mm:ss, 24 hour format) // Mandatory
   "firstName": "Kirubaharan",        // Mandatory
   "lastName": "Palani",              // Mandatory 
   "sendTestDriveConfirmation": true, // Mandatory
   "communicationType": 0,            // Mandatory (1->sms, 3->whatsapp)
   "remarks": "",                     // Optional
   "phoneCodeId": 1,                  // Mandatory (default:1) 
   "phoneNumber": 551883151,          // Mandatory (eg:5XXXXXXXX) 
   "countryId": 56,                   // Mandatory (listId: 56) 
   "regionId": 0,                     // Optional (listId: 100)
   "cityId": 0,                       // Optional (listId: 101)
   "email": "test@gmail.com"          // Optional (default: empty)
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
