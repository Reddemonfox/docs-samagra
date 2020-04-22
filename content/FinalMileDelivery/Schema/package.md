```json
{
    "$id": "https://developers.beckn.org/fmd/schema/0.7.1/package.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the package object",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "contents" : {
            "type" : "array",
            "items" : {
                "type" : "string"
            }
        },
        "weight": {
            "type": "object",
            "properties": {
                "min": {
                    "type": "integer"
                 },
                "max": {
                    "type": "integer"
                },
                "unit": {
                    "type": "string"
                }
            }
        },
        "dimensions": {
            "type": "object",
            "properties": {
                "length": {
                    "type": "number"
                },
                "width": {
                    "type": "number"
                },
                "height": {
                    "type": "number"
                },
                "unit": {
                    "type": "string"
                }
            }
        }

    }
}
```    