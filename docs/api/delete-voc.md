---
layout: page
title: DELETE a vocalist
---

# DELETE a vocalist

Remove a vocalist's profile from the database by sending this request.

## Base endpoint

```shell
{base_url}/vocalist
```

## Parameters

```shell
{base_url}/vocalist/{profile ID number}
```

| Parameter | Type | Description |
| --- | --- | --- |
| id | integer | Identification number assigned to a users instrumentalist or vocalist profile upon creation.|

Get a profile's ID number by sending a request to [Create a vocalist profile](api/voc-create-voc/) or sending a request for [GET all vocalists](api/voc-get-all-vocalists/).

## Request example

```curl
curl --location --request DELETE 'http://localhost:3000/vocalist/6'
```

## Verify request

Determine the success of the request by sending a [GET all vocalist](api/voc-get-all-vocalists/) call and verifying the specified profile is no longer part of the database.

## Related pages

* [CREATE a vocalist](create-voc.md)
* [GET all instrumentalists](get-all-inst.md)
* [Vocalist resource](vocalist.md)