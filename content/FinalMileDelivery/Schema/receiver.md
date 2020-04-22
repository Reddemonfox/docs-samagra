```json
{
    "$id": "https://developers.beckn.org/fmd/schema/0.7.1/receiver.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the receiver of a package",
    "type": "object",
    "properties": {
        "personal_info" : {
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