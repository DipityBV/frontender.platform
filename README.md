# Frontender Platform

Frontender is a front-end solution for API driven website architecture. Read more about Frontender on our website [https://getfrontender.com](https://getfrontender.com)


[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)
[![Version](https://img.shields.io/badge/Stable-v2.1.2-FFE550)](https://github.com/getfrontender/frontender.desktop/releases/latest)
[![Version](https://img.shields.io/badge/Dev-v2.2.0a1-ff7bb5)](https://github.com/getfrontender/frontender.desktop/releases/tag/v2.2.a1)



## Table of content
- [Server Requirements](https://github.com/getfrontender/frontender.platform#server-requirements)
- [Pre-requisites](https://github.com/getfrontender/frontender.platform#pre-requisites)
- [Creating your first project](https://github.com/getfrontender/frontender.platform#creating-your-first-project)
- [Updating controls](https://github.com/getfrontender/frontender.platform#updating-controls)
- [Updating blueprints](https://github.com/getfrontender/frontender.platform#updating-blueprints)

## Server Requirements
- PHP 7.1 or higher
- PHP MongoDB extension
- PHP Zip extension
- PHP GD extension
- Composer
- MongoDB

## Pre-requisites

### Prepare a functional Mongo DB instance.
Install Mongo DB. You can create a database or have the installer do it for you.

### Register a (free) Frontender account
Visit https://getfrontender.com and register your free account.

### Request a project token
Register a new project by sending your project domain and the email you used for your registration to create-project@getfrontender.com.

## Creating your first project

### Step 1. Install Frontender Platform

Create a file `install.json`. You can use the `install.json-preset` we have provided as a template: `cp install.json-preset install.json`. It should contain the following:
```json
{
  "token": "###",
  "mongo_host": "mongodb+srv://#USERNAME#:#PASSWORD#@#DOMAIN#:#PORT#",
  "mongo_dbname": ""
}
```

Run the following from the commandline: `composer install`. Frontender Platform will now run a sequence of install commands to set up the database and import a barebones structure for further development.

### Step 2. Setup your hosts file

Next, setup your hosts file. The implementation will differ depending on your server or development setup, but basically you just need to make sure your server is pointing to the `public` folder for routing.

### Step 3. Import a project
Your installation now contains most the resources and dependencies, except for pages. You can create these manually, or import a barebones project to create your new project. Import a project by running:
```
composer run-script import-project https://github.com/getfrontender/frontender.project.stark/archive/master.zip
```

You can select any of the [Frontender prefab projects](https://github.com/getfrontender), or create your own.

**All done, you can now remove the `install.json` file.**

## Updating controls
To update all existing controls in your project you can run the command:  
```composer run-script import-project-controls```

## Updating blueprints
To update all existing blueprints in your project you can run the command:  
```composer run-script import-project-blueprints```

## Updating pages
To update all existing pages in your project you can run the command:  
```composer run-script import-project-pages```

## Debugging
Frontender Platform will also function with PHP MongoDB extensions version 1.5 and up, but this will require you to run the installer with the `--ignore-platform-reqs` flag.
