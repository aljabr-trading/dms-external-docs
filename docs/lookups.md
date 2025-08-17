---
hide:
  - toc
---

```
PROD: https://dms-api.jtc.aljabr.com.sa/api
TEST: https://dms-api-test.jtc.aljabr.com.sa/api
```

## Master Lookup List (for reference)
<span class="http-get">GET</span> `/v1/leads/listmaster`

!!!Note
    This is provide the list of lookups we are using in the create lead. Based on listId, you can get the specific list.


### Response Body

```json
[
  {
    "listName": "Company",
    "listId": 0,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Branch",
    "listId": 1,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Brand",
    "listId": 2,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Department",
    "listId": 3,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Division",
    "listId": 4,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Priority",
    "listId": 22,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "CustomerType",
    "listId": 27,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Company Industry Type",
    "listId": 39,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Title",
    "listId": 50,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Nationality",
    "listId": 51,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Gender",
    "listId": 52,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Occupation",
    "listId": 53,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Language",
    "listId": 54,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Contact Type",
    "listId": 55,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Country",
    "listId": 56,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Purchase Plan",
    "listId": 59,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Payment Mode",
    "listId": 60,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Currency",
    "listId": 61,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Phone Code",
    "listId": 62,
    "parentListId": 56,
    "parentListName": "Country"
  },
  {
    "listName": "ModelFamily",
    "listId": 63,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Model Year",
    "listId": 64,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Lead Source",
    "listId": 70,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Lead Sub Source",
    "listId": 71,
    "parentListId": 70,
    "parentListName": "Lead Source"
  },
  {
    "listName": "Lead Intrerest",
    "listId": 74,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Lead Monthly Income",
    "listId": 78,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Lead Vehicle Type",
    "listId": 79,
    "parentListId": 0,
    "parentListName": ""
  },
  {
    "listName": "Customer Region",
    "listId": 100,
    "parentListId": 56,
    "parentListName": "Country"
  },
  {
    "listName": "Customer City",
    "listId": 101,
    "parentListId": 100,
    "parentListName": "Customer Region"
  }
]
 
```

## Master lookup based on lookup types
<span class="http-get">GET</span> `/v1/leads/list`

### Query Parameters

```
listId: integer
parentListId: integer(optional)
parentId: integer (optional)
``` 
listId will get the drop down list based on lookuptype
!!!Note
    Refer the listId from master lookup list
    parentListId and parentId: applicables for Region and City
    
        for Region: 
        listId: Region LookupId from master list
        parentListId: Country master Id
        parentId: Country Id which is selected
        
        for City: 
        listId: City LookupId from master list
        parentListId: Region master Id
        parentId: Region Id which is selected