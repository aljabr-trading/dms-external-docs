---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Communication Messages

<span class="http-get">GET</span> `/v1/core/communication-messages`

### Query Parameters

```
companyId: integer ( default :1) master -> masterlist -> listId=1
lang: string (default "en") "en" | "ar"
```

### Response

```json
[
  {
    "messageId": 8,
    "messageEn": "Complaint Follow-Up Fail",
    "isActive": true,
    "messageText": "Dear Customer,  \nWe couldn’t complete complaint ({complaintNumber}) due to no response within 3 days.  \nIt has been closed.  \nTo resume, please call us at ({contactNumber}).  \nYour satisfaction is our goal, Aljabr Trading Co.",
    "applicationId": 4,
    "applicationName": "Complaint",
    "companyId": 1,
    "messageTypeId": 2,
    "messageTypeName": "Manual",
    "communicationChannelId": 1,
    "communicationChannel": "SMS"
  },
  {
    "messageId": 9,
    "messageEn": "Duplicate Complaint",
    "isActive": true,
    "messageText": "Dear Customer,  \nComplaint ({complaintNumber}) has been closed as there is an active complaint ({activeComplaintNumber}) with the same details.  \nYour satisfaction is our goal, Aljabr Trading Co.",
    "applicationId": 4,
    "applicationName": "Complaint",
    "companyId": 1,
    "messageTypeId": 2,
    "messageTypeName": "Manual",
    "communicationChannelId": 1,
    "communicationChannel": "SMS"
  }
]
```
