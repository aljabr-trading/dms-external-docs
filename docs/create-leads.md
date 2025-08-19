---
hide:
  - toc
---

## API endpoint


```
PROD: https://dms-api.jtc.aljabr.com.sa/api
TEST: https://dms-api-test.jtc.aljabr.com.sa/api
``` 
<a><span class="http-get">POST</span></a> `/v1/leads/bulks`


---
This symbol <span class="flag-required">*</span>  means the field is mandatory 

### 📌 API

### Field Name <span class="flag-required">*</span>

What do we type here?

#### Request Mapping

```json
{
  "leads": [
    {
      "company": "JTC", (list Id : 0  eg : JTC)
      "businessArea": "Sales", (list Id : 3 eg : Sales)
      "brand": "JMC", (list Id : 2 eg : Kia)
      "title": "Mr", (list Id : 50 eg : Mr)
      "nationality": "Saudi Arabian", (list Id : 51 eg : Saudi Arabian)
      "gender": "Male", (list Id : 52 eg: Male)
      "source": "Showroom", (list Id : 70 eg : Showroom)
      "subSource": "Walk-in", (list Id : 71 eg : Walk-in)
      "phoneCode": "00966", (list Id : 62 eg: 00966)
      "phoneNumber": "555555555", (user input eg : 5xxxxxxxx)
      "preferredLanguage": "English", (list Id : 54 eg : English)
      "preferredContactType": "Phone", (list Id : 55 eg : Phone)
      "purchasePlan": "Immediate", (list Id :59 eg : Immediate)
      "paymentMode": "Cash", (list Id : 60 eg : Cash)
      "monthlyIncome": "0-5000 SAR", (list Id : 78 eg : 0-5000 SAR)
      "currency": "SAR", (list Id : 61 eg : SAR)
      "testDriveRequired": true, (boolean eg : true)
      "acceptNewsLetter": true, (boolean eg : true)
      "acceptMarketing": true, (boolean eg : true)
      "acceptPrivatePolicy": true, (boolean eg : true)
      "priority": "Hot", (list Id : 22 eg : Hot)
      "leadType": "Company", (list Id : 55 eg : Company)
      "interest": "Vehicle Inquiry", (list Id : 74 eg : Vehicle Inquiry)
      "vehicleType": "New", (list Id : 79 eg : New)
      "firstName": "Abdullah", (user input eg : Abdullah)
      "middleName": "Mobarak", (user input eg : Mobarak)
      "lastName": "Careem", (user input eg : Careem)
      "dateOfBirth": "2025-08-17T06:49:41.761Z", (yyyy-mm-dd eg : 2025-08-17)
      "occupation": "Civil Engineer", (list Id 53 eg : Civil Engineer)
      "address1": "Building 7, King Fahad Road", (user input eg : Building 7, King Fahad Road)
      "address2": "Khobar", (user input eg : Khobar)
      "email": "string", (user input eg : email)
      "leadName": "Example Holdings", (user input eg : Example Holdings)
      "leadDate": "2025-08-17T06:49:41.761Z", (yyyy-mm-dd eg : 2025-08-17)
      "leadReference": "string", (user input eg : any text)
      "leadNote": "string", (user input eg : any text)
      "contactName": "Abdullah", (user input eg : Abdullah)
      "leadTypeName": "Company", (list Id : 27 eg : Company)
      "companyIndustryType": "Bank", (list Id : 39 eg : Bank)
      "customerCountry": "Saudi Arabia", (list Id : 56 eg : Saudi Arabia)
      "customerRegion": "Eastern Province", (list Id : 100 eg : Eastern Province)
      "customerCity": "Dammam", (list Id : 101 eg : Dammam)
      "vehicles": [
        {
          "modelFamily": "Grand Avenue", (list Id : 63 eg : Grand Avenue)
          "modelYear": 2025, (list Id : 64 eg : 2025)
          "modelMemo": "string", (user input eg : any text)
          "modelPreferences": "string", (user input eg : any text)
          "totalQty": 1 (minimum 1 & maximum 1000)
        }
      ]
    }
  ],
  "isProcessed": 1
}
```




#### Request Body <span class="flag-required">*</span>

```json
{
  "leads": [
    {
      "company": "JTC",
      "businessArea": "Sales",
      "brand": "JMC",
      "title": "Mr",
      "nationality": "Saudi Arabian",
      "gender": "Male",
      "source": "Showroom",
      "subSource": "Walk-in",
      "phoneCode": "00966",
      "phoneNumber": "555555555",
      "preferredLanguage": "English",
      "preferredContactType": "Phone",
      "purchasePlan": "Immediate",
      "paymentMode": "Cash",
      "monthlyIncome": "0-5000 SAR",
      "currency": "SAR",
      "testDriveRequired": true, 
      "acceptNewsLetter": true,
      "acceptMarketing": true,
      "acceptPrivatePolicy": true,
      "priority": "Hot",
      "leadType": "Company",
      "interest": "Vehicle Inquiry",
      "vehicleType": "New",
      "firstName": "Abdullah",
      "middleName": "Mobarak",
      "lastName": "Careem",
      "dateOfBirth": "2025-08-17T06:49:41.761Z",
      "occupation": "string",
      "address1": "Building 7, King Fahad Road",
      "address2": "Khobar",
      "email": "example@example.com",
      "leadName": "Example Holdings",
      "leadDate": "2025-08-17T06:49:41.761Z",
      "leadReference": "string",
      "leadNote": "string",
      "contactName": "Abdullah",
      "leadTypeName": "Company", 
      "companyIndustryType": "Bank",
      "customerCountry": "Saudi Arabia",
      "customerRegion": "Eastern Province",
      "customerCity": "Dammam",
      "vehicles": [
        {
          "modelFamily": "Grand Avenue",
          "modelYear": 2025,
          "modelMemo": "string",
          "modelPreferences": "string",
          "totalQty": 1
        }
      ]
    }
  ],
  "isProcessed": 1
}
```


#### Company Request Body Example
```json
{
   "leads":[
      {
        "leadtype":"Company",                         //Mandatory
        "companyIndustryType":"Bank",                 //Mandatory
        "companyname":"",                             //Mandatory
        "contactname":"",                             //Mandatory
        "phonecode":"00966",                          //Mandatory
        "phoneNumber":"",                             //Mandatory
        "preferredLanguage":"Arabic",                 //Mandatory
        "preferredContactType":"email",
        "leadName":"",                                //Mandatory
        "leadReference":"",
        "source":"Direct Contact",                    //Mandatory
        "subsource":"Email",                          //Mandatory
        "interest":"Price Quote",                     //Mandatory
        "customerCountry":"Saudi Arabia",             //Mandatory
        "customerRegion":"Riyadh",                    //Mandatory
        "customerCity":"Afif",                        //Mandatory
        "purchasePlan":"Within 30 Days",
        "paymentMode":"Credit",      
        "currency":"SAR",         
        "brand":"KIA",                                 //Mandatory
        "vehicleType":"New",
        "businessArea":"Sales",                        //Mandatory
        "testdriverequired":true,                      //Mandatory
        "leadnote":"",
        "acceptMarketing":true, 
        "acceptNewsLetter":true,                       //Mandatory
        "acceptPrivatePolicy":true,                    //Mandatory
        "company":"JTC",                               //Mandatory
        "priority":"Warm",                             //Mandatory
        "leaddate":"yyyy-dd-mm",
        "vehicles":[                                   //Mandatory
          {
            "modelFamily":"RIO",                       //Mandatory
            "modelYear":"2024",
            "ModelMemo":"",
            "ModelPreferences":"",
            "totalQty":1                               //Mandatory
          }
        ]
      }
   ]
    "isProcessed":1,
}

```
#### Individual Request Body Example

```json
{
   "leads":[
      {
        "leadtype":"Individual",                        //Mandatory
        "title":"Mr",
        "firstName":"",                                 //Mandatory
        "middlename":"",
        "lastName":"",
        "nationality":"Saudi Arabian",                  //Mandatory
        "gender":"Male",
        "dateofbirth":"yyyy-mm-dd",
        "occupation":"",
        "address1":"",
        "address2":"",       
        "email":"",
        "phonecode":"00966",                            //Mandatory
        "phoneNumber":"",                               //Mandatory
        "preferredLanguage":"Arabic",                   //Mandatory
        "preferredContactType":"Email",
        "leadName":"",                                  //Mandatory
        "leadReference":"",
        "source":"Direct Contact",                      //Mandatory
        "subsource":"Email",                            //Mandatory
        "interest":"Price Quote",                       //Mandatory
        "customerCountry":"Saudi Arabia",               //Mandatory
        "customerRegion":"Riyadh",                      //Mandatory
        "customerCity":"Afif",                          //Mandatory
        "purchasePlan":"Within 30 Days",
        "paymentMode":"Credit",
        "monthlyIncome":"5000-10000 SAR",         
        "currency":"SAR",         
        "brand":"KIA",                                  //Mandatory
        "vehicleType":"New",
        "businessArea":"Sales",                         //Mandatory
        "testdriverequired":"true",                     //Mandatory
        "leadnote":"",
        "acceptMarketing":"true",
        "acceptNewsLetter":"true",
        "acceptPrivatePolicy":"true",                   //Mandatory
        "company":"JTC",                                //Mandatory
        "priority":"Warm",                              //Mandatory
        "leaddate":"yyyy-mm-dd",
        "vehicles":[                                    //Mandatory
            {
               "modelFamily":"RIO",                     //Mandatory
               "modelYear":"2024",
               "ModelMemo":"",
               "ModelPreferences":"",
               "totalQty":1                             //Mandatory
            }
         ]
      }
   ]
    "isProcessed":1,
}

```



#### Response

```json
integer
```

---


#### leadType <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{CUSTOMER_TYPE}`

!!! note "Mandatory Fields for Company Lead Type"
    When `leadType` value is Individual, the following fields are mandatory

    1. `firstName`

    When `leadType` value is Company, the following fields will be **mandatory**:
    
    1. `companyIndustryType`
    2. `contactName`
    3. `leadTypeName`


#### companyIndustryType 

<a><span class="http-get">GET</span></a> `/v1/list/{CUSTOMER_INDUSTRY_TYPE}`

#### contactName:`string`

#### leadTypeName:`string`

#### title

<a><span class="http-get">GET</span></a> `/v1/list/{TITLE}`

#### nationality

<a"><span class="http-get">GET</span></a> `/v1/list/{NATIONALITY}`

#### gender

<a><span class="http-get">GET</span></a> `/v1/list/{GENDER}`

#### firstName:`string`

#### lastName:`string`

#### middleName:`string`

#### dateOfBirth:`yyyy-mm-dd` 

#### occupation:`string`

#### customerCountry <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{COUNTRY}`  

#### customerRegion <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{REGION}?parentId={customerCountry.value}`

#### customerCity <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{CITY}?parentId={customerRegion.value}`

#### address1:`string`

#### address2:`string`

#### phoneCode <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{PHONE_CODE}`

#### phoneNumber:`string`

!!! note "phoneNumber length should be 9 characters"

#### email:`string`

#### monthlyIncome

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_MONTHLY_INCOME}`

#### preferredLanguage <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LANGUAGE}`

#### preferredContactType

<a><span class="http-get">GET</span></a> `/v1/list/{CONTACT_TYPE}`

#### company:`JTC`

#### ou <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{OU_TYPE}`

#### businessArea <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{BUSINESS_AREA}?parentId={ou_type.value}`

#### branch <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{BRANCH_TYPE}?parentId={branch_type.value}`

#### leadDate:`string` <span class="flag-required">*</span>

#### leadInterest <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_INTEREST}`

#### source <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_SOURCE}`

#### subSource <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_SUB_SOURCE}?parentId={lead_source.value}`

#### leadName:`string` <span class="flag-required">*</span>

#### leadReference:`string`

#### leadNote:`string`

#### vehicleType

<a><span class="http-get">GET</span></a> `/v1/list/{VEHICLE_TYPE}`

#### vehicles.modelFamily

<a><span class="http-get">GET</span></a> `/v1/list/{MODEL}?parentId={ou_type.value}`

#### vehicles.modelYear

<a><span class="http-get">GET</span></a> `/v1/list/{MODEL_YEAR}`

<!-- should I keep as not in json -->
#### vehicles.modelMemo:`string`

<!-- should I keep as not in json -->
#### vehicles.modelPreferences:`string`

<!-- should I keep as not in json -->
#### vehicles.totalQty:`string`


#### purchasePlan

<a><span class="http-get">GET</span></a> `/v1/list/{PURCHASE_PLAN}`

#### paymentMode

<a><span class="http-get">GET</span></a> `/v1/list/{PAYMENT_MODE}`

#### currency

<a><span class="http-get">GET</span></a> `/v1/list/{CURRENCY}`

#### priority <span class="flag-required">*</span>

<a><span class="http-get">GET</span></a> `/v1/list/{LEAD_PRIORITY}`

#### testDriveRequired

<a><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`

#### acceptNewsLetter

<a><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`

#### acceptMarketing

<a><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`

#### acceptPrivatePolicy

<a><span class="http-get">GET</span></a> `/v1/list/{YES_OR_NO}`