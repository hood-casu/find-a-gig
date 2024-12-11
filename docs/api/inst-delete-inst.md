---
layout: page
---

# DELETE an instrumentalist

## Base endpoint

```shell
{base_url}/instrumentalist
```

## Description

Use this call to delete an existing instrumentalist profile with the instrumentalist ID.

## Parameters

```shell
{base_url}/instrumentalist/{profile ID number}
```

| Parameter | Type | Description |
| --- | --- | --- |
| id | integer | Identification number assigned to a users instrumentalist or vocalist profile upon creation.|

## Request example

```curl
curl --location --request DELETE 'http://localhost:3000/instrumentalist/6'
```

## Verify request

Determine the success of the request by sending a [GET all instrumentalist](api/inst-get-all-inst/) call and verifying the specified profile is no longer part of the database.
