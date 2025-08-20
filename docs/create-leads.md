---
hide:
  - toc
---

## API endpoint


```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
``` 

<a><span class="http-get">POST</span></a> `/v1/leads/bulks`


---
Refere the comment  <span class="flag-required"> //Mandatory</span>  means the property is required 

### 📌 API
 
sample data with reference of master list mapping

#### Request Mapping

```json
{
  "leads": [
    {
      "company": "JTC", (List Id : 0  eg : JTC)
      "businessArea": "Sales", (List Id : 3 eg : Sales)
      "brand": "JMC", (List Id : 2 eg : Kia)
      "title": "Mr", (List Id : 50 eg : Mr)
      "nationality": "Saudi Arabian", (List Id : 51 eg : Saudi Arabian)
      "gender": "Male", (List Id : 52 eg: Male)
      "source": "Showroom", (List Id : 70 eg : Showroom)
      "subSource": "Walk-in", (List Id : 71 eg : Walk-in)
      "phoneCode": "00966", (List Id : 62 eg: 00966)
      "phoneNumber": "555555555", (user input eg : 5xxxxxxxx)
      "preferredLanguage": "English", (List Id : 54 eg : English)
      "preferredContactType": "Phone", (List Id : 55 eg : Phone)
      "purchasePlan": "Immediate", (List Id :59 eg : Immediate)
      "paymentMode": "Cash", (List Id : 60 eg : Cash)
      "monthlyIncome": "0-5000 SAR", (List Id : 78 eg : 0-5000 SAR)
      "currency": "SAR", (List Id : 61 eg : SAR)
      "testDriveRequired": true, (boolean eg : true)
      "acceptNewsLetter": true, (boolean eg : true)
      "acceptMarketing": true, (boolean eg : true)
      "acceptPrivatePolicy": true, (boolean eg : true)
      "priority": "Hot", (List Id : 22 eg : Hot)
      "leadType": "Company", (List Id : 55 eg : Company)
      "interest": "Vehicle Inquiry", (List Id : 74 eg : Vehicle Inquiry)
      "vehicleType": "New", (List Id : 79 eg : New)
      "firstName": "Abdullah", (user input eg : Abdullah)
      "middleName": "Mobarak", (user input eg : Mobarak)
      "lastName": "Careem", (user input eg : Careem)
      "dateOfBirth": "2025-08-17T06:49:41.761Z", (yyyy-mm-dd eg : 2025-08-17)
      "occupation": "Civil Engineer", (List Id 53 eg : Civil Engineer)
      "address1": "Building 7, King Fahad Road", (user input eg : Building 7, King Fahad Road)
      "address2": "Khobar", (user input eg : Khobar)
      "email": "string", (user input eg : email)
      "leadName": "Example Holdings", (user input eg : Example Holdings)
      "leadDate": "2025-08-17T06:49:41.761Z", (yyyy-mm-dd eg : 2025-08-17)
      "leadReference": "string", (user input eg : any text)
      "leadNote": "string", (user input eg : any text)
      "contactName": "Abdullah", (user input eg : Abdullah)
      "leadTypeName": "Company", (List Id : 27 eg : Company)
      "companyIndustryType": "Bank", (List Id : 39 eg : Bank)
      "customerCountry": "Saudi Arabia", (List Id : 56 eg : Saudi Arabia)
      "customerRegion": "Eastern Province", (List Id : 100 eg : Eastern Province)
      "customerCity": "Dammam", (List Id : 101 eg : Dammam)
      "vehicles": [
        {
          "modelFamily": "Grand Avenue", (List Id : 63 eg : Grand Avenue)
          "modelYear": 2025, (List Id : 64 eg : 2025)
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




#### Request Body <span class="flag-required"></span> 

Below are the possible values for creating lead and properties will be mandatory or optionals based on business conditions and type of the leads

!!!Note 
    Minimum 1 Lead and Maximum 20 leads per request will be allowed and for each lead minimum one vehicle details and maximum 5 vehicle details will be allowed.

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


#### Lead Type : Company  (Sample Json)
```json
{
   "leads":[                                          //Minimum 1 & Maximum 20
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
        "vehicles":[         //Minimum 1 & Maximum 5   //Mandatory
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
#### Lead Type : Individual  (Sample Json)

```json
{
   "leads":[                                            //Minimum 1 & Maximum 20
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
        "vehicles":[         //Minimum 1 & Maximum 5    //Mandatory
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
!!!warning "Maximum 20 leads are allowed"
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