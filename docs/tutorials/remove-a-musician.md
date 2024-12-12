---
layout: default
title: Remove a musician profile
---

# Tutorial: Remove a musician profile

This tutorial shows you how to delete a profile from the Find-a-gig database.

Expect this tutorial to take about 20 minutes.

**CAUTION**: Deleting a profile will remove a profile from the Find-a-gig API forever. Consider [changing a profile's][def2] long_term_gig and short_term_gig properties to `false` before deleting a full profile in case you would like to take a break from gigs. If you want to proceed with profile deletion, please make sure you use the correct profile ID to complete this request.

## Prerequisites

Follow the steps on the [Prerequisites][def] page to prepare for this tutorial.

## How to add a vocalist profile

Use a POST request to create a new vocalist profile.

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
2. Select the `DELETE` request.
3. Enter base URL for the API endpoint into the request field. It may look like the following if `http://localhost:3000/` is your base URL.

    ```shell
    http://localhost:3000/vocalist
    ```

4. Enter the profile ID parameter for the profile you want to delete. If the you want to delete a vocalist and the ID for the profile is, "6," the request will look like this:

   ```shell
    http://localhost:3000/vocalist/6
    ```

**TIP**: You can verify you have the correct ID by [getting a list of all vocalists][def4] or [getting a list of all instrumentalists][def3].

1. Click the **Send** button and wait for the response.

### In cURL

1. In your terminal, enter your version of the following command:

    ```curl
    curl --location --request DELETE 'http://localhost:3000/vocalist/6'
    ```

### Response example

If you correctly sent added a vocalist profile, the response will look something like this:

```json
{}
```

**Congratulations!** You've removed a musician profile to the Find-a-gig database.

## Related pages

* [CREATE an instrumentalist](inst-create-inst.md)
* [GET all instrumentalists](inst-get-all-inst.md)
* [Vocalist resource](vocalists.md)


[def]: prerequisites.md
[def2]: change-a-musician-profile.md
[def3]: find-an-inst.md
[def4]: find-a-vocalist.md
