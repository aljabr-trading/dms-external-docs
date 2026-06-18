---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<a><span class="http-put">PUT</span></a> `/v1/testdrive/reschedule`

---

Refer the comment <span class="flag-required"> //Mandatory</span> means the property is required

### 📌 API

sample data with reference of master list mapping

#### Request Mapping

```json
{
  "requestMasterId": 2729,                          // Mandatory
  "aptVehicleId": 211,                              // Mandatory
  "slotMasterId": 19,                               // Mandatory
  "reBookingDate": "2026-06-19T10:08:08.660Z"       // Mandatory
}
```

#### Request Body <span class="flag-required"></span>

#### Response

```json
{
  "success": true,
  "message": "testdrive-request-rescheduled-successfully",
  "requestMasterId": 2731
}
```
