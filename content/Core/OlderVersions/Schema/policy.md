```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/policy.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a policy",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "type" : {
            "type" : "string",
            "enum" : ["CONFIRMATION_POLICY", "PAYMENT_POLICY", "CANCELLATION_POLICY", "REFUND_POLICY"]
        },
        "parent_policy_id" : {
            "type" : "string",
            "default" : null
        },
        "heading" : {
            "type" : "string"
        },
        "terms" : {
            "type" : "array",
            "items" : {
                "type" : "object",
                "properties": {
                    "id" : {
                        "type" : "string"
                    },
                    "name" : {
                        "type" : "string"
                    },
                    "description" : {
                        "type" : "string"
                    }
                }
            }
        }
        
    }
}
```