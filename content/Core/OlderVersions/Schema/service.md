```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/service.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes contents of the mobility service object",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "catalog" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/catalog.json"
        },
        "provider" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/provider.json"
        }
    }
}
```