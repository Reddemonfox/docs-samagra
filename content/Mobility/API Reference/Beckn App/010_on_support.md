---
title: "On Support"
metaTitle: "Beckn for Developers"
metaDescription: "Documentation for developers of the Beckn ecosystem"
---

On Support
===================

>   Contact Support

Overview
--------

>   The BPP will send the support information to the BAP.

Request
-------

### URL

>   /on_support

### Method

>  *POST*

### Request Body Schema

|**Field**|**Type**|
|---------|--------|
|context*|[ContextForOn_support](/Mobility/Schema%20Reference/contextforon_support)|
|message| [MessageForOn_support](/Mobility/Schema%20Reference/messageforon_support) |
|error| [Error](/Mobility/Schema%20Reference/error) |

### Request Body Example

```
{
    "context": {
        "domain": "mobility",
        "country": "IND",
        "city": "std:080",
        "action": "on_support",
        "core_version": "0.9.1",
        "bap_id": "https://mock_bap.com/",
        "bap_uri": "https://mock_bap.com/beckn/",
        "bpp_id": "https://mock_bpp.com/",
        "bpp_uri": "https://mock_bpp.com/beckn/",
        "transaction_id": "1209849124",
        "message_id": "12341242343",
        "timestamp": "2021-03-23T10:00:40.065Z"
    },
    "message": {
        "phone": "+919898989898",
        "email": "support@example.com",
        "uri": "http://support.mock_bpp.com?order_id=trip_1"
    }
}
```

>   The support information of the BPP is returned

Response
--------

### Response Body Schema

|**Field**|**Type**|
|---------|--------|
|message*|{ [Ack](/Mobility/Schema%20Reference/ack) }|
|error| [Error](/Mobility/Schema%20Reference/error) |

### Response Body Example

```
{
  "message": {
    "ack": {
      "status": "ACK"
    }
  }
}
```

> Acknowldegement response

### Response Codes

| **Code**       | **Description** |
|----------------|-----------------|
| 200 | Acknowledgement of message received   |