The agent responsible for fulfillment of an FMD task.

**Namespace** : fmd

**Type** : FmdAgent

## JSON Schema
```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_agent.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a delivery agent",
    "allOf": [
        {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/operator.json"
        }
    ]
}
``` 