```json
{
    "$id": "https://developers.beckn.org/fmd/schema/0.7.1/sender.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the sender of a package",
    "type": "object",
    "properties": {
        "descriptor" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/person.json"
        },
        "rating" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/rating.json"
        },
        "location" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/location.json"
        }    
    }
}
```