```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/doctor.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Describes the customer of a kitchen",
    "type": "object",
    "properties": {
        "doctorid": {
            "type": "string"
        },
        "signature": {
            "type": "string"
        },
        "isActive": {
            "type": "boolean"
        },
        "qualifications": {
            "type": "array",
            "items": {
                "type": "string"
            }
        },
        "supportedchannels": {
            "$ref": "#/components/schemas/channel"
        },
        "rating": {
            "$ref": "http://schema.beckn.org/core/schema/0.7.1/rating.json"
        },
        "item": {
            "$ref": "http://schema.beckn.org/core/schema/0.7.1/item.json"
        },
        "availability": {
            "type": "array",
            "items": {
                "$ref": "#/components/schemas/availability"
            }
        }
    }
}
```