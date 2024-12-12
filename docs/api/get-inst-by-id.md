---
layout: page
title: GET instrumentalists by ID
---

# GET instrumentalists by ID

This call will return a single instrumentalist by the assigned ID number.

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
curl --location 'http://localhost:3000/instrumentalist/6'
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
    "location": "Maryland",
    "preferred_genre": "metal",
    "long-term-gig": true,
    "short-term-gig": false,
    "id": 6
}
```

## Return status

| Status Value | Return Status | Indicates |
| --- | --- | --- |
| 200 | Success | Data requested returned successfully |
| 404 | Failed | Instrumentalist record not found |
| ECONREFUSED | N/A | Service is offline. Start the service and try again. |

## Related pages

* [CREATE a vocalist](create-voc.md)
* [GET all instrumentalists][def2]
* [Vocalist resource](vocalist.md)

[def]: create-inst.md
[def2]: get-all-inst.md