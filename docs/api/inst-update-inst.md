---
layout: page
---

# UPDATE an instrumentalist

## Base endpoint

```shell
{base_url}/instrumentalist
```

## Parameters

| Parameter | Type | Description |
| --- | --- | --- |
| id | integer | Identification number assigned to a users instrumentalist or vocalist profile upon creation.|

Get a profile's ID number by sending a request to [CREATE an instrumentalist profile][def] or sending a request for [GET all instrumentalists][def2].

## Request example

```curl
curl --location --request PATCH 'http://localhost:3000/instrumentalist/6' \
--header 'id: 6' \
--header 'Content-Type: application/json' \
--data '{

        "location": "Virginia"
    }'
```

## Return body example

```json
{
    "last_name": "User",
    "first_name": "Test",
    "email": "testuser@example.com",
    "phone_number": "555-555-5555",
    "instrument": "drums",
    "experience_level": 3,
    "location": "Virginia",
    "preferred_genre": "metal",
    "long_term_gig": false,
    "short_term_gig": false,
    "id": 6
}
```

## Related links

[def]: inst-create-inst.md
[def2]: inst-get-all-inst.md