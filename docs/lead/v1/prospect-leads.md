---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Get Prospect Leads
### Returns prospect leads filtered by company, brand, business area, status, contact number, request number, or customer identification number.

<a><span class="http-get">GET</span></a> `/v1/leads/prospect-leads`

### Query Parameters

```
companyId: integer                      // Mandatory (default: 1)
brandId: integer                        // Mandatory (listId: 2) 
businessAreaId: integer                 // Mandatory (default: 2)
isOpen: boolean                         // (optional) (empty:all, true:open, false:closed)
contactNo: string                       // (contact number: eg:5686017083,format:5XXXXXXXX)
leadId: long                            // (DMS Lead Id number)
customerIdentificationNo: string        // (any text)
lang: string                            // optional (default: en) "en" | "ar"
``` 

!!!Note 
    Either `contactNo` or `leadId` or `customerIdentificationNo`is mandatory.

#### Response
```json
{
    "leads": [
        {
            "leadId": 103739,
            "customerIdentificationTypeNo": "",
            "isError": 0,
            "vehicleLists": [
                {
                    "leadVehiclesId": 104318,
                    "modelFamily": "بيجاس",
                    "modelYear": 2026,
                    "totalQty": 1
                }
            ],
            "leadType": "أفراد",
            "firstName": "Kirubaharan Palani",
            "contactName": "",
            "companyName": "أفراد",
            "customerCountry": "المملكة العربية السعودية",
            "customerRegion": "المنطقة الشرقية",
            "customerCity": "الدمام",
            "phoneCode": "00966",
            "phoneNumber": "551883151",
            "email": "pkiruba85@gmail.com",
            "monthlyIncome": "من 5000-10000 ريال",
            "preferredLanguage": "الإنجليزية",
            "preferredContactType": "مكالمة صوتية",
            "company": "شركة الجبر التجارية",
            "brand": "كيا",
            "businessArea": "مبيعات",
            "leadDate": "2026-02-02T00:00:00",
            "interest": "طلب عرض سعر",
            "source": "طرف ثالث",
            "subSource": "موتوري",
            "leadName": "Motory Leads",
            "leadReference": "46850",
            "vehicleType": "جديد",
            "purchasePlan": "أكثر من 60 يوم",
            "paymentMode": "تمويل",
            "currency": "ريال سعودي",
            "priority": "بارد",
            "testDriveRequired": false,
            "acceptNewsLetter": false,
            "acceptMarketing": false,
            "acceptPrivatePolicy": false,
            "lang": "ar",
            "sendCommunicationConfirmation": false,
            "communicationType": 1
        }
    ]
}
``` 
