---
title: Wellthie Individual API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: cURL
  - go: golang
  - javascript: jQuery
  - powershell: Powershell
  - objective_c: Objective-C

toc_footers:
  - © Copyright 2020 Wellthie Inc.
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - authentication
  - quotes
  - plans
  - errors

search: true
---

# Introduction

Welcome to the Wellthie Individual API Documentation.

## API Base URL

Examples in this document will reference the Wellthie demo site at wellthie-qa.affordablecareadvisor.net whose API base URL is therefore `https://wellthie-qa.affordablecareadvisor.net/api/`.

<!-- Authentication is implemented using the `devise-token-auth` gem. Visit their docs [here](https://github.com/lynndylanhurley/devise_token_auth) for more information. -->

## API Authentication

```json
{
    "data": {
        "id": 23614,
        "slug": "rAC4Y2iLUkSdGdTfowryiq5t",
        "first_name": "test",
        "last_name": "test",
        "email": "email@domain.com",
        "provider": "email",
        "uid": "email@domain.com",
        "password_changed_at": "2020-02-27T10:56:29.972-05:00",
        "organization_id": 35,
        "team_id": null,
        "role": "individual",
        "user_type": null,
        "broker_code": null,
        "phone_number": null,
        "account_expiration_date": null,
        "created_by_user_id": null,
        "time_zone": "Eastern Time (US & Canada)",
        "deleted_at": null,
        "salesforce_email": null,
        "salesforce_access_token": null,
        "salesforce_refresh_token": null,
        "salesforce_lock": false,
        "allow_password_change": false,
        "is_any_broker_type": false,
        "latest_quote_id": "TX-213456",
        "access_token": "eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDI1MDk2fQ.IXCIo5ZH2yum0-FO_ovYrpbJ8Xvpd5s4T6VlkqLR26o"
    }
}
```

<aside class="notice">Wellthie Individual App uses a <a href="https://jwt.io/introduction/">JWT Based Token Authentication Mechanism</a></aside>

This app uses JWT token based authentication [Oauth 2.0 RFC](https://tools.ietf.org/html/rfc6750). Each protected request is expected to include the `Authorization` header with the access_token value.

When you [sign in](#sign-in) the response would include `access_token` as part of the `data` in case of a successful login. 

The Header should set the following values…

1. Authorization Bearer [access_token value]
2. Content-Type = application/json

<aside class="notice">
A Bearer Token is set in the Authorization header of every Inline Action HTTP Request.

<br/>`Bearer tokens` are used to access OAuth 2.0 protected resources.
</aside>

