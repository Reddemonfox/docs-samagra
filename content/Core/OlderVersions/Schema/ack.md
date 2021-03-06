```json

{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/ack.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the ACK response",
    "type": "object",
    "properties": {
        "context" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/context.json"
        },
        "body" : {
            "message" : {

            },
            "code" : {

            },
            "error" : {
                "type" : "array",
                "items" : {
                    "type" : "object",
                    "properties" : {
                        "path" : {
                            "type" : "string"
                        },
                        "error_msg" : {
                            "type" : "string"
                        }
                    }
                }

            }
        }
    }
}

```