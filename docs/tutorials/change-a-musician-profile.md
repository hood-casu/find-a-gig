---
layout: default
title: Change a vocalist or instrumentalist profile
---

# Tutorial: Change a vocalist or instrumentalist profile

This tutorial shows you how to change a musician profile in the Find-a-gig database.

Expect this tutorial to take about 20 minutes.

## Prerequisites

Follow the steps on the [Prerequisites][def] page to prepare for this tutorial.

## How to add a vocalist profile

Use a PATCH request to update a musician profile.

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

Now that your json server is running, you are ready to change a musician profile in Postman or the command line with cURL.

### In Postman

1. In the Postman desktop app, create a new request.
2. Select the `PATCH` request.
3. Enter base URL for the API endpoint into the request field. It may look like the following if `http://localhost:3000/` is your base URL.

    ```shell
    http://localhost:3000/vocalist
    ```

    If you are changing an instrumentalist profile, it may look like this:

    ```shell
    http://localhost:3000/instrumentalist
    ```

4. Enter the profile ID parameter so you update the correct profile. If the ID for the profile is, "6," it looks like this:

   ```shell
    http://localhost:3000/vocalist/6
    ```

5. Select the **Body** tab then the **raw** radio button.
6. Enter the properties you would like to change in the profile.

    ```json
    {
    "location": "{updated location}",
    "short_term_gig": {updated boolean}
    }
    ```

7. Click the **Send** button and wait for the response.

### In cURL

1. In your terminal, enter your version of the following command:

    ```curl
    curl --location --request PATCH 'http://localhost:3000/vocalist/6' \
    --header 'Content-Type: application/json' \
    --data '{
        "location": "{updated location}",
        "short_term_gig": {updated boolean}
    }'
        ```

### Response example

If you correctly sent added a vocalist profile, you will receive a response containing all the profile properties with the new value(s) now showing.

```json
{
    "last_name": "User",
    "first_name": "Test",
    "email": "testuser@example.com",
    "phone_number": "555-555-5555",
    "experience_level": 4,
    "location": "{updated location}",
    "preferred_genre": "blues",
    "long_term_gig": false,
    "short_term_gig": {updated boolean},
    "id": 6
}
```

**Congratulations!** You've updated a musician profile in the Find-a-gig API database.

## Related pages

* [CREATE an instrumentalist](inst-create-inst.md)
* [GET all instrumentalists](inst-get-all-inst.md)
* [Vocalist resource](vocalists.md)


[def]: prerequisites.md
