---
layout: default
title: Find an instrumentalist
---

# Tutorial: Find an instrumentalist

This tutorial shows you how to add a new vocalist profile to the Find-a-gig database.

Expect this tutorial to take about 20 minutes.

## Prerequisites

Follow the steps on the [Prerequisites][def] page to prepare for this tutorial.

## How to add a vocalist profile

Get a list of all the instrumentalists in the Find-a-gig API.

1. Verify your `json-server` is running.
2. In your terminal, navigate to the following directory:

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
3. Enter base URL for the API endpoint and the `instrumentalist` resource into the request field. It may look like the following if `http://localhost:3000/` is your base URL.

    ```shell
    http://localhost:3000/instrumentalist
    ```

4. Click the **Send** button and wait for the response.

### In cURL

1. In your terminal, enter your version of the following command:

    ```curl
    curl --location 'http://localhost:3000/instrumentalist'
    ```

### Response example

If you correctly sent added a vocalist profile, the response will look something like this:

    ```json
    [
    {
        "last_name": "Beverly",
        "first_name": "Levi",
        "email": "levi.bev.md@gmail.com",
        "phone_number": "443-555-1347",
        "instrument": "drums",
        "experience_level": 5,
        "location": "Maryland",
        "preferred_genre": "metal",
        "long-term-gig": true,
        "short-term-gig": false,
        "id": 1
    },
    {
        "last_name": "Johnson",
        "first_name": "Lily",
        "email": "ljohnson512@gmail.com",
        "phone_number": "512-555-2741",
        "instrument": "guitar",
        "experience_level": 5,
        "location": "Texas",
        "preferred_genre": "blues",
        "long-term-gig": false,
        "short-term-gig": true,
        "id": 2
    },
    ...
]
    ```

**Congratulations!** You've found an instrumentalist!

## Related pages

* [CREATE an instrumentalist](inst-create-inst.md)
* [GET all instrumentalists](inst-get-all-inst.md)
* [Vocalist resource](vocalists.md)

[def]: prerequisites.md

