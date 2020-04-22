```json

{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/api.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes contact info of a Person or Organization",
    "type": "object",
    "properties": {
        "url" : {
            "type" : "string"
        },
        "exp" : {
            "type" : "string",
            "format" : "date-time"
        }
    }
}

```