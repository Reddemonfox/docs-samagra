Billing
===
>Describes a billing event

### Schema Definition

|**Field**|**Type**|**Description**|
|---------|--------|---------------|
|name|string|Personal details of the customer needed for billing.
|organization|[Organization](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/organization)|Describes an organization
|address|[Address](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/address)|Describes an address
|email|string|
|phone|string|
|time|[Time](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/time)|Describes time in its various forms. It can be a single point in time; duration; or a structured timetable of operations
|tax_number|string|
|created_at|string|
|updated_at|string|
