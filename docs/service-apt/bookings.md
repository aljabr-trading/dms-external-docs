---
hide:
  - toc
---

Base URL

```
PROD: https://dms-gs.jtc.aljabr.com.sa/gs
TEST: https://dms-gs-test.jtc.aljabr.com.sa/gs
```

## Search service appointment bookings
### Returns service appointment bookings for a required brand as ServiceRequestViewExternal rows. OUId is optional: when supplied it must match the brand; when omitted a default OU is used if the brand has exactly one, otherwise results are filtered by brand only. At least one of contactNo, requestNo, or customerIdentificationNo is required. Optional filters: businessAreaId, branchId, isOpen, isFutureOnly, pageNumber, and pageSize. lang (en/ar, default en) collapses bilingual lookup texts onto the primary fields; Arabic-only properties are omitted from the response.

<span class="http-get">GET</span> `/v1/service-apt/bookings`

### Query Parameters

```
companyId: integer                      // Mandatory
brandId: integer                        // Mandatory
ouId: integer                           // Optional (must match brand when supplied)
businessAreaId: integer                 // Mandatory
branchId: integer                       // Optional
isOpen: boolean                         // Optional (true: Created, NoShow, Pending)
isFutureOnly: boolean                   // Optional (true: request date in the future only)
contactNo: string                       // At least one of contactNo, requestNo, or customerIdentificationNo is required
requestNo: string                       // At least one of contactNo, requestNo, or customerIdentificationNo is required
customerIdentificationNo: string        // At least one of contactNo, requestNo, or customerIdentificationNo is required
pageNumber: integer                     // Optional
pageSize: integer                       // Optional
lang: string                            // Optional "en" | "ar"
```

!!! note

    **Example:**

    - **companyId:** `1`
    - **brandId:** `1`
    - **businessAreaId:** `3`
    - **contactNo:** `555123456`
    - **pageNumber:** `1`
    - **pageSize:** `10`
    - **lang:** `en`

### Response

```json
[
  {
    "serviceRequestId": 90001,
    "detailRequestId": 70001,
    "requestNo": "SA-2026-0001",
    "companyId": 1,
    "companyText": "Al Jabr",
    "regionId": 1,
    "regionName": "Central",
    "ouId": 1,
    "ouName": "Passenger Cars",
    "brandId": 1,
    "brandName": "Kia",
    "branchId": 101,
    "branchName": "Riyadh Showroom",
    "businessAreaId": 3,
    "departmentName": "Service",
    "remarks": "Periodic maintenance",
    "sourceId": 1,
    "source": "Website",
    "subSourceId": 2,
    "subSource": "Campaign",
    "isActive": true,
    "statusId": 1,
    "status": "Created",
    "createdBy": 1001,
    "createdUser": "api.user",
    "modifiedBy": 1001,
    "modifiedUser": "api.user",
    "createdDate": "2026-06-20T15:00:00",
    "modifiedDate": "2026-06-20T15:00:00",
    "guId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "companyVersionId": 1,
    "modelFamilyId": 1001,
    "modelFamilyName": "Sportage",
    "modelYear": "2026",
    "vinCode": "KNAAE12345A123456",
    "plateNo": "ABC 1234",
    "customerVehicleId": 5001,
    "prospectVehicleId": 0,
    "prospectId": 0,
    "customerId": 4001,
    "recordTypeId": 1,
    "recordTypeName": "Customer",
    "customerVersionId": 1,
    "requestDate": "2026-06-22T00:00:00",
    "milage": 15000,
    "customerNumber": "555123456",
    "advisorId": 3001,
    "categoryId": 10,
    "categoryName": "Maintenance",
    "subCategoryId": 20,
    "subCategoryName": "Periodic",
    "aptMasterId": 500,
    "aptSlotId": 1201,
    "fullContactNumber": "966555123456",
    "firstName": "Ahmed",
    "lastName": "Ali",
    "companyName": "",
    "contactName": "Ahmed Ali",
    "customerTypeId": 1,
    "customerType": "Individual",
    "emailAddress": "ahmed.ali@example.com",
    "phoneCodeId": 1,
    "phoneCode": "+966",
    "customerName": "Ahmed Ali",
    "startDate": "2026-06-22T09:00:00",
    "endDate": "2026-06-22T10:00:00",
    "customerRemarks": "Please call before arrival"
  }
]
```

### Response (400)

```json
{
  "message": "At least one of contactNumber, requestNo, or customerIdentificationNo is required"
}
```

!!! note

    The query parameter name is `contactNo`. The 400 example text uses `contactNumber`.
