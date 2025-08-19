---
hide:
  - toc
---

# Aljabr Dealer Management System API Documentation

Welcome to the **Dealer Management System (DMS) API Documentation**.  
This website is designed to help developers and integrators understand and interact with our API endpoints efficiently.

## Purpose of this API

The DMS API allows authorized systems to interact with our Dealer Management System programmatically.  
It is intended for use by partners, dealerships, and internal teams who need to integrate their applications with DMS data and processes.


With this API, you can:

- Create and retrieve leads.

- Access Master List such as titles, nationalities, regions, and more.

- Integrate with existing ERP platforms to streamline automotive sales operations.

## Current Scope

At present, this documentation covers the **"Create Lead"** process, which enables clients to submit new leads into the DMS, along with all associated customer and vehicle details.

<!-- - Inventory queries
- Appointment scheduling
- Test drive management
- Sales reporting
-->

## How to Use This Documentation
URL: 

```
PROD: https://dms-api.jtc.aljabr.com.sa/swagger/index.html
TEST: https://dms-api-test.jtc.aljabr.com.sa/swagger/index.html
``` 

Each API endpoint in this documentation includes:
- **Endpoint URL**  
- **HTTP method** (GET, POST)  
- **Request body format** (with example JSON)  
- **Response examples**  
- **Field descriptions**  

As applicable, the Master list should be refered with specified endpoints to retrieve possible values for list certain fields, ensuring valid data. Incase if any incorrect or junk data for list field will be resulted in errors.

---