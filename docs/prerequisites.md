# Prerequisites
Use these steps to quickly set up your system so you can dive into using the Find-a-gig API.

These steps take about 30 minutes.

## Prerequisite steps

1. [Set up a GitHub account](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account#part-1-configuring-your-github-account).
2. Ensure your development system is running a current Mac, Windows, or Linux operating system.
3. Download or verify installation of the following software:
    * [Git](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git) 
    * [GitHub Desktop](https://github.com/apps/desktop) (optional)
    * A current or long-term support version of `node.js`
    * A current version of [json-server](https://www.npmjs.com/package/json-server)
    * [The Postman desktop](https://www.postman.com/downloads/) app.  
    **NOTE:** Testing the API will not work using the web version of Postman since you will use the same port to test the API that the web version would use to operate.

4. Create a fork of the Find-a-gig repo
5. Sync your fork of the find-a-gig-db.json file so you have the latest version.  
**TIP:** If you're using a fork of the repo, create a working branch in which to do your tutorials. Create a new branch for each tutorial to prevent a mistake in one from affecting your work in another.

## Test your setup
1. Create and checkout a test branch of your fork of the Find-a-gig API repo. Your `GitHub repo workspace` is the directory that contains your fork of the `find-a-gig` repo.
In a command line interface. 
```shell
    cd <your GitHub repo workspace>
    ls
    # (see the Find-a-gig API directory in the list)
    cd find-a-gig
    git checkout -b tutorial-test
    cd api
    json-server -w find-a-gig-db.json
```
If your development system is installed correctly, you should see
the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl http://localhost:3000/users
    ```

3. If the service is running correctly, you should see a list of users from the service, such as in this example.

    ```js
    [
        {
            "last_name": "Smith",
            "first_name": "Ferdinand",
            "email": "f.smith@example.com",
            "id": 1
        },
        {
            "last_name": "Jones",
            "first_name": "Jill",
            "email": "j.jones@example.com",
            "id": 2
        },
        ...
    ```

If you don't see the list of users, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of users from the service, you're ready to do
the [Tutorials](tutorials.md).