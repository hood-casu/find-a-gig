---
layout: default
title: Find a musician by property
---

# Tutorial: Find a musician by profile property

This tutorial shows you how to find a musician profile with specific preferences in the Find-a-gig database.

Expect this tutorial to take about 20 minutes.

## Prerequisites

Follow the steps on the [Prerequisites][def] page to prepare for this tutorial.

## How to add a vocalist profile

Use a GET request with parameters to find a musician with specific profile preferences.

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

Now that your json server is running, you are ready to find a musician profile in Postman or the command line with cURL.

### In Postman

1. In the Postman desktop app, create a new request.
2. Select the `GET` request.
3. Enter base URL for the API endpoint into the request field. It may look like the following if `http://localhost:3000/` is your base URL.

    ```shell
    http://localhost:3000/vocalist
    ```

    If you want to find an instrumentalist profile, it may look like this:

    ```shell
    http://localhost:3000/instrumentalist
    ```

4. Select the **Params** tab.
5. In the Keys field enter the parameter and value by which you want to search. Example:

    | Key | Value |
    | --- | --- |
    | long_term_gig | true |

6. Click the **Send** button and wait for the response.

### In cURL

1. In your terminal, enter your version of the following command:

    ```curl
    curl --location 'http://localhost:3000/instrumentalist?long_term_gig=true' \
    --data ''
    ```

### Response example

If you correctly sent the request with parameters, you will receive a response containing all the profiles in the Find-a-gig API that have key values matching your parameters.

```json
{
    "last_name": "User",
    "first_name": "Test",
    "email": "testuser@example.com",
    "phone_number": "555-555-5555",
    "preferred_instrument": "drums"
    "experience_level": 4,
    "location": "Texas",
    "preferred_genre": "blues",
    "long_term_gig": true,
    "short_term_gig": false,
    "id": 6
}
```

**Congratulations!** You've found a musician!

## Related pages

* [Add an instrumentalist profile](add-an-inst-profile.md)
* [Add a vocalist profile](add-a-vocalist-profile.md)
* [Find an instrumentalist](find-an-inst.md)
* [Find a vocalist](find-a-vocalist.md)
* [Change a musician profile](change-a-musician-profile.md)


[def]: prerequisites.md