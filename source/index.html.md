---
title: Wellthie Business API Documentation

language_tabs:
  - shell

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Wellthie Business API Documentation.

Authentication is implemented using the `devise-token-auth` gem. Visit their docs [here](https://github.com/lynndylanhurley/devise_token_auth) for more information.

<!-- Welcome to the Kittn API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation. -->

# Authentication

## Sign In

```shell
curl -X POST "http://organization_slug.lvh.me:3030/api/auth/sign_in" \
     -H "Content-Type: application/json" \
     -d '{"email": "name.lastname@domain.com", "password": "pswrd"}' \
     -i
```

> The above command returns a json like the following:

```json
{
  "data": {
    "id": id,
    "slug": "slug",
    "first_name": "Name",
    "last_name": "Lastname",
    "email": "name.lastname@domain.com",
    "provider": "email",
    "uid": "name.lastname@domain.com",
    "password_changed_at": "2017-05-04T12:57:21.000-04:00",
    "organization_id": 1,
    "team_id": null,
    "role": "organization_admin",
    "user_type": null,
    "npn": "A1B2",
    "broker_code": "A1B2",
    "phone_number": "",
    "account_expiration_date": null,
    "created_by_user_id": 2,
    "time_zone": "Eastern Time (US & Canada)",
    "deleted_at": null,
    "is_any_broker_type": true
  }
}
```

> And headers like this:

```code
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Transfer-Encoding: chunked
Connection: keep-alive
Status: 200 OK
Cache-Control: max-age=0, private, must-revalidate
...
access-token: pFROqRpujmUQjLtJDwgUQw
X-Request-Id: 2787fd10-3057-4d0a-a2ea-35e0ea1e3faf
token-type: Bearer
expiry: 1495669515
uid: name.lastname@domain.com
```

This endpoint allows you to get a session token.

### HTTP Request

`POST http://organization_slug.lvh.me:3030/api/auth/sign_in`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
email        | N/A     | User's email address  | true
password     | N/A     | User's password       | true

## Sign out

Describe Signout

# Organizations

Describe here.


## Broker Branding

`GET            /api/organization/broker_brandings`

## Settings

`GET            /api/organization/settings`


## Content Areas

`GET            /api/organization/content_areas`


# Companies

`POST           /api/companies`

`GET            /api/companies/:slug`

`PATCH          /api/companies/:slug`

`PUT            /api/companies/:slug`

## Settings

`GET            /api/companies/:company_slug/settings`

## Current Plan

`GET            /api/companies/:company_slug/current_plan`

`POST           /api/companies/:company_slug/current_plan`

## Inquiries

`GET            /api/companies/:company_slug/inquiries`

## Group Plans

`GET            /api/companies/:company_slug/group_plans`

## Group Plans Pricing

`GET            /api/companies/:company_slug/group_plans_pricing`

## Plan Selections

`GET            /api/companies/:company_slug/plan_selections`

## Individual Quotes

`GET            /api/companies/:company_slug/individual_quotes`


# Census

`POST           /api/companies/:company_slug/census`

`GET            /api/companies/:company_slug/census`

## Create Census from Excel

`POST           /api/companies/:company_slug/census/create_from_excel`

# Inquiries

`POST           /api/inquiries`

`GET            /api/inquiries/:slug`

`PATCH          /api/inquiries/:slug`

`PUT            /api/inquiries/:slug`

## Plan Selections

`GET            /api/inquiries/:inquiry_slug/plan_selections`

## Individual Quotes

`GET            /api/inquiries/:inquiry_slug/individual_quotes`

## Download Excel

`POST           /api/inquiries/:inquiry_slug/download_excel`

# Plans

## Group Plans

`GET            /api/inquiries/:inquiry_slug/plans/group_plans`

## Group Plans Pricing

`GET            /api/inquiries/:inquiry_slug/plans/group_plans_pricing`

## Individual Plans

`GET            /api/inquiries/:inquiry_slug/plans/individual_plans`

## Individual Plans Pricing

`GET            /api/inquiries/:inquiry_slug/plans/individual_plans_pricing`

## Filters

`GET            /api/inquiries/:inquiry_slug/plans/filters`

## Compare

`POST           /api/inquiries/:inquiry_slug/plans/compare/generate_excel`

`GET            /api/inquiries/:inquiry_slug/plans/compare/download_excel`

`POST           /api/inquiries/:inquiry_slug/plans/compare/generate_filtered_plan_excel`

`GET            /api/inquiries/:inquiry_slug/plans/compare/download_filtered_plan_excel`

## Select Plan

`POST           /api/inquiries/:inquiry_slug/plans/select`

## Unselect Plan

`DELETE         /api/inquiries/:inquiry_slug/plans/unselect`

# Enrollments

## Contact

`POST           /api/inquiries/:inquiry_slug/enrollments/contact`

## Employees Contact

`POST|PUT|PATCH /api/inquiries/:inquiry_slug/enrollments/employees_contact`

## Household Download

`GET            /api/inquiries/:inquiry_slug/enrollments/household/:household_id/download`

