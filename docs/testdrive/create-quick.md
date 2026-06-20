---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

<a><span class="http-post">POST</span></a> `/v1/testdrive/create/quick`

---

Refer the comment <span class="flag-required"> //Mandatory</span> means the property is required

### 📌 API

sample data with reference of master list mapping

#### Request Mapping

```json
{
  "companyId": 1,                       // default(1)
  "brandId": 0,                         // (listId:2)
  "branchId": 0,                        // (/v1/core/branchlist -> branchId)
  "businessAreaId": 2,                  // default(2)
  "sourceId": 1,                        // (direct)
  "subSourceId": 1,                     // (unified number)
  "bookType": 1,                        // (1-Morning,2-Evening)
  "bookingDate": "2026-06-19",
  "sendTestDriveConfirmation": true,
  "communicationType": 1,               // (1-Sms,3-WhatsApp)
  "remarks": "string",                  // (optional)
  "firstName": "",
  "lastName": "",
  "phoneCodeId": 1,                     // (default:1)
  "phoneNumber": 568617083,             // (format:5XXXXXXXX)
  "countryId": 56,                      // (listId-56)
  "regionId": 0,                        // optional (listId-100)
  "cityId": 0,                          // optional (listId-101)
  "email": "string",
  "modelFamilies": [
    {
      "modelFamilyId": 12               // (branch-vehicle-stock-list -> modelFamilyId)
    },
    {
      "modelFamilyId": 13               // (branch-vehicle-stock-list -> modelFamilyId)
    }
  ]
}
```

#### Request Body <span class="flag-required"></span>

#### Response

```json
{
  "success": true,
  "requestMasterId": 2730
}
```
