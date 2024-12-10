---
layout: page
---

# CREATE a vocalist

## Base endpoint

```shell
{base_url}/vocalist
```

## Description

Using this API call, you can create a new vocalist resource and receive a resource ID associated with the vocalist profile.

## Parameters


## Request example

``` curl
curl --location 'http://localhost:3000/vocalist' \
--header 'Content-Type: application/json' \
--data-raw '{
    "last_name": "User",
    "first_name": "Test",
    "email": "testuser@example.com",
    "phone_number": "555-555-5555",
    "experience_level": "advanced",
    "location": "Texas",
    "preferred_genre": "blues",
    "gig_type": "one-time"  
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
    "instrument": "guitar",
    "experience_level": "advanced",
    "location": "State",
    "preferred_genre": "blues",
    "gig_type": "one-time",
    "id": 6
}
```