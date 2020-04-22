```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/route.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the route of a trip",
    "type": "object",
    "properties" : {
        "edge" : {
            "type" : "object",
            "properties" : {
                "endpoints" : {
                    "type" : "object",
                    "start" : {
                        "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/stop.json"
                    },
                    "stop" : {
                        "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/stop.json"
                    }
                },
                
                "path" : {
                    "type" : "string"
                },
                "duration" : {
                    "$ref" : "http://schema.beckn.org/core/schema/0.7.1/scalar.json"
                },
                "distance" : {
                    "$ref" : "http://schema.beckn.org/core/schema/0.7.1/scalar.json" 
                }
            }
        },
        "stops" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/stop.json"
            }
        }
    }
}
```