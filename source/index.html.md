---
title: Wellthie Business API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - go
  - javascript
  - powershell
  - objective_c

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - authentication
  - organizations
  - companies
  - proposals
  - inquiries
  - census
  - plans
  - enrollments
  - errors

search: true
---

# Introduction

Welcome to the Wellthie Business API Documentation.

## API Base URL

Examples in this document will reference the Wellthie demo site at wellthiedemo-smallbusiness.affordablecareadvisor.com whose API base URL is therefore `https://wellthiedemo-smallbusiness.affordablecareadvisor.com/api/`.


<!-- Authentication is implemented using the `devise-token-auth` gem. Visit their docs [here](https://github.com/lynndylanhurley/devise_token_auth) for more information. -->

In the curl examples you'll see on the right, when trying to execute those on the command line, remember to add a particular host with the appropriate organization_slug. For example: `http://wellthiedemo-smallbusiness-test.lvh.me:3030`.

## API Authentication
```javascript|go|shell|powershell
auth_headers = {
  "access-token":"X258……….",
  "token-type":"Bearer",
  "client":"IWc…...",
  "expiry":"<EXPIRY VALUE",
  "uid":"<UID VALUE>"
};
```

> The auth_headers has to be URL Encoded. Final Cookie for auth_header will look like this.

```javascript|go|shell|powershell
auth_headers%3D%7B%22access-token%22%3A%22X258%E2%80%A6%E2%80%A6%E2%80%A6.%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22IWc%E2%80%A6...%22%2C%22expiry%22%3A%22EXPIRY+VALUE%22%2C%22uid%22%3A%22UID+VALUE%22%7D%3B
```

The Header should set the following values…

1. Cookie  
2. access-token
3. client
4. expiry
5. uid
6. Content-Type = application/json

<aside class="success">
This app uses token based authentication . Each request would respond with a set of headers which has to be set to make further calls.
</aside>
