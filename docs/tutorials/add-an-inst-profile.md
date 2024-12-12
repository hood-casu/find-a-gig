---
layout: default
title: Add an instrumentalist profile
---
# Add an instrumentalist profile

This tutorial will provide steps for creating an instrumentalist profile in the Find-a-gig API.

Expect this tutorial to take about 20 minutes.

## Prerequisites

Follow the steps on the [Prerequisites][def] page to prepare for this tutorial.

## How to add an instrumentalist profile

Use a POST request to create a new instrumentalist profile.

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
2. Select the `POST` request.
3. Enter base URL for the API endpoint into the request field. It may look like the following if `http://localhost:3000/` is your base URL.

    ```shell
    http://localhost:3000/instrumentalist
    ```

4. Select the **Body** tab, the **raw** radio button.
5. Enter your version of the following into the text field:

    ```json
    {
    "last_name": "{instrumentalist last name}",
    "first_name": "{instrumentalist first name}",
    "email": "{instrumentalist email}",
    "phone_number": "555-555-5555",
    "experience_level": {number 1-5},
    "location": "{Location}",
    "preferred_genre": "{genre}",
    "long_term_gig": {boolean},
    "short_term_gig": {boolean}
    }
    ```
6. Click the **Send** button and wait for the response.

### In cURL

1. In your terminal, enter your version of the following command:

    ```curl
    curl --location 'http://localhost:3000/instrumentalist' \
    --header 'Content-Type: application/json' \
    --data-raw '{
        "last_name": "{instrumentalist last name}",
        "first_name": "{instrumentalist first name}",
        "email": "{instrumentalist email}",
        "phone_number": "{555-555-5555}",
        "instrument": "{instrument}",
        "experience_level": {number 1-5},
        "location": "{Location}",
        "preferred_genre": "{genre}",
        "long_term_gig": {boolean},
        "short_term_gig": {boolean}
    }'
    ```

### Response example

If you correctly sent added a instrumentalist profile, the response will look something like this:

    ```json
    {
        "last_name": "User",
        "first_name": "Test",
        "email": "testuser@example.com",
        "phone_number": "555-555-5555",
        "instrument": "drums",
        "experience_level": 4,
        "location": "State",
        "preferred_genre": "blues",
        "long_term_gig": false,
        "short_term_gig": true,
        "id": 6
    }
    ```
    
**TIP**: If you want to alter the information in the profile at any time, keep the ID number for the profile on hand so you can reference it later.

**Congratulations!** You've added a new instrumentalist profile to the Find-a-gig database.

## Related pages

* [CREATE an instrumentalist](inst-create-inst.md)
* [GET all instrumentalists](inst-get-all-inst.md)
* [Vocalist resource](vocalists.md)

