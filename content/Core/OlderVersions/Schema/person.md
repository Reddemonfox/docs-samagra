```json
{
    "$id": "http://schema.beckn.org/core/schema/0.7.1/person.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a person",
    "type": "object",
    "properties": {
        "title": {
            "type": "string",
            "enum": ["Mr", "Mrs", "Miss", "Dr"]
        },
        "first_name": {
            "type": "string"
        },
        "middle_name": {
            "type": "string"
        },
        "last_name": {
            "type": "string"
        },
        "full_name": {
            "type": "string"
        },
        "image": {
            "type": "object",
            "properties" : {
                "format" : {
                    "type" : "string",
                    "enum" : [ "url", "encoded" ]
                },
                "data" : {
                    "type" : "string"
                }
            }
        },
        "dob": {
            "type": "string",
            "format" : "date"
        },
        "gender" : {
            "type" : "string",
            "enum" : [ "male", "female" ]
        },
        "contact" : {
            "type": "object",
            "properties": {
                "email" : {
                    "type" : "string",
                    "format" : "email"
                },
                "mobile" : {
                    "type" : "object",
                    "properties": {
                        "country_code" : {
                            "type" : "string"
                        },
                        "number" : {
                            "type" : "string"
                        }
                    }
                },
                "landline" : {
                    "type" : "object",
                    "properties": {
                        "country_code" : {
                            "type" : "string"
                        },
                        "std_code" : {
                            "type" : "string"
                        },
                        "number" : {
                            "type" : "string"
                        },
                        "extension" : {
                            "type" : "string"
                        }
                    }
                },
                "ivr" : {
                    "type" : "array",
                    "items" : {
                        "type" : "string"
                    }
                }
            }
        }
    }
}
```