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

Refere the comment <span class="flag-required"> //Mandatory</span> means the property is required

### 📌 API

sample data with reference of master list mapping

#### Request Mapping

```json
{
  "leads": [
    {
      "leadType": "Company", (List Id : 27 eg : Company)
      "title": "Mr", (List Id : 50 eg : Mr)
      "gender": "Male", (List Id : 52 eg: Male)
      "nationality": "Saudi Arabian", (List Id : 51 eg : Saudi Arabian)
      "firstName": "Abdullah", (user input eg : Abdullah)
      "middleName": "Mobarak", (user input eg : Mobarak)
      "lastName": "Careem", (user input eg : Careem)
      "companyName": "string", (user input eg : any text)
      "companyIndustryType": "Bank", (List Id : 39 eg : Bank)
      "contactName": "Abdullah", (user input eg : Abdullah)
      "dateOfBirth": "2025-08-17", (yyyy-MM-dd eg : 2025-08-17)
      "occupation": "Civil Engineer", (List Id 53 eg : Civil Engineer)
      "customerCountry": "Saudi Arabia", (List Id : 56 eg : Saudi Arabia)
      "customerRegion": "Eastern Province", (List Id : 100 eg : Eastern Province)
      "customerCity": "Dammam", (List Id : 101 eg : Dammam)
      "address1": "Building 7, King Fahad Road", (user input eg : Building 7, King Fahad Road)
      "address2": "Khobar", (user input eg : Khobar)
      "phoneCode": "00966", (List Id : 62 eg: 00966)
      "phoneNumber": "555555555", (user input eg : 5xxxxxxxx)
      "email": "string", (user input eg : email)
      "monthlyIncome": "0-5000 SAR", (List Id : 78 eg : 0-5000 SAR)
      "preferredLanguage": "English", (List Id : 54 eg : English)
      "preferredContactType": "Phone Call", (List Id : 55 eg : Phone Call)
      "company": "JTC", (List Id : 0  eg : JTC)
      "brand": "Kia", (List Id : 2 eg : Kia)
      "businessArea": "Sales", (List Id : 3 eg : Sales)
      "leadDate": "2025-08-17", (yyyy-MM-dd eg : 2025-08-17)
      "interest": "Vehicle Inquiry", (List Id : 74 eg : Vehicle Inquiry)
      "source": "Showroom", (List Id : 70 eg : Showroom)
      "subSource": "Walk-in", (List Id : 71 eg : Walk-in)
      "leadName": "Example Holdings", (user input eg : Example Holdings)
      "leadReference": "string", (user input eg : any text)
      "leadNote": "string", (user input eg : any text)
      "vehicleType": "New", (List Id : 79 eg : New)
      "vehicles": [
        {
          "modelFamily": "Rio", (List Id : 63 eg : Rio)
          "modelYear": 2025, (List Id : 64 eg : 2025)
          "modelMemo": "string", (user input eg : any text)
          "modelPreferences": "string", (user input eg : any text)
          "totalQty": 1 (minimum 1 & maximum 1000)
        }
      ],
      "purchasePlan": "Immediate", (List Id :59 eg : Immediate)
      "paymentMode": "Cash", (List Id : 60 eg : Cash)
      "currency": "SAR", (List Id : 61 eg : SAR)
      "priority": "Hot", (List Id : 75 eg : Hot)
      "testDriveRequired": true, (boolean eg : true)
      "acceptNewsLetter": true, (boolean eg : true)
      "acceptMarketing": true, (boolean eg : true)
      "acceptPrivatePolicy": true, (boolean eg : true)
    }
  ],
  "isProcessed": 1
}
```

#### Request Body <span class="flag-required"></span>

Below are the possible values for creating lead and properties will be mandatory or optionals based on business conditions and type of the leads

!!!Note
    Minimum 1 Lead and Maximum 20 leads per request will be allowed and for each lead minimum one vehicle details and maximum 5 vehicle details will be allowed.

<!--
```json
{
  "leads": [
    {
      "leadType": "Company/Individual",
      "title": "Mr",
      "gender": "Male",
      "nationality": "Saudi Arabian",
      "firstName": "Abdullah",
      "middleName": "Mobarak",
      "lastName": "Careem",
      "contactName": "Abdullah",
      "companyName": "Example Holdings",
      "companyIndustryType": "Bank",
      "dateOfBirth": "2025-08-17T06:49:41.761Z",
      "occupation": "string",
      "customerCountry": "Saudi Arabia",
      "customerRegion": "Eastern Province",
      "customerCity": "Dammam",
      "address1": "Building 7, King Fahad Road",
      "address2": "Khobar",
      "phoneCode": "00966",
      "phoneNumber": "555555555",
      "email": "example@example.com",
      "monthlyIncome": "0-5000 SAR",
      "preferredLanguage": "English",
      "preferredContactType": "Phone",
      "company": "JTC",
      "brand": "Kia",
      "businessArea": "Sales",
      "branch": "string",
      "leadDate": "2025-08-17T06:49:41.761Z",
      "interest": "Vehicle Inquiry",
      "source": "Showroom",
      "subSource": "Walk-in",
      "leadName": "Example Holdings",
      "leadReference": "string",
      "leadNote": "string",
      "vehicleType": "New",
      "vehicles": [
        {
          "modelFamily": "Rio",
          "modelYear": 2025,
          "modelMemo": "string",
          "modelPreferences": "string",
          "totalQty": 1
        }
      ],
      "purchasePlan": "Immediate",
      "paymentMode": "Cash",
      "currency": "SAR",
      "priority": "Hot",
      "testDriveRequired": true,
      "acceptNewsLetter": true,
      "acceptMarketing": true,
      "acceptPrivatePolicy": true
    }
  ],
  "isProcessed": 1
}
```
-->

#### Lead Type : Company (Sample Json)

```json
{
  "leads": [                                                    // Minimum 1 & Maximum 20
    {
      "leadType": "Company",                                    // Mandatory
      "contactName": "",                                        // Mandatory
      "companyName": "",                                        // Mandatory
      "companyIndustryType": "Bank",                            // Mandatory
      "dateOfBirth": yyyy-MM-dd,
      "occupation": "string",
      "customerCountry": "Saudi Arabia",                        // Mandatory
      "customerRegion": "Riyadh",                               // Mandatory
      "customerCity": "Afif",                                   // Mandatory
      "address1": "string",
      "address2": "string",
      "phoneCode": "00966",                                     // Mandatory
      "phoneNumber": "",                                        // Mandatory
      "email": "",
      "monthlyIncome": "string",
      "preferredLanguage": "Arabic",                            // Mandatory
      "preferredContactType": "email",
      "company": "JTC",                                         // Mandatory
      "brand": "KIA",                                           // Mandatory
      "businessArea": "Sales",                                  // Mandatory
      "branch": "string",
      "leadDate": "yyyy-MM-dd",
      "interest": "Price Quote",                                // Mandatory
      "source": "Direct Contact",                               // Mandatory
      "subSource": "Email",                                     // Mandatory
      "leadName": "",                                           // Mandatory
      "leadReference": "",
      "leadNote": "",
      "vehicleType": "New",
      "vehicles": [                  // Minimum 1 & Maximum 5    // Mandatory
        {
          "modelFamily": "RIO",                                  // Mandatory
          "modelYear": "2024",
          "modelMemo": "",
          "modelPreferences": "",
          "totalQty": 1                                          // Mandatory
        }
      ],
      "purchasePlan": "Within 30 Days",
      "paymentMode": "Credit",
      "currency": "SAR",
      "priority": "Warm",                                         // Mandatory
      "testDriveRequired": true,                                  // Mandatory
      "acceptNewsLetter": true,                                   // Mandatory
      "acceptMarketing": true,                                    // Mandatory
      "acceptPrivatePolicy": true                                 // Mandatory
    }
  ],
  "isProcessed": 1
}

```

#### Lead Type : Individual (Sample Json)

```json
{
  "leads": [                                                      // Minimum 1 & Maximum 20
    {
      "leadType": "Individual",                                   // Mandatory
      "title": "Mr",
      "gender": "Male",
      "nationality": "Saudi Arabian",
      "firstName": "",                                            // Mandatory
      "middleName": "",
      "lastName": "",
      "contactName": "",
      "companyName": "",
      "companyIndustryType": "",
      "dateOfBirth": "yyyy-MM-dd",
      "occupation": "",
      "customerCountry": "Saudi Arabia",                          // Mandatory
      "customerRegion": "Riyadh",                                 // Mandatory
      "customerCity": "Afif",                                     // Mandatory
      "address1": "",
      "address2": "",
      "phoneCode": "00966",                                       // Mandatory
      "phoneNumber": "",                                          // Mandatory
      "email": "",
      "monthlyIncome": "5000-10000 SAR",
      "preferredLanguage": "Arabic",                              // Mandatory
      "preferredContactType": "Email",
      "company": "JTC",                                           // Mandatory
      "brand": "KIA",                                             // Mandatory
      "businessArea": "Sales",                                    // Mandatory
      "branch": "string",
      "leadDate": "yyyy-MM-dd",
      "interest": "Price Quote",                                  // Mandatory
      "source": "Direct Contact",                                 // Mandatory
      "subSource": "Email",                                       // Mandatory
      "leadName": "",                                             // Mandatory
      "leadReference": "",
      "leadNote": "",
      "vehicleType": "New",
      "vehicles": [                   // Minimum 1 & Maximum 5    // Mandatory
        {
          "modelFamily": "RIO",                                   // Mandatory
          "modelYear": "2024",
          "modelMemo": "",
          "modelPreferences": "",
          "totalQty": 1                                           // Mandatory
        }
      ],
      "purchasePlan": "Within 30 Days",
      "paymentMode": "Credit",
      "currency": "SAR",
      "priority": "Warm",                                         // Mandatory
      "testDriveRequired": true,                                  // Mandatory
      "acceptNewsLetter": true,                                   // Mandatory
      "acceptMarketing": true,                                    // Mandatory
      "acceptPrivatePolicy": true                                 // Mandatory
    }
  ],
  "isProcessed": 1
}
```

#### Response

```json
integer
```

!!!warning 
    "Maximum 20 leads are allowed"

#### <span class="flag-required">\*</span> leadType: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={CUSTOMER_TYPE}`

!!! note "Mandatory Fields for Company Lead Type"
    When `leadType` value is Individual, the following fields are mandatory

    1. `firstName`

    When `leadType` value is Company, the following fields will be **mandatory**:

    1. `companyIndustryType`
    2. `contactName`
    3. `companyName`

#### companyIndustryType: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={CUSTOMER_INDUSTRY_TYPE}`

#### contactName: `string`

#### companyName: `string`

#### title: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={TITLE}`

#### nationality: `string`

<a"><span class="http-get">GET</span></a> `/v1/leads/list?listId={NATIONALITY}`

#### gender: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={GENDER}`

#### firstName: `string`

#### lastName: `string`

#### middleName: `string`

#### dateOfBirth: `yyyy-MM-dd`

#### occupation: `string`

#### <span class="flag-required">\*</span> customerCountry: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={COUNTRY}`

#### <span class="flag-required">\*</span> customerRegion: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={REGION}&parentId={customerCountry.value}`

####<span class="flag-required">\*</span> customerCity: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={CITY}&parentId={customerRegion.value}`

#### address1: `string`

#### address2: `string`

#### <span class="flag-required">\*</span> phoneCode: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={PHONE_CODE}`

#### phoneNumber: `string`

!!! note "phoneNumber length should be 9 characters"

#### email: `string`

#### monthlyIncome: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={LEAD_MONTHLY_INCOME}`

#### <span class="flag-required">\*</span> preferredLanguage: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={LANGUAGE}`

#### preferredContactType: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={CONTACT_TYPE}`

#### company: `string`

#### <span class="flag-required">\*</span> ou: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={OU_TYPE}`

#### <span class="flag-required">\*</span> businessArea: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={BUSINESS_AREA}&parentId={ou_type.value}`

#### <span class="flag-required">\*</span> leadDate: `string`

#### <span class="flag-required">\*</span> leadInterest: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={LEAD_INTEREST}`

#### <span class="flag-required">\*</span> source: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={LEAD_SOURCE}`

#### <span class="flag-required">\*</span> subSource: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={LEAD_SUB_SOURCE}&parentId={lead_source.value}`

#### <span class="flag-required">\*</span> leadName: `string`

#### leadReference: `string`

#### leadNote: `string`

#### vehicleType: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={VEHICLE_TYPE}`

#### vehicles: `array`
!!! info 
    #### modelFamily: `string`

    <a><span class="http-get">GET</span></a> `/v1/leads/list?listId={MODEL_FAMILY}&parentId={ou_type.value}`

    #### modelYear: `string`

    <a><span class="http-get">GET</span></a> `/v1/leads/list?listId={MODEL_YEAR}`

    <!-- should I keep as not in json -->
    #### modelMemo: `string`

    <!-- should I keep as not in json -->
    #### modelPreferences: `string`

    <!-- should I keep as not in json -->
    #### totalQty: `string`

#### purchasePlan: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={PURCHASE_PLAN}`

#### paymentMode: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={PAYMENT_MODE}`

#### currency: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={CURRENCY}`

#### <span class="flag-required">\*</span> priority: `string`

<a><span class="http-get">GET</span></a> `/v1/leads/list?listId={LEAD_PRIORITY}`

#### testDriveRequired: `boolean`

#### acceptNewsLetter: `boolean`

#### acceptMarketing: `boolean`

#### acceptPrivatePolicy: `boolean`
