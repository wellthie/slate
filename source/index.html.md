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
curl -X POST "/api/auth/sign_in" \
     -H "Content-Type: application/json" \
     -d '{"email": "name.lastname@domain.com", "password": "pswrd"}'
```

> Response looks like this:

```json
{
  "data": {
    "id": "id",
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

This endpoint allows you to get a session token.

### HTTP Request

`POST /api/auth/sign_in`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
email        | N/A     | User's email address  | true
password     | N/A     | User's password       | true

## Sign out

```shell
curl -X DELETE "/api/auth/sign_in" \
     -H "Content-Type: application/json" \
     -d '{"uid": "name.lastname@domain.com", "client": "pswrd", "access-token": 'UyuaNMouSdihadn'}'
```

> Response looks like this:

```json
{
  "data": {
    "id": "id",
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

Describe Signout

# Organizations

Describe here.


## Broker Branding

`GET /api/organization/broker_brandings`

## Settings

`GET /api/organization/settings`


## Content Areas

`GET            /api/organization/content_areas`


# Companies

## GET
`GET            /api/companies/:slug`

## CREATE
`POST           /api/companies`

## UPDATE
`PUT            /api/companies/:slug`

## GET Settings
`GET            /api/companies/:company_slug/settings`

## GET CurrentPlan
`GET            /api/companies/:company_slug/current_plan`

## POST CurrentPlan
`POST           /api/companies/:company_slug/current_plan`


# Proposals

## GET Inquiries

`GET            /api/proposals/:company_slug/inquiries`

## Group Plans

`GET            /api/proposals/:company_slug/group_plans`

## Group Plans Pricing

`GET            /api/proposals/:company_slug/group_plans_pricing`

## Plan Selections

`GET            /api/proposals/:company_slug/plan_selections`

## Individual Quotes

`GET            /api/proposals/:company_slug/individual_quotes`

# Census

## GET
`GET            /api/companies/:company_slug/census`

## POST
`POST           /api/companies/:company_slug/census`

## Upload Census
`POST           /api/companies/:company_slug/census/create_from_excel`

# Inquiries

## GET
`GET            /api/inquiries/:slug`

## POST
`POST           /api/inquiries`

## PUT
`PUT            /api/inquiries/:slug`

## GET PlanSelections
`GET            /api/inquiries/:inquiry_slug/plan_selections`

## GET IndividualQuotes
`GET            /api/inquiries/:inquiry_slug/individual_quotes`

## POST DownloadExcel
`POST           /api/inquiries/:inquiry_slug/download_excel`


# Plans

## GET GroupPlans
`GET            /api/inquiries/:inquiry_slug/plans/group_plans`

## GET GroupPlansPricing
`GET            /api/inquiries/:inquiry_slug/plans/group_plans_pricing`

## GET IndividualPlans
`GET            /api/inquiries/:inquiry_slug/plans/individual_plans`

## GET IndividualPlansPricing
`GET            /api/inquiries/:inquiry_slug/plans/individual_plans_pricing`

## GET Filters
`GET            /api/inquiries/:inquiry_slug/plans/filters`

## POST SelectPlan (TODO)
`POST           /api/inquiries/:inquiry_slug/plans/select`

## DELETE UnselectPlan (TODO)
`DELETE         /api/inquiries/:inquiry_slug/plans/unselect`

## Compare (TODO)

`POST           /api/inquiries/:inquiry_slug/plans/compare/generate_excel`

`GET            /api/inquiries/:inquiry_slug/plans/compare/download_excel`

`POST           /api/inquiries/:inquiry_slug/plans/compare/generate_filtered_plan_excel`

`GET            /api/inquiries/:inquiry_slug/plans/compare/download_filtered_plan_excel`

# Enrollments

## POST Contact
`POST           /api/inquiries/:inquiry_slug/enrollments/contact`

## POST Employees Contact
`POST /api/inquiries/:inquiry_slug/enrollments/employees_contact`

## PUT Employees Contact
`PUT /api/inquiries/:inquiry_slug/enrollments/employees_contact`

## GET HouseholdDownload
`GET            /api/inquiries/:inquiry_slug/enrollments/household/:household_id/download`
