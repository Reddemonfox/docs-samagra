```json
{
    "$id": "https://developers.beckn.org/fnb/schema/0.7.1/cuisine.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the cuisine served by a kitchen",
    "type": "object",
    "properties": {
        "category" : {
            "type" : "object",
            "properties": {
                "descriptor" : {
                    "$ref" : "https://developers.beckn.org/core/schema/0.7.1/descriptor.json"
                },
                "sub_categories" : {
                    "type" : "array",
                    "items" : {
                        "$ref" : "https://developers.beckn.org/core/schema/0.7.1/cuisine.json"
                    }
                }
            }
        }
    }
}
```