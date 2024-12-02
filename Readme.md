# Automation Guide for Postman and Newman

**Author:** Aleksandr Mironov  
**Role:** Manual QA at Keep-Calm digital agency

## 0. BUGS

| Bug ID | Description                                                                                                                                                            |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| API-01 | Error 500 occurs when attempting to delete an existing user.                                                                                                           |
| API-02 | Actual result: All games are returned, including the one with the exact title. Expected result: Only the game with the exact title should be included in the response. |
| API-03 | Actual result: The nickname is not created. Expected result: All required fields should be created correctly.                                                          |
| API-04 | Undefined                                                                                                                                                              |
| API-05 | The user has an empty space in their wishlist, but it's impossible to add a new item due to a 422 Error.                                                               |
| API-06 | The offset parameter is not working as expected. When used, all users are included in the response.                                                                    |
| API-07 | Unable to retrieve a user with valid credentials.                                                                                                                      |
| API-08 | The item is not removed from the wishlist as expected.                                                                                                                 |
| API-09 | Error 404 occurs when making a request with valid `game_uuids`.                                                                                                        |
| API-10 | The `category_UUID` in the games does not match the requested category.                                                                                                |
| API-11 | The avatar URL is not saved in the database. It appears after the file is uploaded, but disappears when checking the "get user" endpoint.                              |
| API-12 | The total order sum is always displayed as 0.                                                                                                                          |
| API-13 | The items list is empty when changing an item in the cart.                                                                                                             |
| API-14 | Undefined                                                                                                                                                              |
| API-15 | The "clear" endpoint does not clear the item list as expected.                                                                                                         |
| API-16 | It is possible to create a new order with duplicate items in the list. Expected result: A 400 error should be returned.                                                |
| API-17 | The `limit` parameter is ignored by the endpoint.                                                                                                                      |
| API-18 | The endpoint does not update the status to "canceled" as expected.                                                                                                     |
| API-19 | The endpoint does not update the status to "canceled" as expected.                                                                                                     |
| API-20 | Undefined                                                                                                                                                              |
| API-21 | The total value is 0, which does not match the sum of the user's items.                                                                                                |
| API-22 | Error 500 ("Internal server error") occurs when trying to create a new user. The user is not created.                                                                  |
| API-23 | Despite using different `user_uuid` values, the same response (for the first user) is returned.                                                                        |
| API-24 | Unable to log in with email and password after updating the user.                                                                                                      |
| API-25 | The added item does not appear in the database when fetching the user's wishlist via the "get user's wishlist" endpoint.                                               |

All automation has been created in Postman with Newman.

To run the automation, you have two options:

- **Use Postman to run collections**
- **Install Newman to your local computer to run tests**

## 1. Using Postman

### Steps to Run Automation Using Postman:

1. Open Postman.
2. Drag and drop all files from the repository `/data` into Postman.
3. Choose the appropriate environment from the dropdown in the top-right corner.
4. Click **Run** to start the collection.

---

This guide should help you get the automation up and running using Postman. Let me know if you need further assistance!

# Getting Started with Newman

Newman is a command-line tool that allows you to run Postman collections. This guide will walk you through installing and using Newman.

## 1. Install Node.js and npm

Newman is a Node.js package, so you need to have Node.js and npm (Node Package Manager) installed on your computer.

- Go to the [Node.js download page](https://nodejs.org/).
- Download and install the **LTS** version for your operating system (Windows, macOS, or Linux).
- After installation, verify that Node.js and npm are installed by running the following commands in your terminal:

  ```bash
  node -v
  npm -v
  ```

## 2. Install Newman

Once Node.js and npm are installed, you can install **Newman** globally on your system.

- Open a terminal (or Command Prompt on Windows) and run:

  ```bash
  npm install -g newman
  ```

This will install Newman globally, allowing you to use it from anywhere on your system.

## 3. Verify Installation

To verify that Newman is installed correctly, run the following command:

```bash
newman -v
```

## 4. Run a Postman Collection with Newman

Once you have Newman installed, you can run Postman collection from the command line.

run the following command in your terminal:

    ```bash
    newman run path/to/your/postman_collection.json -e path/to/your/postman_environment.json -g path/to/your/postman_globals.json
    ```

## 5 Here are all command for RELEASE (PROD) / DEV

## 5.1

      ```bash

    newman run data/collections/api-01_Delete_a_user.postman_collection.json -e data/environments/PROD.postman_environment.json - g data/globals/workspace.postman_globals.json

    newman run data/collections/api-01_Delete_a_user.postman_collection.json -e data/environments/DEV.postman_environment.json - g data/globals/workspace.postman_globals.json

    ```

## 5.1

      ```bash

    newman run data/collections/api-01_Delete_a_user.postman_collection.json -e data/environments/PROD.postman_environment.json - g data/globals/workspace.postman_globals.json

    newman run data/collections/api-01_Delete_a_user.postman_collection.json -e data/environments/DEV.postman_environment.json - g data/globals/workspace.postman_globals.json

    ```

newman run data/collections/api-01_Delete_a_user.postman_collection.json -e data/environments/DEV.postman_environment.json -g data/globals/workspace.postman_globals.json

newman run data/collections/api-01_Delete_a_user.postman_collection.json -e data/environments/PROD.postman_environment.json -g data/globals/workspace.postman_globals.json

newman run data/collections/api-11_Update_users_avatar.postman_collection.json -e data/environments/PROD.postman_environment.json -g data/globals/workspace.postman_globals.json
