---
title: "Confirm"
metaTitle: "Beckn for Developers"
metaDescription: "Documentation for developers of the Beckn ecosystem"
---

Confirm
===================

>   Confirms an order by agreeing to the terms of the order.

Overview
--------

>   The BAP will send the confirm request to the BPP after agreeing to the payment and fulfilment terms sent by the BPP.

Request
-------

### URL

>   /confirm

### Method

>  *POST*

### Request Body Schema

|**Field**|**Type**|
|---------|--------|
|context*|[ContextForContext](/Mobility/Schema%20Reference/contextforcontext)|
|message| [MessageForConfirm](/Mobility/Schema%20Reference/messageforconfirm) |

### Request Body Example

```
{
    "context": {
        "domain": "mobility",
        "country": "IND",
        "city": "std:080",
        "action": "confirm",
        "core_version": "0.9.1",
        "bap_id": "https://mock_bap.com/",
        "bap_uri": "https://mock_bap.com/beckn/",
        "bpp_id": "https://mock_bpp.com/",
        "bpp_uri": "https://mock_bpp.com/beckn/",
        "transaction_id": "1209849124",
        "message_id": "12341242345",
        "timestamp": "2021-03-23T10:00:40.065Z"
    },
    "message": {
        "order": {
            "items":[
                {
                    "id": "sedan_spot",
                    "quantity": {
                        "count": 1
                    }
                },
            ],
            "billing": {
                "name": "John Doe",
                "address": {
                    "door": "21A",
                    "name": "ABC Appartments",
                    "locality": "HSR Layout",
                    "city": "Bengaluru",
                    "state": "Karnataka",
                    "country": "India",
                    "area_code": "560102"
                },
                "email": "user@example.com",
                "phone": "+919876543210"
            },
            "fulfillment": {
                "tracking": true,
                "start": {
                    "location": {
                        "id": "user-location",
                        "descriptor": {
                            "name": "Current user location"
                        },
                        "gps": "12.9349377,77.6055586"
                    },
                    "instructions": {
                        "name": "pick up instructions",
                        "short_desc": "Ask doorman to ring 21A"
                    },
                    "time": {
                        "label": "ETA",
                        "duration": "P12M"
                    },
                    "contact": {
                        "phone": "+919999999999",
                        "email": "test@example.com"
                    }
                },
                "end": {
                    "location": {
                        "gps": "12.914028, 77.638698"
                    }
                }
            },
            "quote": {
                "price": {
                    "currency": "INR",
                    "value": "180"
                },
                "breakup": [
                    {
                        "title": "Sedan Spot Booking",
                        "price": {
                            "currency": "INR",
                            "value": "170"
                        }
                    },
                    {
                        "title": "Service Charge",
                        "price": {
                            "currency": "INR",
                            "value": "10"
                        }
                    }
                ]
            },
            "payment": {
                "uri": "https://api.bpp.com/pay?amt=$640&mode=upi&vpa=bpp@upi",
                "tl_method": "http/get",
                "params": {
                    "amount": "180",
                    "mode": "upi",
                    "vpa": "bpp@upi"
                },
                "type": "ON-FULFILMENT",
                "status": "NOT-PAID"
            }
        }
    }
}
```

>   Here the BAP confirms the order by agreeing to pay the amount on fulfilment.

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