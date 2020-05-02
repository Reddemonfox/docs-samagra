```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/telehealth_app.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description" : "Describes a telehealth end user app",
    "type": "object",
    "properties": {
        "registration": {
            "type": "string"
        },
        "phone": {
            "type": "string"
        },
        "email": {
            "type": "string"
        },
        "address": {
            "$ref": "https://schema.beckn.org/core/schema/0.7.1/location.json"
        },
        "documents": {
            "type": "array",
            "items": {
                "type": "string"
            }
        },
        "apiendpoints": {
            "type": "array",
            "items": {
                "type": "object",
                "properties": {
                    "api": {
                        "type": "string"
                    },
                    "endpoint": {
                        "$ref": "http://schema.beckn.org/core/schema/0.7.1/api.json"
                    }
                }
            }
        }
    }
}
```