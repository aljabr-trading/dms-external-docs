---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Send location inquiry SMS
### Sends a location inquiry SMS using the configured Location_Inquiry communication template.

<span class="http-get">GET</span> `/v1/communications/location-inquiry`

#### Request Body 
```json
{
  "companyId": 1,                           // Mandatory
  "brandId": 1,                             // Mandatory
  "companyHierarchyId": 1,                  // Mandatory
  "mobileNo": "568617083",                  // Mandatory
  "lang": "ar"                              // optional (default "en")
}
```

### Response (200)
```json
{
  "communicationId": 70001,
  "message": "Your request has been received."
}
```

### Response (400) 
```json
{
  "applicationId": null,
  "status": 400,
  "errorCode": "DMS-Error-001",
  "operationError": "sms-send-failed",
  "error": "invalid-operation",
  "timeStamp": "2026-06-20T15:00:00"
}
```
