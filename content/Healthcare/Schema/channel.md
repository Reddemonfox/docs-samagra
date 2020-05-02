```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/ack.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a communication channel",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "integer"
          },
          "name" : {
            "type" : "string",
            "enum" : [ "phone", "chat", "video", "audio", "physical" ]
          }
    }
}
```