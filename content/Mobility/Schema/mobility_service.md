```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/mobility_service.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes contents of the mobility service object",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "catalog" : {
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
        "fare_products" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/fare_product.json"
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
        "trip" : {
            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/trip.json"
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