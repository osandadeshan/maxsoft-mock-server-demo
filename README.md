# MaxSoft Mock Server Demo
A simple mock API server using [Express.js](https://expressjs.com/) that is hosted on [Firebase](https://firebase.google.com/).

## Why custom mock server
You have full control of what API to define and what data to respond with with minimal coding.

## How it works
The APIs are defined via Express.js framework and served though Firebase cloud functions. All the defined API can be found at [functions/index.js](https://github.com/osandadeshan/maxsoft-mock-server-demo/blob/master/functions/index.js) and pre-loaded mock responses example can be found at [mock-responses](https://github.com/osandadeshan/maxsoft-mock-server-demo/tree/master/functions/mock-responses)

* References: https://expressjs.com/en/guide/routing.html

#### GET Routes
1. Hello! \
https://maxsoft-mock-server-demo.web.app/say/hello?name=Osanda

2. Get User Details \
https://maxsoft-mock-server-demo.web.app/users/1

3. Get large list of photos response from mocked JSON file \
https://maxsoft-mock-server-demo.web.app/photos

4. Get a single photo item from mocked JSON file \
https://maxsoft-mock-server-demo.web.app/photos/29647

#### POST Route
1. Register a new user \

**Success**
```
curl -X POST \
  https://maxsoft-mock-server-demo.web.app/register \
  -H 'Content-Type: application/json' \
  -d '{"userId": "myusername", "email":"my@email.com", "name": "New User"}'
```

**Fail**
```
curl -X POST \
  https://maxsoft-mock-server-demo.web.app/register \
  -H 'Content-Type: application/json' \
  -d '{"userId": "2", "email":"existing@email.com", "name": "Existing User"}'
```

> NOTE: You will have to use terminal to execute these curl commands or you can import [postman collection](https://www.getpostman.com/collections/4414bc745e79aedb2173)
