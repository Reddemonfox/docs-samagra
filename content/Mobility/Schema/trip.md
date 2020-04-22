```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/trip.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a Trip",
    "type": "object",
    "properties": {
        "id" :{
            "type" : "string"
        },
        "vehicle" : {
            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/vehicle.json"
        },
        "driver" : {
            "type" : "object",
            "properties" : {
                "persona" : {
                    "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/driver.json"
                },
                "rating" : {
                    "$ref" : "http://schema.beckn.org/core/schema/0.7.1/rating.json"
                }
            }
        },
        "travellers" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/traveller.json"
            }
        },
        "tracking" : {
            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/tracking.json"
        },
        "corridor_type" : {
            "type" : "string",
            "enum" : ["FIXED","ON-DEMAND"]
        },
        "state" : {
            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/state.json"
                    }, 
        "fare" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/price.json"
        },
        "route" : {
            "$ref": "http://schema.beckn.org/mobility/schema/0.7.1/route.json"
        }
    }
}
```