---
layout: default
title: Find a vocalist
---

# Tutorial: Find a vocalist

This tutorial details get a list of all vocalists in the Find-a-gig API.

Expect this tutorial to take about 20 minutes.

## Prerequisites

Follow the steps on the [Prerequisites][def] page to prepare for this tutorial.

## How to add a vocalist profile

Use a GET request to receive a list of all vocalist profiles.

1. Verify your `json-server` is running.
2. In your command line or Git Bash tool, navigate to the following directory:

    ```curl
    cd {your GitHub repo workspace}/find-a-gig/
    git checkout -b {your tutorial branch}
    cd api
    ```

3. Enter the following command:

    ```curl
    json-server -w to-do-db-source.json
    ```

Now that your json server is running, you are ready to add a new profile in Postman or the command line with cURL.

### In Postman

1. In the Postman desktop app, create a new request.
2. Select the `GET` request.
3. Enter base URL for the API endpoint into the request field. It may look like the following if `http://localhost:3000/` is your base URL.

    ```shell
    http://localhost:3000/vocalist
    ```

4. Click the **Send** button and wait for the response.

### In cURL

1. In your terminal, enter your version of the following command:

    ```curl
    curl --location 'http://localhost:3000/vocalist'
    ```

### Response example

If you correctly sent added a vocalist profile, you will receive a list of all vocalist profiles in the database.

```json
[
    {
        "last_name": "Nguyen",
        "first_name": "Anya",
        "email": "anya.nguyen@gmail.com",
        "phone_number": "202-555-7853",
        "experience_level": 3,
        "location": "California",
        "preferred_genre": "pop",
        "long-term-gig": false,
        "short-term-gig": true,
        "id": 1
    },
    {
        "last_name": "Kim",
        "first_name": "Soo",
        "email": "soosingskim@gmail.com",
        "phone_number": "404-555-3429",
        "experience_level": 1,
        "location": "Georgia",
        "preferred_genre": "rock",
        "long-term-gig": true,
        "short-term-gig": false,
        "id": 2
    },
...
]
```

**Congratulations!** You've added a new vocalist profile to the Find-a-gig database.

## Related pages

* [CREATE an instrumentalist](inst-create-inst.md)
* [GET all instrumentalists](inst-get-all-inst.md)
* [Vocalist resource](vocalists.md)


[def]: prerequisites.md
