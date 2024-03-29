## Test cases using Mocha in Nodejs with typescript

## Introduction
Test-driven development (TDD) is an evolutionary approach to development which combines test-first development where you write a test before you write just enough production code to fulfill that test and refactoring. In simple terms, test cases are created before code is written.

In this approach we are using Express as a backend server and mongo-db as a database.

For testing purposes we are using mocha & chais.

Mocha: Mocha is a feature-rich JavaScript test framework running on Node.js and in the browser, making asynchronous testing simple and fun.

Chai:Chai is a BDD / TDD assertion library for node and the browser that can be delightfully paired with any javascript 
testing framework.

What we have implemented in this project?
1. User login via email and password.

## Required dependencies:

Node is installed (v 16.16.0)

npm is installed (v 8.11.0)

mongodb is installed

Git is installed

## Prerequisites
Express

Understanding of rest api

Idea for working in backend technology.

## Create development.env to setup required environment variables

Go to the pre-start folder and env>development.env file directory

NODE_ENV=development

jwt_secret_key=""

MONGO_URI=""

## Api code
   Api path - src/controllers/admin/

## Test cases
   path - src/test

## Installing Dependencies
Express

Mongoose

Dotenv

Bcryptjs

Mocha: npm install mocha

Chai: npm install chai

Chai-http: npm install chai-http

## DB Setup
    use mongodb so go to mongodb create the cluster and get the url from connection and add in .env file.
    DB_URL = "****"

## Server
PORT=3009

HOST=localhost


## Setup Steps:
`npm install`
### local server
`npm run start:dev`
### install mocha
`npm i @types/mocha`
### install chai
`npm i @types/chai`
### install request
`npm i @types/request`
### use this script in package.json
`"test": "mocha -r ts-node/register src/test/**/*_spec.ts"`
### testing command
`npm test` // Run command in Terminal
