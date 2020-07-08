Describes the search intent for final mile delivery

**Namespace** : fmd

**Type** : FmdIntent


## JSON Schema
```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_intent.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.0",
    "description": "Describes the final mile delivery search intent",
    "allOf": [
        {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/intent.json"
        },
        {
            "properties": {
                "pickups": {
                    "type" : "array",
                    "items" : {
                        "type" : "object",
                        "properties": {
                            "location" : {
                                "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/location.json"
                            },
                            "time" : {
                                "type" : "string",
                                "format" : "date-time"
                            }
                        }
                    }
                },
                "drops": {
                    "type" : "array",
                    "items" : {
                        "type" : "object",
                        "properties": {
                            "location" : {
                                "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/location.json"
                            },
                            "time" : {
                                "type" : "string",
                                "format" : "date-time"
                            }
                        }
                    }
                },
                "packages": {
                    "type" : "array",
                    "items" : {
                        "$ref" : "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_package.json"
                    }
                },
                "tags": {
                    "type" : "array",
                    "items": {
                        "$ref" : "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.7.1/tag.json"
                    }
                }
            }
        }
    ]
}
```