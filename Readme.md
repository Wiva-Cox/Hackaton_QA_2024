# Automation Guide for Postman and Newman

**Author:** Aleksandr Mironov  
**Role:** Manual QA at Keep-Calm digital agency

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
