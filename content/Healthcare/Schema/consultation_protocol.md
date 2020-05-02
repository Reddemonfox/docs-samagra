```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/consultation_protocol.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Describes the tele consultation communication protocol",
    "type": "object",
    "properties": {
        "userverification": {
            "type": "object",
            "properties": {
                "required": {
                    "type": "boolean"
                },
                "responsible": {
                    "$ref": "#/components/schemas/networkside"
                }
            }
        },
        "preconsult": {
            "type": "object",
            "properties": {
                "required": {
                    "type": "boolean"
                },
                "responsible": {
                    "$ref": "#/components/schemas/networkside"
                }
            }
        }
    }
}
```