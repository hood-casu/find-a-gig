---
layout: page
---

# `instrumentalists` resource

Base endpoint

```shell
{base-url}/instrumentalists
```

## Resource properties

Sample `instrumentalists` resource.

``` shell
{
    "last_name": "Johnson",
    "first_name": "Lily",
    "email": "ljohnson@example.com",
    "phone_number": "555-555-2741",
    "instrument": "guitar",
    "experience_level": "advanced",
    "location": "Texas",
    "preferred_genre": "blues",
    "gig_type": "one-time",
    "id": 2    
}
```

| Properties | Type | Description |
|--- | --- | ---|
| last_name | string | Surname of the instrumentalists.|
| first_name | string | First name of the instrumentalist.|
| email | string | Email address for the vocalist.|
| phone_number | string | Vocalist's phone number. |
| instrument | string | Instrumentalists preferred instrument for a gig.|
| experience_level | string | Instrumentalist's self-reported experience level as a vocalist.|
| location | string | Instrumentalists's self-reported location or area in which they can gig.|
| preferred_genre | string | Instrumentalist's preferred music genre for gigs.|
| gig_type | string | Instrumentalist's preference for frequency of gigs.|
| id | number | Identification number assigned to the instrumentalist upon adding their profile to the Find-a-gig API.|

## Related pages

* [CREATE an instrumentalist](inst-create-inst.md)
* [GET all instrumentalists](inst-get-all-inst.md)
* [Vocalist resource](vocalists.md)
