---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - users
  - groups
  - messages
  - errors
 

search: true
---

# Welcome to PostIt API

Welcome to the PostIt API - A simple application that allows friends and colleagues create groups for notifications. You can use our API to access PostIt endpoints, which can give you information on how to register, login, create groups, add users to groups, and manage your manage your groups.

We have language bindings in JavaScript! You can view code examples in the dark area to the right.
This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

PostIt uses (username and password) to login to allow access to the API protected routes. On registering or login, a token is generated.

PostIt expects for the token to be included in all API requests to the server in a header that looks like the following:

Authorization: **token**

> To get access to the users, groups and messages on PostIt, you have to be registered:
> Register and login to get a token to be inserted in the header

## Login

> Request:

```javascript
{
  "username": "abundance",
  "password": "abundance1",
}
```

> Response:

```javascript
{
  "message": "Signin successful!",
  "userId": 1,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjIsImlhdCI6MTUwNTI5OTEwMCwiZXhwIjoxNTA1Mzg1NTAwfQ.013qUhgGJNbkKyET1IvGWCEDco38dE3c3-aSzqo6HS4"
}
```

### Request
- Endpoint: POST: `api/user/signin`
- Body `(application/json)`


### Response
- Status: `200: OK`
- Body `(application/json)`



<aside class="notice">
You must set the token at the header after login to access protected routes
</aside>

