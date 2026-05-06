---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```
<a><span class="http-get">GET</span></a> `/v1/campaign/details`

### Query Parameters

```
Lang: string
Company: string
Brand: string
Department: string (optional)
Active: boolean (optional)
``` 
!!! note

    **`Lang`, `Company` and `Brand` are mandatory fields.**

    **Example:**

    - **Lang:** **ar**
    - **Company:** **jtc**
    - **Brand:** **kia**
    - **Department:** **service**
    - **Active:** **true**
#### Response   
```json
[
    {
        "campaign": {
            "campaignId": 9,
            "campaignCode": "KIASERVICE",
            "campaignName": "اعلان كيا صيانة ",
            "typeId": 2,
            "typeName": "اعلان",
            "statusId": 4,
            "statusName": "موافق",
            "priorityId": 3,
            "priorityName": "عالي",
            "companyId": 1,
            "brandId": 1,
            "departmentId": 3,
            "brandName": "كيا",
            "departmentName": "صيانة",
            "languageId": 3,
            "languageName": "عربي وانجليزي",
            "targetAudienceId": 3,
            "audienceName": "جميع العملاء",
            "totalTargetAudience": 1500,
            "startDate": "2026-05-01T00:00:00",
            "endDate": "2026-06-30T00:00:00",
            "description": "وصف اعلان كيا صيانة ",
            "keyOffer": "صيانة, عروض",
            "condition": "الشروط بالتفصيل",
            "termsAndConditions": "الشروط والاحكام \n1-\n2-",
            "promoCode": "KIASER",
            "landingPage": " Landing Page Test",
            "otherLinks": "Other Links Test"
        },
        "targets": [
            {
                "campaignTargetId": 4,
                "campaignId": 9,
                "regionId": 1,
                "regionName": "الشرقية",
                "cityId": null,
                "cityName": "الدمام",
                "branchId": null,
                "branchName": null
            }
        ],
        "channels": [
            {
                "campaignTChannelId": 7,
                "campaignId": 9,
                "channelId": 1,
                "channelName": "رسائل نصية"
            }
        ],
        "paymentTypes": [
            {
                "campaignPaymentTypeId": 6,
                "campaignId": 9,
                "paymentTypeId": 1,
                "paymentTypeName": "نقدا"
            }
        ],
        "targetVehicles": [
            {
                "campaignTargetVehicleId": 13,
                "campaignId": 9,
                "modelFamilyId": 11,
                "modelId": 9,
                "modelVariantId": null,
                "modelYear": null,
                "familyName": "كارينز",
                "modelName": "ار بي كارنز ",
                "modelVariantName": null
            }
        ]
    }
]
``` 
 