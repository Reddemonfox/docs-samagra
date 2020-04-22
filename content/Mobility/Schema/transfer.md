```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/transfer.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the trip object, its types and links to other objects in a journey",
    "type": "object",
    "properties": {
        "mode" : {
            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/mode.json"
        },
        "route" : {
            "$ref": "http://schema.beckn.org/mobility/schema/0.7.1/route.json"
        }
    }
}
```