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
  "companyId": 1,                       // Mandatory (default: 1)
  "brandId": 0,                         // Mandatory (listId: 2)
  "branchId": 0,                        // Mandatory (/v1/core/branchlist -> branchId)
  "businessAreaId": 2,                  // Mandatory (default: 2)
  "sourceId": 1,                        // Mandatory (default: 1) -> direct
  "subSourceId": 1,                     // Mandatory (default: 1) -> unified number
  "bookType": 1,                        // (1-Morning, 2-Evening)
  "bookingDate": "2026-06-19",          // Mandatory
  "sendTestDriveConfirmation": true,    // Mandatory
  "communicationType": 1,               // Mandatory (1-Sms, 3-WhatsApp) 
  "remarks": "string",                  // (optional)
  "firstName": "",                      // Mandatory
  "lastName": "",                       // Mandatory
  "phoneCodeId": 1,                     // Mandatory (default: 1) 
  "phoneNumber": 568617083,             // Mandatory (format: 5XXXXXXXX) 
  "countryId": 56,                      // (listId: 56)
  "regionId": 0,                        // optional (listId: 100)
  "cityId": 0,                          // optional (listId: 101)
  "email": "string",
  "sendTestDriveConfirmation": true,    // Mandatory
  "communicationType": 1,               // Mandatory Mandatory (1->sms, 3->whatsapp)
  "lang":"en",                          // Mandatory
                                        // Mandatory
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
  "requestMasterId": 2730 ,
  "requestNo": "TD2770",
  "communication": "SMS",
  "communicatioSent": true,
  "communicatioMessage": "Dear Customer,\nYour test drive (TD2770) for  has been submitted, our representative will call you for confirming the appointment.\n \nFor assistance, contact:\nCall Center: 920014200\n\nBranch: Dammam - Khobar Highway\nLocation: https://maps.app.goo.gl/cdJ6reAkeERUKh7w6\n\nThank you for choosing KIA.",
  "communicationId": 179329
}
```
