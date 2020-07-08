```json
{
    "$id": "https://schema.beckn.org/fmd/schema/0.7.1/delivery_intent.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the final mile delivery search intent",
    "type": "object",
    "properties": {
        "domain": {
            "$ref": "https://schema.beckn.org/core/schema/0.7.1/domain.json"
        },
        "pickup": {
            "$ref": "https://schema.beckn.org/core/schema/0.7.1/location.json"
        },
        "drop": {
            "$ref": "https://schema.beckn.org/core/schema/0.7.1/location.json"
        },
        "package_attrs": {
            "$ref" : "https://schema.beckn.org/fmd/schema/0.7.1/package.json"
        },
        "tags": {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/tags.json"
        }
    }
}
```