```json
{
    "$id": "https://schema.beckn.org/core/schema/0.7.1/rating.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the rating of a person or an object",
    "type": "object",
    "properties": {
        "value" : {
            "type" : "string"
        },
        "scale" : {
            "type" : "array",
            "items" : {
                "type" : "string"
            }
        }
    }
}
```