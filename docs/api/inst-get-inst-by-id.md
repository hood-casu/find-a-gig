---
layout: page
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

Get a profile's ID number by sending a request to [Create an instrumentalist profile](api/inst-create-inst/) or sending a request for [GET all instrumentalists](api/inst-get-all-inst/).

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
| 200 | Success |  |
| 404 | Failed |  |
| ECONREFUSED | N/A | |
