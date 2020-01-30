# Frontender Platform

Frontender is a front-end solution for API driven website architecture.

[https://getfrontender.com](https://getfrontender.com)

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

### Step 1. Create an install file
Create a file `install.json`. You can use the `install.json-preset` we have provided as a template: `cp install.json-preset install.json`. It should contain the following:
```json
{
  "project_token": ###,
  "mongodb_hoststring": "mongodb+srv://#USERNAME#:#PASSWORD#@#DOMAIN#:#PORT#",
  "mongodb_databasename": ""
}
```

### Step 2. Run the installation process
Run the following from the commandline: `composer install`. Frontender Platform will now run a sequence of install commands to set up the database and import a barebones structure for further development.

### Step 3. Import a project

Your installation now contains most the resources and dependencies, except for pages. You can create these manually, or import a barebones project to create your new project. Import a project by running:
```
composer run-script import-project https://github.com/getfrontender/frontender.project.stark.git
```

You can select any of the [Frontender prefab projects](https://github.com/getfrontender), or create your own.

### Step 4. Delete install.json

You’re done.

## Updating controls

To do.

## Updating blueprints

To do.