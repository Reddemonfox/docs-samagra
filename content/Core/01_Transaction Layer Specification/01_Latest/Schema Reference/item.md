Item
===
>Describes an item. Allows for domain extension.

### Schema Definition

|**Field**|**Type**|**Description**|
|---------|--------|---------------|
|id|string|This is the most unique identifier of a service item. An example of an Item ID could be the SKU of a product.
|parent_item_id|[Item/properties/id](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/item)|This is the most unique identifier of a service item. An example of an Item ID could be the SKU of a product.
|descriptor|[Descriptor](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/descriptor)|Describes the description of a real-world object. Maintained by Beckn Foundation
|price|[Price](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/price)|Describes the price of an item. Allows for domain extension.
|category_id|[Category/properties/id](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/category)|Unique id of the category
|location_id|[Location/properties/id](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/location)|
|time|[Time](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/time)|Describes time in its various forms. It can be a single point in time; duration; or a structured timetable of operations
|matched|boolean|
|related|boolean|
|recommended|boolean|
|tags|[Tags](/Core/01_Transaction%20Layer%20Specification/Latest/Schema%20Reference/tags)|Describes a tag. This is a simple key-value store which is used to contain extended metadata
