---
layout: page
title: GET all vocalists
---

# GET all vocalists

Use this request to get a list of all vocalist profiles in the Find-a-gig database.

## Base endpoint

```shell
{base_url}/vocalist
```

## Parameters

None

## Request example

```curl
curl --location 'http://localhost:3000/vocalist'
```

## Return body example

```json
[
    {
        "last_name": "Nguyen",
        "first_name": "Anya",
        "email": "anya.nguyen@gmail.com",
        "phone_number": "202-555-7853",
        "experience_level": 3,
        "location": "California",
        "preferred_genre": "pop",
        "long-term-gig": false,
        "short-term-gig": true,
        "id": 1
    },
    {
        "last_name": "Kim",
        "first_name": "Soo",
        "email": "soosingskim@gmail.com",
        "phone_number": "404-555-3429",
        "experience_level": 1,
        "location": "Georgia",
        "preferred_genre": "rock",
        "long-term-gig": true,
        "short-term-gig": false,
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