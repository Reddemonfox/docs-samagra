```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/item.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a catalog item",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "name" : {
            "type" : "string"
        },
        "description" : {
            "type" : "string"
        },
        "image" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/image.json"
        },
        "price" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/price.json"
        },
        "tags" : {
            "type" : "array",
            "items" : {
                "type" : "string"
            } 
        },
        "primary" : {
            "type" : "boolean"
        },
        "selected" : {
            "type" : "boolean"
        },
        "quantity" : {
            "type" : "integer",
            "minimum": 0
        },
        "policy" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/policy.json"
        },
        "category" : {
            "type" : "string"
        }
    }
}
```