```json
{
    "$id": "https://developers.beckn.org/fmd/schema/0.7.1/delivery_intent.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the final mile delivery search intent",
    "type": "object",
    "properties": {
        "domain": {
            "$ref": "https://developers.beckn.org/core/schema/0.7.1/domain.json"
        },
        "pickup": {
            "$ref": "https://developers.beckn.org/core/schema/0.7.1/location.json"
        },
        "drop": {
            "$ref": "https://developers.beckn.org/core/schema/0.7.1/location.json"
        },
        "package_attrs": {
            "$ref" : "https://developers.beckn.org/fmd/schema/0.7.1/package.json"
        },
        "tags": {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/tags.json"
        }
    }
}
```