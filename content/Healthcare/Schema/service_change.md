```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/service_change.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Describes an Ack response",
    "type": "object",
    "properties": {
        "change_type": {
            "type": "string",
            "enum": [
                "reschedule",
                "cancel",
                "missed",
                "complete",
                "update"
            ]
        },
        "change_reason": {
            "type": "object",
            "properties": {
                "reason": {
                    "type": "string"
                },
                "additional_info": {
                    "type": "string"
                }
            }
        },
        "changed_properties": {
            "type": "array",
            "items": {
                "type": "string"
            }
        },
        "service": {
            "$ref": "#/components/schemas/consultationservice"
        }
    }
}
```