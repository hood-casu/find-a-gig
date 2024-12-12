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

## Payload

The following table details the optional properties you can add to a vocalist profile.

| Properties | Type | Description |
|--- | --- | ---|
| last_name | string | Surname of the vocalist.|
| first_name | string | First name of the vocalist.|
| email | string | Email address for the vocalist.|
| phone_number | string | Vocalist's phone number. |
| experience_level | integer | On a scale of 1 to 5, an vocalist's self-reported experience level as a vocalist. One indicates beginner proficiency, and 5 indicates advanced proficiency.|
| location | string | Vocalist's self-reported location or area in which they can gig.|
| preferred_genre | string | Vocalist's preferred music genre for gigs.|
| long_term_gig | boolean | Vocalist's preference for frequency of gigs.|
| short_term_gig | boolean | Vocalist's preference for frequency of gigs.|

## Request example

``` curl
curl --location 'http://localhost:3000/vocalist' \
--header 'Content-Type: application/json' \
--data-raw '{
    "last_name": "User",
    "first_name": "Test",
    "email": "testuser@example.com",
    "phone_number": "555-555-5555",
    "experience_level": 3,
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

| id | number | Identification number assigned to the vocalist upon adding their profile to the Find-a-gig API.|

## Related pages

* [CREATE an instrumentalist](inst-create-inst.md)
* [GET all instrumentalists](inst-get-all-inst.md)
* [Vocalist resource](vocalists.md)
