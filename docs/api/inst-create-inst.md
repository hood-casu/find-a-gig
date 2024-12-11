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

None

## Payload

The following defines the optional payload items that can be added to the instrumentalist profile upon creation.

| Properties | Type | Description |
|--- | --- | ---|
| last_name | string | Surname of the instrumentalists.|
| first_name | string | First name of the instrumentalist.|
| email | string | Email address for the vocalist.|
| phone_number | string | Vocalist's phone number. |
| instrument | string | Instrumentalist's preferred instrument for a gig.|
| experience_level | integer | On a scale of 1 to 5, an instrumentalist's self-reported experience level as an instrumentalist. One indicates beginner proficiency, and 5 indicates advanced proficiency.|
| location | string | Instrumentalists's self-reported location or area in which they can gig.|
| preferred_genre | string | Instrumentalist's preferred music genre for gigs.|
| long_term_gig | boolean | Instrumentalist's preference for frequency of gigs.|
| short_term_gig | boolean | Instrumentalist's preference for frequency of gigs.|

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
