---
layout: page
---

# GET all instrumentalists

## Base endpoint

```shell
{base_url}/instrumentalist
```

## Description

Get a list of all the instrumentalists in the Find-a-gig API.

## Parameters

None

## Request example

```curl
curl --location 'http://localhost:3000/instrumentalist'
```

## Return body example

```
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