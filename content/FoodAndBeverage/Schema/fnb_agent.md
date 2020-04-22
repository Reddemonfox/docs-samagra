```json
{
    "$id": "https://developers.beckn.org/fnb/schema/0.7.1/fnb_agent.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the F&B agent in a restaurant",
    "type": "object",
    "properties": {
        "descriptor" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/person.json"
        },
        "rating" : {
            "$ref" : "https://developers.beckn.org/core/schema/0.7.1/rating.json"
        }    
    }
}
```