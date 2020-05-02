```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/consultation_type.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Describes a consultation type",
    "type": "object",
    "properties": {
        "type": {
            "type": "string",
            "enum": [
                "tele",
                "physical"
            ]
        },
        "subtype": {
            "type": "string",
            "enum": [
                "followup",
                "referral",
                "firstvisit",
                "secondopinion",
                "preliminary"
            ]
        }
    }
}
```