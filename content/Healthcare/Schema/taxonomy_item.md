```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/ack.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Describes a taxonomy item",
    "type": "object",
    "properties": {
        "taxonomy": {
            "$ref": "#/components/schemas/taxonomy"
        },
        "id": {
            "type": "string"
        },
        "taxonomyid": {
            "type": "string"
        },
        "taxonomy_term": {
            "type": "string"
        },
        "name": {
            "type": "string"
        },
        "value": {
            "type": "string"
        }
    }
}
```