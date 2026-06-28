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
   "companyId": 1,                        // Mandatory (default: 1) 
   "brandId": 1,                          // Mandatory (listId: 2) 
   "businessAreaId": 2,                   // Mandatory (default: 2) 
   "branchId": 10,                        // Mandatory (/v1/core/branchlist -> branchId) 
   "aptVehicleId": 212,                   // Mandatory (branch-vehicle-slot-list -> aptVehicleId) 
   "bookingDate": "2026-06-21",           // Mandatory (yyyy-mm-dd, eg: 2026-06-21) 
   "slotMasterId": 31,                    // Mandatory (branch-vehicle-slot-list -> slotMasterId) 
   "sourceId": 1,                         // Mandatory (default: 1) -> direct
   "subSourceId": 1,                      // Mandatory (default: 1) -> unified number
   "firstName": "Kirubaharan",            // Mandatory
   "lastName": "Palani",                  // Mandatory 
   "remarks": "",                         // Optional
   "phoneCodeId": 1,                      // Mandatory (default:1) 
   "phoneNumber": 551883151,              // Mandatory (eg:5XXXXXXXX) 
   "countryId": 56,                       // Mandatory (listId: 56) 
   "regionId": 0,                         // Optional (listId: 100)
   "cityId": 0,                           // Optional (listId: 101)
   "email": "test@gmail.com",             // Optional (default: empty)
   "lang":"en"                            // Mandatory
   "sendCommunicationConfirmation": true, // Mandatory
  "communicationType": 1,                 // Mandatory (1->sms, 3->whatsapp)
   "remarks": "string" 
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
   "remarks": "",                     // Optional
   "phoneCodeId": 1,                  // Mandatory (default:1) 
   "phoneNumber": 551883151,          // Mandatory (eg:5XXXXXXXX) 
   "countryId": 56,                   // Mandatory (listId: 56) 
   "regionId": 0,                     // Optional (listId: 100)
   "cityId": 0,                       // Optional (listId: 101)
   "email": "test@gmail.com",         // Optional (default: empty)
   "sendCommunicationConfirmation": true, // Mandatory
   "communicationType": 0,            // Mandatory (1->sms, 3->whatsapp)
   "lang":"en"                        // Mandatory
}
```

#### Request Body <span class="flag-required"></span>

#### Response

```json
{
  "success": true,
  "requestMasterId": 2729,
  "requestNo": "TD2772",
  "communication": "SMS",
  "communicatioSent": true,
  "communicatioMessage": "Dear Customer,\nYour test drive (TD2772) for Carnival has been confirmed on 24-06-2026 at 04:30 PM - 04:50 PM.\n\nBranch: Dammam - Khobar Highway\nCall Center: 920014200\nLocation: https://maps.app.goo.gl/cdJ6reAkeERUKh7w6\n\nThank you for choosing KIA.",
  "communicationId": 179331
}
```
