```json
{
    "$id": "https://developers.beckn.org/fnb/schema/0.7.1/fnb_service.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the F&B service of a restaurant",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "menu" : {
            "type" : "array",
            "items": {
                "type" : "object",
                "properties" : {
                    "item" : {
                        "$ref" : "https://developers.beckn.org/fnb/schema/0.7.1/fnb_item.json"
                    }
                }
            }
        },
        "provider" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/provider.json"
        },
        "schedule" : {
            "type" : "array",
            "items" : {
                "type" : "object",
                "properties": {
                    "open" : {
                        "$ref" : "https://developers.beckn.org/core/schema/0.7.1/time.json"
                    },
                    "close" : {
                        "$ref" : "https://developers.beckn.org/core/schema/0.7.1/time.json"
                    }
                } 
            }
        },
        "order" : {
            "type" : "array",
            "items" : {
                "$ref" : "https://developers.beckn.org/fnb/schema/0.7.1/fnb_item.json#properties/id"
            } 
        },
        "offers" : {
            "type" : "array",
            "items" : {
                "$ref" : "https://developers.beckn.org/core/schema/0.7.1/offer.json"
            }
        }
    }
}
```