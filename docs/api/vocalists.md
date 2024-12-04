---
layout: page
---

# `vocalists` resource

Base endpoint

```shell
{base-url}/vocalists
```

## Resource properties

Sample `vocalists` resource

``` shell

{
    "last_name": "Johnson",
    "first_name": "Anya",
    "email": "anya@example.com",
    "phone_number": "202-555-7853",
    "experience_level": "intermediate",
    "location": "California",
    "preferred_genre": "pop",
    "gig_type": "one-time",
    "id": 1  
}
```

| Properties | Type | Description |
|--- | --- | ---|
| last_name | string | Surname of the vocalist.|
| first_name | string | First name of the vocalist.|
| email | string | Email address for the vocalist.|
| phone_number | string | Vocalist's phone number. |
| experience_level | string | Vocalist's self-reported experience level as a vocalist.|
| location | string | Vocalist's self-reported location or area in which they can gig.|
| preferred_genre | string | Vocalist's preferred music genre for gigs.|
| gig_type | string | Vocalist's preference for frequency of gigs.|
| id | number | Identification number assigned to the vocalist upon adding their profile to the Find-a-gig API.|

## Related pages

* [ADD a vocalist](../tutorials/add-a-vocalist.md)
* [GET all vocalists](../api/vocalists-get-all-vocalists.md)
* [Instrumentalists resource](../api/instrumentalists.md)