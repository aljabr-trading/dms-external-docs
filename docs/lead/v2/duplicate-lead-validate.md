---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Validate duplicate lead
### Checks whether a lead already exists for the supplied company, brand, department, phone code, and phone number.

<span class="http-get">GET</span> `/v2/leads/duplicate-lead-validate`

### Query Parameters (all fields are mandatory)

```
companyId: integer
ouId: integer
departmentId: integer
phoneCodeId: integer
phoneNo: string
``` 

This will provide the 

### Response (200)

```json
{
  "message": "no--duplicate-lead-found",
  "status": "Success"
}
```

## Response (400)
```json
{
    "status": 400,
    "errorCode": "DMS-Error-001",
    "operationError": "{\"message\":\"Lead {{leadRefNo}} - already has phone no {{phoneNumber}}\",\"field\":\"phoneNumber\",\"data\":{\"leadRefNo\":\"183686\",\"phoneNumber\":\"500000000\"}}",
    "error": "invalid-operation",
    "timeStamp": "2026-07-14T12:24:33.4575626+03:00"
}
```