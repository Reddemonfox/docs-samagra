```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/query.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a logical query",
    "type": "object",
    "properties": {
        "operator" : {
            "type" : "string",
            "enum" : [ "OR", "AND" ]
          },
          "rules" : {
            "type" : "array",
            "items" : {
              "type" : "object",
              "properties" : {
                "condition" : {
                  "type" : "string",
                  "enum" : [ "IN", "NOT", "EQUAL" ]
                },
                "type" : {
                  "type" : "string"
                },
                "key" : {
                  "type" : "string"
                },
                "value" : {
                  "type" : "string"
                }
              }
            }
          }
    }
}
```