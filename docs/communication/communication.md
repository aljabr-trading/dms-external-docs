---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## send communication
<span class="http-get">GET</span> `/v1/communications/sendcommunication`

Action Type 
 Options -> Lead_Welcome,Location_Inquiry,TestDrive_Allocation_Slot,TestDrive_Cancel_Allocation,TestDrive_Allocation,Marketing_Campaign
 

#### Request Body 
```json
{
  "companyId": 1,                           // Mandatory
  "BrandId": 1,                             // Mandatory
  "channelTypeId": 1,                       // Mandatory
  "actionType": "Location_Inquiry",         // Mandatory
  "ReferenceNo": "18",                      // Mandatory User Selection based on action type
  "mobileNo": "568617083",                  // Mandatory
  "lang": "ar"                              // Mandatory
}
```
### Response
```json
 
{
    "communicationId": 179332,
    "message": "Dear Customer,\nHere are the branch details\nBranch Name: Hassa - Al Mubarraz\nAddress: Dhahran Rd, Al Rajhi, Al Mubarraz\nGoogle Maps: https://goo.gl/maps/4s2ExQVwrLZa6fu3A\nWe look forward to assisting you, Aljabr Trading Company!"
}
```


#### Request Body 
```json
{
  "companyId": 1,                           // Mandatory
  "BrandId": 1,                             // Mandatory
  "channelTypeId": 1,                       // Mandatory
  "actionType": "Location_Inquiry",         // Mandatory
  "ReferenceNo": "18",                      // Mandatory User Selection based on action type
  "mobileNo": "568617083",                  // Mandatory
  "lang": "ar"                              // Mandatory
}
```
### Response

```json
{
    "communicationId": 179335,
    "message": "عزيزنا العميل،\nفيما يلي تفاصيل الفرع:\nاسم الفرع: الاحساء - المبرز\nالعنوان: طريق الظهران، المبرز\nموقع الفرع : https://goo.gl/maps/4s2ExQVwrLZa6fu3A\nنتطلع إلى خدمتك، شركة الجبر التجارية!"
}
```