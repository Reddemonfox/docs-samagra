```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/header.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Describes an Ack response",
    "type": "object",
    "properties": {
        "authtoken": {
            "type": "string"
        },
        "signature": {
            "type": "string"
        },
        "callbackurl": {
            "type": "string"
        },
        "caller": {
            "type": "object",
            "properties": {
                "type": {
                    "type": "string",
                    "enum": [
                        "provider",
                        "app",
                        "gateway"
                    ]
                },
                "id": {
                    "type": "string"
                }
            }
        }
    }
}
```