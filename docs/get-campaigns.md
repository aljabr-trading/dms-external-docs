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
CompanyCode: string
BrandCode: string
DepartmentCode: string (optional)
Active: boolean (optional)
``` 
!!! note
    **Both `CompanyCode` and `BrandCode` are mandatory fields.**

    **Example:**

    - **CompanyCode:** **jtc**
    - **BrandCode:** **kia**
    - **DepartmentCode:** **service**
    - **Active:** **true**

#### Response   
```json
[
    {
        "campaign": {
            "campaignId": 9,
            "typeName": "Promotion",
            "typeNameAr": "اعلان",
            "priorityName": "High",
            "brandText": "KIA",
            "brandTextAr": "كيا",
            "departmentName": "Service",
            "departmentNameAr": "صيانة",
            "priorityNameAr": "عالي",
            "statusName": "Approved",
            "statusNameAr": "موافق",
            "languageName": "All",
            "languageNameAr": "عربي وانجليزي",
            "audienceName": "All Customers",
            "audienceNameAr": "جميع العملاء",
            "campaignName": "KIA Service Campaign",
            "campaignNameAr": "اعلان كيا صيانة ",
            "campaignCode": "KIASERVICE",
            "typeId": 2,
            "statusId": 4,
            "startDate": "2026-05-01T00:00:00",
            "endDate": "2026-06-30T00:00:00",
            "priorityId": 3,
            "languageId": 3,
            "companyId": 1,
            "targetAudienceId": 3,
            "totalTargetAudience": 1500,
            "description": "KIA Service Campaign Description",
            "descriptionAr": "وصف اعلان كيا صيانة ",
            "keyOffer": "offers,serivce",
            "keyOfferAr": "صيانة, عروض",
            "condition": "Condtions in detail",
            "conditionAr": "الشروط بالتفصيل",
            "termsAndConditions": "Terms And Condtions:\n1-\n2-",
            "termsAndConditionsAr": "الشروط والاحكام \n1-\n2-",
            "promoCode": "KIASER",
            "landingPage": " Landing Page Test",
            "otherLinks": "Other Links Test"
        },
        "targets": [
            {
                "campaignTargetId": 4,
                "regionText": "Eastern",
                "regionTextAr": "الشرقية",
                "cityText": "Dammam",
                "cityTextAr": "الدمام",
                "branchText": null,
                "branchTextAr": null,
                "campaignId": 9,
                "regionId": 1,
                "branchId": null
            }
        ],
        "channels": [
            {
                "campaignTChannelId": 7,
                "channelName": "SMS",
                "channelNameAr": "رسائل نصية",
                "campaignId": 9,
                "channelId": 1
            }
        ],
        "paymentTypes": [
            {
                "campaignPaymentTypeId": 6,
                "paymentTypeName": "Cash",
                "paymentTypeNameAr": "نقدا",
                "campaignId": 9,
                "paymentTypeId": 1
            }
        ],
        "targetVehicles": [
            {
                "campaignTargetVehicleId": 13,
                "modelVariantName": null,
                "modelVariantNameAr": null,
                "modelNameAr": "ار بي كارنز ",
                "modelName": "RP CARENS",
                "familyName": "Carens",
                "familyNameAr": "كارينز",
                "campaignId": 9,
                "modelFamilyId": 11,
                "brandId": null,
                "modelId": 9,
                "modelVariantId": null,
                "modelYear": null
            }
        ]
    }
]
``` 
 