```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/operator.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the operator of a service",
    "type": "object",
    "properties" : {
        "descriptor" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/person.json"
        },
        "experience" : {
            "label" : {
                "type" : "string"
            },
            "value" : {
                "type" : "string"
            },
            "unit" : {
                "type" : "string"
            }
        }

    }
}
```