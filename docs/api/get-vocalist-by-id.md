---
layout: page
title: GET vocalists by ID
---

# GET vocalists by ID

Get the profile of a single vocalist by using the profile's unique ID number.

## Base endpoint

```shell
{base_url}/vocalist
```

## Parameters

| Parameter | Type | Description |
| --- | --- | --- |
| id | integer | Identification number assigned to a users instrumentalist or vocalist profile upon creation.|

Get a profile's ID number by sending a request to [Create a vocalist profile](api/voc-create-voc/) or sending a request for [GET all vocalists](api/voc-get-all-vocalists/).

## Request example

```curl
curl --location 'http://localhost:3000/vocalist/6'
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
    "preferred_genre": "blues",
    "long_term_gig": false,
    "short_term_gig": true,
    "id": 6
}
```

## Return status

| Status Value | Return Status | Indicates |
| --- | --- | --- |
| 200 | Success | Data requested returned successfully |
| 404 | Failed | Vocalist record not found |
| ECONREFUSED | N/A | Service is offline. Start the service and try again. |

## Related pages

* [CREATE a vocalist](create-voc.md)
* [GET all instrumentalists](get-all-inst.md)
* [GET all instrumentalists by id](get-inst-by-id.md)
* [Vocalist resource](vocalist.md)
