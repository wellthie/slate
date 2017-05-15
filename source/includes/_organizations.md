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

`GET /api/organization/broker_brandings?company_slug=:slug`

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
        }
      ]
    },
    {
      "day": "Tuesday, May 16",
      "data": "2017-05-16",
      "hours": [
        {
          "label": "9:00AM - 10:00AM"
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

No parameters required.


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

No parameters required.
