---
layout: page
title: GET all instrumentalists
---

# GET all instrumentalists

Get a list of all the instrumentalists in the Find-a-gig API.

## Base endpoint

```shell
{base_url}/instrumentalist
```

## Parameters

None

## Request example

```curl
curl --location 'http://localhost:3000/instrumentalist'
```

## Return body example

```json
[
    {
        "last_name": "Beverly",
        "first_name": "Levi",
        "email": "levi.bev.md@gmail.com",
        "phone_number": "443-555-1347",
        "instrument": "drums",
        "experience_level": 5,
        "location": "Maryland",
        "preferred_genre": "metal",
        "long-term-gig": true,
        "short-term-gig": false,
        "id": 1
    },
    {
        "last_name": "Johnson",
        "first_name": "Lily",
        "email": "ljohnson512@gmail.com",
        "phone_number": "512-555-2741",
        "instrument": "guitar",
        "experience_level": 5,
        "location": "Texas",
        "preferred_genre": "blues",
        "long-term-gig": false,
        "short-term-gig": true,
        "id": 2
    },
    ...
]
```

## Return status

| Status Value | Return Status | Indicates |
| --- | --- | --- |
| 200 | Success | Data requested returned successfully |
| ECONREFUSED | N/A | Service is offline. Start the service and try again. |

## Related pages

* [CREATE a vocalist](create-voc.md)
* [GET all instrumentalists](get-all-inst.md)
* [Vocalist resource](vocalist.md)
