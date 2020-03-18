---
title: Wellthie Business API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: cURL
  - go: golang
  - javascript: jQuery
  - objective_c: Objective-C
  - powershell: Powershell

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

Welcome to the Wellthie BIZ API Documentation.

Wellthie helps to discover Small Business health insurance online! [Wellthie](http://www.wellthie.com/smallbuiness) is transforming the insurance shopping experience by helping small businesses discover small business health insurance online. It’s easy to find the best plans for your budget in minutes.

Small-group health insurance is medical insurance geared toward businesses with 50 or fewer full-time equivalent employees. (In four states, they apply to businesses with up to 100 employees).

Small-group plans effective since January 2014 are compliant with the Affordable Care Act’s requirement of health coverage. Wellthie helps the Small businesses find ACA-Compliant plans and the premiums for the companies census (employee list)

* The Wellthie Smallbusiness API is built based on [REST](https://en.wikipedia.org/wiki/Representational_state_transfer). 
* Wellthie BIZ API is resource-oriented, and uses HTTP response codes to indicate API status & errors. We use built-in HTTP features, like HTTP verbs, which are understood by off-the-shelf HTTP clients. 
* Wellthie BIZ API uses JWT token Based authentication which we'll learn in next section
* JSON is returned by all API responses, including errors.

## Audience

This Documentation for BIZ API is specifically intended for developers looking to integrate Wellthie's BIZ Quoting tool in a client facing app. For example:

* Building a custom consumer facing app.
* Integrating Wellthie BIZ App inside a mobile app

<aside class="success">We have provided examples for 
<br/><code style="margin-left: 30px;line-height: 30px;">1. cURL</code>
<br/><code style="margin-left: 30px;line-height: 30px;">2. Golang</code>
<br/><code style="margin-left: 30px;line-height: 30px;">3. jQuery</code>
<br/><code style="margin-left: 30px;line-height: 30px;">4. Objective-C</code>
<br/><code style="margin-left: 30px;line-height: 30px;">5. Powershell</code>
</aside>

## API Base URL

Examples in this document will reference the Wellthie Staging Environment site at wellthiedemo-smallbusiness-qa.affordablecareadvisor.net whose API base URL is therefore `https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/`.

<aside class="notice">
Reach out to <a href="mailto:hello@wellthie.com">Wellthie</a> for production URL and other credentials
</aside>

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

<aside class="notice">Wellthie SmallBusiness API uses a <a href="https://jwt.io/introduction/">JWT Based Token Authentication Mechanism</a></aside>

This app uses JWT token based authentication [Oauth 2.0 RFC](https://tools.ietf.org/html/rfc6750). Each protected request is expected to include the `Authorization` header with the access_token value.

When you [sign in](#sign-in) the response would include `access_token` as part of the `data` in case of a successful login. 

The Header should set the following values…

1. Authorization Bearer [access_token value]
2. Content-Type = application/json

<aside class="notice">
A Bearer Token is set in the Authorization header of every Inline Action HTTP Request.

<br/>`Bearer tokens` are used to access OAuth 2.0 protected resources.
</aside>
