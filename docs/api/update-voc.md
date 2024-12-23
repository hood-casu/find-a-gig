---
layout: page
title: UPDATE a vocalist
---

# UPDATE a vocalist

This request allows you to change specific information in a vocalist's profile.

## Base endpoint

```shell
{base_url}/vocalist
```

## Parameters

| Parameter | Type | Description |
| --- | --- | --- |
| id | integer | Identification number assigned to a users instrumentalist or vocalist profile upon creation.|

Get a profile's ID number by sending a request to [CREATE a vocalist](create-voc.md) or sending a request for [GET all vocalists](get-all-vocalists.md).

## Request example

```curl
curl --location --request PATCH 'http://localhost:3000/vocalist/6' \
--header 'Content-Type: application/json' \
--data '{
    "preferred_genre": "bluegrass"
}'
```

## Return body example

```json
{
    "last_name": "User",
    "first_name": "Test",
    "email": "testuser@example.com",
    "phone_number": "555-555-5555",
    "experience_level": "advanced",
    "location": "State",
    "preferred_genre": "bluegrass",
    "long_term_gig": true,
    "short_term_gig": true,
    "id": 6
}
```

## Related pages

* [CREATE a vocalist](create-voc.md)
* [GET all vocalists](get-all-voc.md)
* [Vocalist resource](vocalist.md)
