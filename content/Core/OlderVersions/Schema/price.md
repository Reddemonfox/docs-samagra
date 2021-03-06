```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/price.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the price of an item or service",
    "type": "object",
    "properties": {
        "currency": {
            "type": "string"
        },
        "estimated_value" : {
            "type": "number"
        },
        "computed_value" : {
            "type": "number"
        },
        "listed_value": {
            "type": "number"
        },
        "offered_value": {
            "type": "number"
        },
        "unit": {
            "type": "string"
        },
        "discount": {
            "type" : "number"
        },
        "tax" : {
            "type" : "object",
            "properties" : {
                "computed" : {
                    "type": "number"
                },
                "breakup" : {
                    "type" : "array",
                    "items" : {
                        "type" : "object",
                        "properties" : {
                            "line_item" : {
                                "type" : "string"
                            },
                            "amount" : {
                                "type" : "number"
                            }
                        }
                    }
                }
            }
        }
    }
}

```