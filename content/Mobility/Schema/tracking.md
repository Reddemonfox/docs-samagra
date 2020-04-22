```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/tracking.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the tracking object",
    "type": "object",
    "properties" : {
        "method" : {
            "type" : "string",
            "enum" : ["PULL", "PUSH"]
        },   
        "pull" : {
            "type" : "object",
            "properties" : {
                "data_url" : {
                    "type" : "string"
                },
                "embed_url" : {
                    "type" : "string"
                }
            }
        }
    }
}
```