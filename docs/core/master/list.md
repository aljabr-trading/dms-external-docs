---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Master list based on lookup types (with language specific)
<span class="http-get">GET</span> `/v1/core/list`

### Query Parameters

```
listId: integer (default: 0)
parentListId: integer (default: 0)
parentId: integer (default: 0)
lang: string (default "en") "en" | "ar"
``` 

This will provide the master list based on the language provided, default is en

### Response

```json
[
  {
    "listName": "Company",
    "id": 1,
    "text": "JTC",                                // Text based on lang passed
    "code": "JTC",
    "listId": 0,
    "parentListId": 0,
    "parentId": 0,
    "regularExpression": ""
  },
  {
    "listName": "Branch",
    "id": 1,
    "text": "الرياض - القادسية",                // Text based on lang passed
    "code": "LYK1",
    "listId": 1,
    "parentListId": 0,
    "parentId": 0,
    "regularExpression": ""
  }
]
```
