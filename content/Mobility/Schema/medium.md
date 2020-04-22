```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/medium.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the medium of transportation used in a journey",
    "type": "object",
    "properties": {
        "type": {
                "type": "string",
                "enum": ["ROADWAY", "WATERWAY", "AIRWAY", "RAILWAY"]
        },
        "roadway": {
            "type": "object",
            "properties" : {
                "type" : {
                    "type" : "string",
                    "enum": ["HIGHWAY", "LOCAL-ROAD"]
                },
                "lanes" : {
                    "type" : "integer"
                },
                "oneway" : {
                    "type" : "boolean"    
                },
                "toll" : {
                    "type" : "object",
                    "properties" : {
                        "has_toll" : {
                            "type" : "boolean"
                        },
                        "fare" : {
                            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/price.json"

                        } 

                    },
                    "description" : "TODO: account for Fastag and other systems"
                }
            }
        },
        "waterway": {
            "type" : "object",
            "properties" : {
                "type" : {
                    "type" : "string",
                    "enum" : ["SEA", "RIVER", "LAKE"]
                }
            } 
        },
        "airway": {
            "type" : "object",
            "properties" : {
                "type" : {
                    "type" : "string",
                    "enum" : ["CIVILIAN", "MILITARY"]
                }
            } 
        },
        "railway": {
            "type" : "object",
            "properties" : {
                "type" : {
                    "type" : "string",
                    "enum" : ["NARROW-GAUGE", "METER-GAUGE", "BROAD-GAUGE"]
                }
            } 
        }    
    }
}
```