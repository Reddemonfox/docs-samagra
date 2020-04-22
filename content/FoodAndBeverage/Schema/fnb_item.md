```json
{
    "$id": "https://developers.beckn.org/fnb/schema/0.7.1/fnb_item.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the F&B item object",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "descriptor" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/descriptor.json"
        },
        "price" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/price.json"
        },
        "preparation_time" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/scalar.json"
        },
        "availability" : {
            "type" : "object",
            "properties": {
                "available" : {
                    "type" : "boolean"
                },
                "available_from" : {
                    "$ref" : "https://developers.beckn.org/core/schema/0.7.1/time.json"                    
                }
            }
        },
        "categories" : {
            "type" : "array",
            "items" : {
                "type" : "string"
            }
        },
        "tags" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/tags.json"
        }
    }
}
```