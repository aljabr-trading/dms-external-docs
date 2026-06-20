---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<a><span class="http-post">POST</span></a> `/v1/testdrive/cancel`

---

Refer the comment <span class="flag-required"> //Mandatory</span> means the property is required

### 📌 API

sample data with reference of master list mapping

#### Request Mapping

```json
{
  "requestMasterId": 2729 // Mandatory
  "remarks": "string"     // Optional
}
```

#### Request Body <span class="flag-required"></span>

#### Response (200)

```json
{
  "success": true,
  "message": "testdrive-request-cancelled-successfully"
}
```

#### Response (404)

```json
{
  "success": false,
  "message": "testdrive-request-not-found-or-already-processed"
}
```
