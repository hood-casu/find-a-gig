---
layout: page
---

# CREATE instrumentalist

## Base endpoint

```shell
{base_url}/instrumentalist
```

## Description

Using this API call, you can create a new instrumentalist resource and receive a resource ID associated with the instrumentalist profile. 

## Parameters


## Request example

``` curl
curl --location 'http://localhost:3000/instrumentalist' \
--header 'Content-Type: application/json' \
--data-raw '{
        "last_name": "User",
        "first_name": "Test",
        "email": "testuser@example.com",
        "phone_number": "555-555-5555",
        "instrument": "drums",
        "experience_level": 3,
        "location": "Maryland",
        "preferred_genre": "metal",
        "long-term-gig": true,
        "short-term-gig": false
}'
```

## Return body example

The return should include all the information included in the request as well as a newly assigned profile ID number.

``` json
{
    "last_name": "User",
    "first_name": "Test",
    "email": "testuser@example.com",
    "phone_number": "555-555-5555",
    "instrument": "drums",
    "experience_level": 3,
    "location": "Maryland",
    "preferred_genre": "metal",
    "long-term-gig": true,
    "short-term-gig": false,
    "id": 6
}
```