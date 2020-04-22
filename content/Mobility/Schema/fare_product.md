```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/fare_product.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the fare product object",
    "type": "object",
    "properties" : {
        "id" : {
            "type" : "string"
        },
        "fare_media" : {
            "type" : "string"
        },
        "name" : {
            "type" : "string"
        },
        "fare_policy" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/policy.json"
        },
        "applies_to_items" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/core/schema/0.7.1/item.json#/properties/id"
            }
        }
    }
}
```