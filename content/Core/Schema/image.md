```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/image.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Image of an object",
    "type": "object",
    "properties": {
        "type" : {
            "type" : "string",
            "enum" : ["url", "data"]
        },
        "url" : {
            "type" : "string",
            "format" : "date-time"
        },
        "data" : {
            "type" : "string"
        }
    }
}
```
