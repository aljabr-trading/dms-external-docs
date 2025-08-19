---
hide:
  - toc
---

```
PROD: https://dms-api.jtc.aljabr.com.sa/api
TEST: https://dms-api-test.jtc.aljabr.com.sa/api
```

## Master List (for reference)
<span class="http-get">GET</span> `/v1/leads/listmaster`

!!!Note
    This provide the Master list we are using in the create lead. Based on List Id, you can get the specific list.




### Response Body

```json
[
  {
    "listName": "Company",
    "List Id": 0,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Branch",
    "List Id": 1,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Brand",
    "List Id": 2,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Department",
    "List Id": 3,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Division",
    "List Id": 4,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Priority",
    "List Id": 22,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "CustomerType",
    "List Id": 27,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Company Industry Type",
    "List Id": 39,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Title",
    "List Id": 50,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Nationality",
    "List Id": 51,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Gender",
    "List Id": 52,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Occupation",
    "List Id": 53,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Language",
    "List Id": 54,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Contact Type",
    "List Id": 55,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Country",
    "List Id": 56,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Purchase Plan",
    "List Id": 59,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Payment Mode",
    "List Id": 60,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Currency",
    "List Id": 61,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Phone Code",
    "List Id": 62,
    "parentList Id": 56,
    "parentListName": "Country"
  },
  {
    "listName": "ModelFamily",
    "List Id": 63,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Model Year",
    "List Id": 64,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Lead Source",
    "List Id": 70,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Lead Sub Source",
    "List Id": 71,
    "parentList Id": 70,
    "parentListName": "Lead Source"
  },
  {
    "listName": "Lead Intrerest",
    "List Id": 74,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Lead Monthly Income",
    "List Id": 78,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Lead Vehicle Type",
    "List Id": 79,
    "parentList Id": 0,
    "parentListName": ""
  },
  {
    "listName": "Customer Region",
    "List Id": 100,
    "parentList Id": 56,
    "parentListName": "Country"
  },
  {
    "listName": "Customer City",
    "List Id": 101,
    "parentList Id": 100,
    "parentListName": "Customer Region"
  }
]
 
```

## Master list based on lookup types
<span class="http-get">GET</span> `/v1/leads/list`

### Query Parameters

```
List Id: integer
parentList Id: integer(optional)
parentId: integer (optional)  
``` 
List Id will get the drop down list based on lookuptype
!!!Note
    Refer the List Id from master lookup list
    parentList Id and parentId: applicables for Region and City
    
        example for Region: 
        List Id: Region LookupId from master list (List Id 100)
        parentList Id: Country master Id (List Id 56) 
        parentId: Country Id which is selected (List Id 56, Saudi Arabia)
        
        example for City: 
        List Id: City LookupId from master list (List Id 101)
        parentList Id: Region master Id (List Id 100)
        parentId: Region Id which is selected (List Id 100, Riyadh)