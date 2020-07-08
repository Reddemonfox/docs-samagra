```json
{
    "$id": "https://schema.beckn.org/fmd/schema/0.7.1/delivery_service.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes contents of the delivery service object",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "delivery_catalog" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/catalog.json"
        },
        "matched_items" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/core/schema/0.7.1/item.json#/properties/id"
            } 
        },
        "selected_items" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/core/schema/0.7.1/item.json#/properties/id"
            }
        },
        "offers" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/core/schema/0.7.1/offer.json"
            }
        },
        "provider" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/provider.json"
        },
        "delivery" : {
            "$ref" : "https://schema.beckn.org/fmd/schema/0.7.1/delivery.json"
        },
        "policies" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/core/schema/0.7.1/policy.json"
            }
        },
        "billing_address" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/location.json"
        }
    }
}
```