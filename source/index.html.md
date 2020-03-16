---
title: Wellthie Business API Documentation

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
  - organizations
  - companies
  - inquiries
  - census
  - plans
  - proposals
  - enrollments
  - others
  - errors

search: true
---

# Introduction

Welcome to the Wellthie Business API Documentation.

## API Base URL

Examples in this document will reference the Wellthie demo site at wellthiedemo-smallbusiness-qa.affordablecareadvisor.net whose API base URL is therefore `https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/`.

<aside class="notice">
Reach out to <a href="mailto:hello@wellthie.com">Wellthie</a> for production URL and other credentials
</aside>
<!-- Authentication is implemented using the `devise-token-auth` gem. Visit their docs [here](https://github.com/lynndylanhurley/devise_token_auth) for more information. -->

## API Authentication

```json
{
    "data": {
        "id": 58463,
        "slug": "poVcXdGc35qERs1ngPTXgsZ1",
        "first_name": "firstName",
        "last_name": "lastName",
        "email": "apidoc+broker@wellthie.com",
        "provider": "email",
        "uid": "apidoc+broker@wellthie.com",
        "password_changed_at": "2020-03-05T07:38:17.526-05:00",
        "organization_id": 23,
        "team_id": null,
        "role": "broker",
        "user_type": null,
        "broker_code": "123456",
        "phone_number": null,
        "account_expiration_date": null,
        "created_by_user_id": null,
        "time_zone": "Eastern Time (US & Canada)",
        "deleted_at": null,
        "company_id": null,
        "allow_password_change": false,
        "is_any_broker_type": true,
        "access_token": "eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ2MywiY2xpZW50Ijoiem82VnJxYTRhZ0ZQVkhITS1jTnA0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiMGY4ZTg5YmFkOGY4YjMzZjFlNjc0MjVlMjE3NzVjYmQiLCJleHAiOjE1ODQ0Mjg4MDF9.XJP8sJVUX2mxwQ_MkryQbB8AUPcuQMvr65Dxrsvp7PA"
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
