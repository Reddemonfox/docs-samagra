Describes an item in a Package

**Namespace** : fmd

**Type** : FmdOrder


## JSON Schema
```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_order.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.0",
    "description": "Describes an FMD order",
    "allOf": [
        {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/order.json"
        },
        {
            "properties": {
                "agent" : {
                    "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_agent.json"
                },
                "vehicle" : {
                    "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/mobility/schema/0.8.0/mobility_vehicle.json"
                },
                "tasks" : {
                    "type" : "array",
                    "items": {
                        "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_task.json"
                    }
                },
                "packages" : {
                    "type" : "array",
                    "items": {
                        "allOf": [
                            {
                                "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_package.json"
                            },
                            {
                                "properties": {
                                    "state" : {
                                        "type" : "string",
                                        "enum": [ "READY", "PICKED-UP", "DROPPED" ]
                                    },
                                    "task_id" : {
                                        "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_task.json#/properties/id"
                                    },
                                    "created_at" : {
                                        "type" : "string",
                                        "format" : "date-time"
                                    },
                                    "updated_at" : {
                                        "type" : "string",
                                        "format" : "date-time"
                                    }
                                }
                            }
                        ]
                    }
                }
            }
        }
    ]    
}    
```