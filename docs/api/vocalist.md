---
layout: page
title: Vocalist resource
---

# `vocalist` resource

Base endpoint

```shell
{base-url}/vocalist
```

## Resource properties

Sample `vocalist` resource

``` json
{
    "last_name": "Johnson",
    "first_name": "Anya",
    "email": "anya@example.com",
    "phone_number": "202-555-7853",
    "experience_level": 4,
    "location": "California",
    "preferred_genre": "pop",
    "long-term-gig": true,
    "short-term-gig": false,
    "id": 1  
}
```

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
| id | number | Identification number assigned to the vocalist upon adding their profile to the Find-a-gig API.|

## Related pages

* [CREATE a vocalist](create-voc.md)
* [CREATE an instrumentalist](create-inst.md)
* [GET all instrumentalists](get-all-inst.md)
* [`instrumentalist` resource](instrumentalist.md)
