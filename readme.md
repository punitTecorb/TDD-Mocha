## Write test cases using Mocha in Nodejs
## Introduction
TDD (Test Driven Approach) in node js. TDD by using mocha and chai..Mocha is a feature-rich JavaScript test framework running on Node.js and in the browser, making asynchronous testing simple and fun. Mocha tests run serially, allowing for flexible and accurate reporting, while mapping uncaught exceptions to the correct test cases`    

## Mocha
    Mocha is a feature-rich JavaScript test framework running on Node.js and in the browser.

## Chai
    Chai is a BDD / TDD assertion library for node and the browser that can be delightfully paired with any javascript testing framework.

## Test case demo 
describe('Admin Authentication ***********************************', () => {
    //lOGIN
    describe('Login-------------------', () => {
        it('login api', (done) => {
            request.post(base_url + "" + 'auth/login', {
                json: true, headers: { 'timezone': 'Asia/Kolkata' }, body: {
                    "password": "1234qww56",
                    "email": "admiqqn@gmail.com"
                }
            },
                function (err: any, body: any, res: any) {
                    expect(res.code).to.be.eq(OK);
                    expect(res.message).to.be.eq('success');
                    expect(res.data).to.have.property('token');
                    expect(res.data).to.have.property('role');
                    done();
                })
        })
    });

});

## Installation
    npm install
    yarn install

## DB Setup
    use mongodb so go to mongodb create the cluster and get the url from connection and add in .env file.
    DB_URL = "****"


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
