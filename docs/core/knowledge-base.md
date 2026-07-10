---
hide:
  - toc
---

Base URL
```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Knowledge Base   
<span class="http-get">GET</span> `/v1/core/knowledge-base`

Get knowledge base feed

### Query Parameters

```
companyId: integer (mandatory)
brandId: integer (mandatory)
ouId: integer (optional)
businessAreaId: integer (optional)
categoryId: integer (optional)
modifiedSince: string (optional)
lang: string
``` 
!!! note

    **`companyId` and `brandId` are mandatory fields.**

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **lang:** `ar`
  
 
### Response

```json
{
    "items": [
        {
            "knowledgeId": 35,
            "knowledgeCode": "KB34",
            "companyId": 1,
            "ouId": 2,
            "brandId": 2,
            "businessAreaId": 2,
            "categoryId": 1,
            "categoryName": "Warranty",
            "inquiry": "TEAS",
            "answer": "TEAS",
            "additionalInfo": "TEAS",
            "referenceLink": "",
            "fromDate": "2026-07-09T00:00:00",
            "modifiedDate": "2026-07-10T03:33:00.263"
        }
    ]
}
```
 
