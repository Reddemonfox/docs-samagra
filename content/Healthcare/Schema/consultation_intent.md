```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/ack.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Defines the intent of the end user who is looking for a consultation",
    "type": "object",
    "properties": {
        "complaints": {
            "type": "array",
            "items": {
                "$ref": "#/components/schemas/taxonomyitem"
            }
        },
        "speciality": {
            "type": "string"
        },
        "type": {
            "$ref": "#/components/schemas/consultationtype"
        },
        "time_range": {
            "$ref": "http://schema.beckn.org/core/schema/0.7.1/scalar_range.json"
        },
        "location": {
            "$ref": "https://schema.beckn.org/core/schema/0.7.1/location.json"
        },
        "price_range": {
            "$ref": "http://schema.beckn.org/core/schema/0.7.1/scalar_range.json"
        },
        "providers": {
            "type": "array",
            "items": {
                "$ref": "http://schema.beckn.org/core/schema/0.7.1/provider.json#/properties/id"
            }
        },
        "doctors": {
            "type": "array",
            "items": {
                "$ref": "http://schema.beckn.org/core/schema/0.7.1/item.json#/properties/id"
            }
        },
        "rating_range": {
            "$ref": "http://schema.beckn.org/core/schema/0.7.1/scalar_range.json"
        },
        "languages": {
            "type": "array",
            "items": {
                "type": "string"
            }
        },
        "channel": {
            "$ref": "#/components/schemas/channel"
        },
        "clinical_summary": {
            "$ref": "#/components/schemas/clinicalnotes"
        },
        "person": {
            "$ref": "#/components/schemas/person"
        }
    }
}
```