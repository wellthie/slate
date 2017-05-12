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

In the curl examples you'll see on the right, when trying to execute those on the command line, remember to add a particular host with the appropriate organization_slug. For example: `http://wellthiedemo-smallbusiness-test.lvh.me:3030`.

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
curl -X DELETE "/api/auth/sign_out" \
     -H "Content-Type: application/json" \
     -d '{"uid": "name.lastname@domain.com", "client": "WedFsHGWTiAfdhl4LbFVjg", "access-token": "UyuaNMouSdihadn"}'
```

> Response looks like this:

```json
{
  "success": true
}
```

Use this endpoint to finish the session and discard the access-token acquired on the sign in API call

### HTTP Request

`POST /api/auth/sign_out`

### Parameters

Parameter    | Default | Description            | Required?
------------ | ------- | ---------------------- | ----------
uid          | N/A     | User's email address   | true
client       | N/A     | Client token [HEADERS] | true
access-token | N/A     | Token from sign in     | true


# Organizations

## Broker Branding

```shell
curl -X GET "/api/organization/broker_brandings?company_slug=j1Lp7yarNg4F3nGuHhwH7Gr3" \
     -H "Content-Type: application/json"
```

> Response looks like this:

```json
{
  "contact_name": "Wellthie",
  "contact_email": "support@wellthie.com",
  "contact_phone": "888-680-0856",
  "website_url": "www.wellthie.com",
  "logo": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/broker_brandings/logos/000/000/030/original/wellthie-logo-300square.png?2016",
  "logo_small_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/broker_brandings/logos/000/000/030/small/wellthie-logo-300square.png?2016",
  "logo_cover_page_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/broker_brandings/logos/000/000/030/cover_page/wellthie-logo-300square.png?2016"
}
```

Use this endpoint to get the broker branding information.

<aside class="notice">
  This endpoint does not require any session or authorization token.
</aside>

### HTTP Request

`GET /api/organization/broker_brandings`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
company_slug | N/A     | Company's slug        | true


## Settings

```shell
curl -X POST "/api/organization/settings" \
     -H "Content-Type: application/json"
```

> Response looks like this:

```json
{
  "logo": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/organizations/logos/000/000/023/main/logo-4-color.png?1474486469",
  "splash_image": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/organizations/splash_photos/000/000/023/homepage/1600x800-Banner-01.png?1461855472",
  "show_broker_code": true,
  "effective_dates": [
    {
      "label": "June 1, 2017",
      "data": "2017-06-01"
    }
  ],
  "show_schedule_a_call": true,
  "schedule_a_call_availabilities": [
    {
      "day": "Monday, May 15",
      "data": "2017-05-15",
      "hours": [
        {
          "label": "9:00AM - 10:00AM"
        },
        {
          "label": "10:00AM - 11:00AM"
        },
        {
          "label": "11:00AM - 12:00AM"
        },
        {
          "label": "12:00AM - 1:00PM"
        },
        {
          "label": "1:00PM - 2:00PM"
        },
        {
          "label": "2:00PM - 3:00PM"
        },
        {
          "label": "3:00PM - 4:00PM"
        },
        {
          "label": "4:00PM - 5:00PM"
        }
      ]
    },
    {
      "day": "Tuesday, May 16",
      "data": "2017-05-16",
      "hours": [
        {
          "label": "9:00AM - 10:00AM"
        },
        {
          "label": "10:00AM - 11:00AM"
        },
        {
          "label": "11:00AM - 12:00AM"
        },
        {
          "label": "12:00AM - 1:00PM"
        },
        {
          "label": "1:00PM - 2:00PM"
        },
        {
          "label": "2:00PM - 3:00PM"
        },
        {
          "label": "3:00PM - 4:00PM"
        },
        {
          "label": "4:00PM - 5:00PM"
        }
      ]
    },
    {
      "day": "Wednesday, May 17",
      "data": "2017-05-17",
      "hours": [
        {
          "label": "9:00AM - 10:00AM"
        },
        {
          "label": "10:00AM - 11:00AM"
        },
        {
          "label": "11:00AM - 12:00AM"
        },
        {
          "label": "12:00AM - 1:00PM"
        },
        {
          "label": "1:00PM - 2:00PM"
        },
        {
          "label": "2:00PM - 3:00PM"
        },
        {
          "label": "3:00PM - 4:00PM"
        },
        {
          "label": "4:00PM - 5:00PM"
        }
      ]
    }
  ],
  "show_issuer_logos": false,
  "broker_code_regex": "^[a-zA-Z0-9]{4,10}$",
  "broker_code_message": "4-10 Alphanumeric Codes",
  "excel_template_file": true,
  "excel_template_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/organizations/excel_templates/000/000/023/original/downloadable_census-rc37-oc36.xlsx?1478203799",
  "show_group_to_individual": true,
  "hide_enrollment_buttons_on_quote_page": false,
  "business_large_group_url": "https://www.amerihealthnj.com/html/employers/large_businesses.html?",
  "business_individual_url": "https://www.healthcare.gov/",
  "census_child_max_age_for_inclusion_in_household": 26,
  "show_renewals": true,
  "use_sso": true,
  "sso_idp_target_url": "https://wellthieinc-dev.onelogin.com",
  "sso_idp_login_link_text": "Login through Wellthie's OneLogin",
  "disable_direct_login": false,
  "organization_name": "Wellthie Demo",
  "show_dental": true,
  "show_vision": true,
  "show_value_add": true
}
```

Use this endpoint to retrieve the particular 

<aside class="notice">
  This endpoint does not require any session or authorization token.
</aside>

### HTTP Request

`GET /api/organization/settings`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------




`GET            /api/organization/content_areas`

## Content Areas

```shell
curl -X POST "/api/organization/content_areas" \
     -H "Content-Type: application/json"
```

> Response looks like this:

```json
{
  {
    "name": "Plan Attribute Tooltip: physical_occupational_speech",
    "content": "Therapy for mobility, language and/or speech related issues."
  },
  {
    "name": "Plan Attribute Tooltip: durable_medical_equipment",
    "content": "Supplies used for everyday or extended use. Covers oxygen supplies, wheelchairs, crutches or blood testing strips."
  },
  {
    "name": "Plan Attribute Tooltip: hearing_aids",
    "content": "A device placed around or in the ear that makes sounds louder."
  },
{
```

Use this endpoint to list the content areas configured to a particular organization.

<aside class="notice">
  This endpoint does not require any session or authorization token.
</aside>

<aside class="notice">
  The JSON response on the right is way longer than this example shows.
</aside>

### HTTP Request

`POST /api/organization/content_areas`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------

# Companies

## Show Company
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
