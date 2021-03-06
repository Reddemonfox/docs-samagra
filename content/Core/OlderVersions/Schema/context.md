```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/context.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the beckn message packet context",
    "type": "object",
    "properties": {
        "domain" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/domain.json"
        },
        "action" : {
            "type" : "string"
        },
        "version" : {
            "type" : "string"
        },
        "ctx_id" : {
            "type" : "string"
        },
        "timestamp" : {
            "type" : "string",
            "format" : "date-time"
        }
    }
}

```