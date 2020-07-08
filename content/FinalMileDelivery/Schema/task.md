# FMD Task

A pickup or drop event

**Namespace** : fmd

## JSON Schema
```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_task.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.7.0",
    "description": "Describes an FMD task",
    "type": "object",
    "properties": {
        "id": {
            "type": "string"
        },
        "parent_task_id" : {
            "$ref" : "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_task.json#/properties/id"
        },
        "state" : {
            "type" : "string",
            "enum": [ "AT-LOCATION", "EN-ROUTE" ]
        },
        "type" : {
            "type" : "string",
            "enum" : [ "PICKUP", "DROP", "RTO-PICKUP", "RTO-DROP" ]
        },
        "descriptor" : {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/descriptor.json"
        },
        "location" : {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/location.json"
        },
        "spoc" : {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/person.json"
        },
        "instructions": {
            "type": "array",
            "items" : {
                "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/descriptor.json"
            }
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
```