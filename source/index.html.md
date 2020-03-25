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

Welcome to the Wellthie Affordable Care Advisor (Individual) API Documentation.

The Wellthie Affordable Care Advisor is a tool that helps you plan for and estimate costs of your insurance options based on the Affordable Care Act (ACA). One can also understand if they may be eligible for any financial assistance and estimate the potential penalty for not having insurance for an ongoing period/year. By entering your zip code, date of birth, family members and household income, the Wellthie Individual platform presents insurance options and makes calculations based on the ACA, state regulations and approved insurance rates. The calculations are estimates only, based on the information you provide. You will also get a list of important things to remember such as key dates, where to apply for insurance and who to call to get assistance.

[Wellthie](https://wellthie.affordablecareadvisor.com) helps individuals to discover health insurance online! It’s easy to find the best plans for your budget in minutes.

* Wellthie Individual is a [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) API.
* Wellthie Individual API uses JWT token-based authentication.
* JSON is returned by all API responses, including errors.

## Audience

This Documentation for Wellthie Individual API is specifically intended for developers looking to integrate Wellthie's Individual Insurance Quoting tool in a client facing app. For example:

* Building a custom consumer facing app.
* Integrating Wellthie Individual App inside a mobile app

<aside class="success">We have provided examples for 
<br/><code style="margin-left: 30px;line-height: 30px;">1. cURL</code>
<br/><code style="margin-left: 30px;line-height: 30px;">2. Golang</code>
<br/><code style="margin-left: 30px;line-height: 30px;">3. jQuery</code>
<br/><code style="margin-left: 30px;line-height: 30px;">4. Objective-C</code>
<br/><code style="margin-left: 30px;line-height: 30px;">5. Powershell</code>
</aside>

## API Base URL

Examples in this document will reference the Wellthie whose API base URL is

`https://wellthie-qa.affordablecareadvisor.net/api/`.

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

This app uses JWT token-based authentication (see [Oauth 2.0 RFC](https://tools.ietf.org/html/rfc6750)). Each protected request is expected to include the `Authorization` header with the `access_token` value.

When you [sign in](#sign-in) the response would include `access_token` as part of the `data` in case of a successful login. 

The Header should set the following values…

1. `Authorization Bearer [access_token value]`
2. `Content-Type` set to `application/json`

<aside class="notice">
A Bearer Token is set in the Authorization header of every Inline Action HTTP Request.

<br/>`Bearer tokens` are used to access OAuth 2.0 protected resources.
</aside>