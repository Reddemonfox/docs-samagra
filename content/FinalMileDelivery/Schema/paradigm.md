Describes a paradigm

**Namespace** : fmd

**Type** : FmdParadigm


## JSON Schema
```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_paradigm.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.7.0",
    "description": "Describes a paradigm",
    "type": "object",
    "properties": {
        "id": {
            "type": "string"
        },
        "descriptor" : {
            "allOf": [
                {
                    "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/descriptor.json"
                },
                {
                    "properties": {
                        "code" : {
                            "type": "string",
                            "enum": [
                                "SINGLE-PICKUP-SINGLE-DROP",
                                "MULTI-PICKUP-SINGLE-DROP",
                                "SINGLE-PICKUP-MULTI-DROP",
                                "MULTI-PICKUP-MULTI-DROP"
                            ]
                        }
                    }
                }
            ]
        },
        "policy_id" : {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/policy.json#/properties/id"
        }
    }
}
```