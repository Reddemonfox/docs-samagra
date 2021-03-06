```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/scalar.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "An object representing the range of a scalar quantity",
    "type": "object",
    "properties": {
        "min" : {
            "type" : "number"
        },
        "max" : {
            "type" : "number"
        },
        "unit" : {
            "type" : "string"
        }
    }
}
```