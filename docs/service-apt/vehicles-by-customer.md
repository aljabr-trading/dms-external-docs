---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get vehicles by customer
### Returns localized vehicles filtered by mobile number, customer id and/or prospect id for the requested brand and language. Use customerId for registered customers and prospectId for prospects; the two id spaces are separate. Rows sourced from a vehicle prospect are flagged with isProspectVehicle and carry prospectVehicleId.

<span class="http-get">GET</span> `/v1/core/vehicles-by-customer`

### Query Parameters

```
mobileNo: string                        // Optional
customerId: string                      // Optional (registered customer)
prospectId: string                      // Optional (prospect; separate id space from customerId)
brandId: integer                        // Optional
lang: string                            // Optional (default: en) "en" | "ar"
```

!!! note

    **Example:**

    - **mobileNo:** `555123456`
    - **customerId:** `4001`
    - **brandId:** `1`
    - **lang:** `en`

### Response

```json
{
  "items": [
    {
      "customerId": 4001,
      "customerVehicleId": 5001,
      "mobileNumber": "555123456",
      "firstName": "Ahmed",
      "lastName": "Ali",
      "contactName": "Ahmed Ali",
      "stockId": 8001,
      "stockNo": 10001,
      "vinCode": "KNAAE12345A123456",
      "plateNo": "ABC 1234",
      "modelYear": 2026,
      "soldDate": "2026-01-10T00:00:00",
      "dateOfPurchase": "2026-01-10T00:00:00",
      "brandId": 1,
      "brandName": "KIA",
      "modelFamilyId": 1001,
      "familyCode": "SPORTAGE",
      "familyName": "Sportage",
      "modelId": 2001,
      "modelCode": "SPG-1.6",
      "modelName": "Sportage 1.6",
      "modelVariantId": 3001,
      "variantCode": "LX",
      "trimCode": "LX",
      "interiorColor": "Black",
      "exteriorColor": "White",
      "relationTypeText": "Owner",
      "prospectVehicleId": null,
      "prospectId": null,
      "isProspectVehicle": false
    }
  ]
}
```

### Response (400)

```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "dms-invalid-data",
  "error": "invalid-operation",
  "timeStampe": "2026-06-20T15:00:00"
}
```
