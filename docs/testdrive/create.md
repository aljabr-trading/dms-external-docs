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

```json
{
  "companyId": 1,                               // Mandatory
  "brandId": 1,                                 // Mandatory
  "businessAreaId": 2,                          // Mandatory
  "branchId": 10,                               // Mandatory
  "aptVehicleId": 211,                          // Mandatory
  "bookingDate": "2026-06-18T07:45:31.784Z",    // Mandatory
  "slotMasterId": 19,                           // Mandatory
  "firstName": "string",                        // Mandatory
  "lastName": "string",                         // Mandatory
  "sourceId": 0,
  "subSourceId": 0,
  "sendTestDriveConfirmation": true,
  "communicationType": 0,
  "remarks": "string",
  "phoneCodeId": 0,
  "phoneNumber": 0,
  "countryId": 0,
  "regionId": 0,
  "cityId": 0,
  "email": "string"
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
