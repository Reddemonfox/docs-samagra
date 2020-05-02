```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/availability.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Describes the availability list of a service",
    "type": "object",
    "properties": {
        "slots": {
            "type": "array",
            "items": {
                "type": "object",
                "properties": {
                    "type": {
                        "type": "string",
                        "enum": [
                            "FREE",
                            "BUSY"
                        ]
                    },
                    "slot": {
                        "$ref": "http://schema.beckn.org/core/schema/0.7.1/scalar_range.json"
                    },
                    "item": {
                        "$ref": "http://schema.beckn.org/core/schema/0.7.1/item.json"
                    }
                }
            }
        }
    }
}
```