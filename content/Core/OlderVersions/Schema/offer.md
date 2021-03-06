```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/offer.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the offer object",
    "type": "object",
    "properties" : {
        "id" : {
            "type" : "string"
        },
        "name" : {
            "type" : "string"
        },
        "code" : {
            "type" : "string"
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