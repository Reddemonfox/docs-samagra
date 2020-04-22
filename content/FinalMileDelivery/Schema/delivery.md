```json
{
    "$id": "https://developers.beckn.org/mobility/schema/0.7.1/trip.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the trip object, its types and links to other objects in a journey",
    "type": "object",
    "properties": {
            "id" :{
                "type" : "string"
            },
            "delivery_agent" : {
                "$ref" : "https://developers.beckn.org/final-mile-delivery/schema/0.7.1/delivery_agent.json"
            },
            "tracking" : {
                "$ref" : "https://developers.beckn.org/mobility/schema/0.7.1/tracking.json"
            },
            "state" : {
                "$ref" : "https://developers.beckn.org/core/schema/0.7.1/state.json"
            },
            "charge" : {
              "$ref" : "https://developers.beckn.org/core/schema/0.7.1/price.json"
            },
            "route" : {
                "$ref": "https://developers.beckn.org/mobility/schema/0.7.1/route.json"
            },
            "rating" : {
                "$ref" : "https://developers.beckn.org/core/schema/0.7.1/rating.json"
            },
            "packages" : {
                "type" : "array",
                "items" : {
                    "$ref" : "https://developers.beckn.org/final-mile-delivery/schema/0.7.1/package.json"
                }
            }
    }
}
```