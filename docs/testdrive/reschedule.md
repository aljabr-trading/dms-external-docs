---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<a><span class="http-post">POST</span></a> `/v1/testdrive/reschedule`

---

Refer the comment <span class="flag-required"> //Mandatory</span> means the property is required

### 📌 API

sample data with reference of master list mapping

#### Request Body (Using Slot Type)

```json
{
  "requestMasterId": 2729,                  // Mandatory
  "aptVehicleId": 211,                      // Mandatory
  "slotMasterId": 19,                       // Mandatory
  "reBookingDate": "2026-06-19"             // Mandatory
}
```

#### Request Body (Using Period)

```json
{
  "requestMasterId": 2729,                  // Mandatory
  "aptVehicleId": 211,                      // Mandatory
  "reBookingDate": "2026-06-19",            // Mandatory
  "startTime": "15:30:30"                   // Mandatory (HH:mm:ss)
}
```

#### Response

```json
{
  "success": true,
  "message": "testdrive-request-rescheduled-successfully",
  "requestMasterId": 2731
}
```
