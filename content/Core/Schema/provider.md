```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/provider.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a provider",
    
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "name" : {
            "type" : "string"
        },
        "website" : {
            "type" : "string",
            "format" : "url"
        },
        "contact" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/contact.json"
        },
        "api" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/api.json"
        }
    }
}
```