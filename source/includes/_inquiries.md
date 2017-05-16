# Inquiries

## Show

```shell
curl -X GET "/api/inquiries/NDQJ3912" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A"
```

> Response looks like this:

```json
{
  "title": null,
  "slug": "NDQJ3912",
  "company_slug": "j1Lp7yarNg4F3nGuHhwH7Gr3",
  "penalty_for_company_not_providing_insurance": 0,
  "monthly_cost_of_individual_plans_for_all_employees_after_credit_and_salary_adjustment": {},
  "individual_salary_adjustment": 30,
  "individual_salary_adjustment_after_tax": 21,
  "is_renewal": false,
  "group_to_individual_selected": false,
  "coverage": "small_group",
  "errors_json": [],
  "created_at": "2017-05-11T11:30:26.000-04:00",
  "contribution": {
    "id": 75468,
    "medical_input_type": "percent",
    "medical_primary_percentage": 100,
    "medical_spouse_percentage": 100,
    "medical_dependent_percentage": 100,
    "medical_primary_currency": 0,
    "medical_spouse_currency": 0,
    "medical_dependent_currency": 0,
    "medical_single_percentage": 100,
    "medical_single_currency": 0,
    "medical_single_and_spouse_percentage": 100,
    "medical_single_and_spouse_currency": 0,
    "medical_single_and_children_percentage": 100,
    "medical_single_and_children_currency": 0,
    "medical_family_percentage": 100,
    "medical_family_currency": 0
  }
}
```

Use this endpoint to fetch a particular inquiry.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/inquiries/:slug`

### Parameters

No parameters required.


## Create (Unused)

```shell
curl -X POST "/api/inquiries" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A"
     -d '{}'
```

> Response looks like this:

```json
# TO BE DEFINED
```

Use this endpoint to create a new inquiry for a company.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`POST /api/inquiries`

### Parameters

TO BE DEFINED


## Update

```shell
curl -X PUT "/api/inquiries/NDQJ3912" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q" \
     -d '{"title":"Updating title","individual_salary_adjustment":30,"individual_salary_adjustment_after_tax":21,"coverage":"small_group","contribution":{"medical_input_type":"percent","medical_primary_percentage":100,"medical_spouse_percentage":100,"medical_dependent_percentage":100,"medical_primary_currency":0,"medical_spouse_currency":0,"medical_dependent_currency":0,"medical_single_percentage":100,"medical_single_currency":0,"medical_single_and_spouse_percentage":100,"medical_single_and_spouse_currency":0,"medical_single_and_children_percentage":100,"medical_single_and_children_currency":0,"medical_family_percentage":100,"medical_family_currency":0}}'
```

> Response looks like this:

```json
{
  "title": "Updating title",
  "slug": "NDQJ3912",
  "company_slug": "j1Lp7yarNg4F3nGuHhwH7Gr3",
  "penalty_for_company_not_providing_insurance": 0,
  "monthly_cost_of_individual_plans_for_all_employees_after_credit_and_salary_adjustment": {},
  "individual_salary_adjustment": 30,
  "individual_salary_adjustment_after_tax": 21,
  "is_renewal": false,
  "group_to_individual_selected": false,
  "coverage": "small_group",
  "errors_json": [],
  "created_at": "2017-05-11T11:30:26.000-04:00",
  "contribution": {
    "id": 75468,
    "medical_input_type": "percent",
    "medical_primary_percentage": 100,
    "medical_spouse_percentage": 100,
    "medical_dependent_percentage": 100,
    "medical_primary_currency": 0,
    "medical_spouse_currency": 0,
    "medical_dependent_currency": 0,
    "medical_single_percentage": 100,
    "medical_single_currency": 0,
    "medical_single_and_spouse_percentage": 100,
    "medical_single_and_spouse_currency": 0,
    "medical_single_and_children_percentage": 100,
    "medical_single_and_children_currency": 0,
    "medical_family_percentage": 100,
    "medical_family_currency": 0
  }
}
```

Use this endpoint to update an inquiry.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`PUT /api/inquiries/:slug`

### Parameters

Parameter                              | Default               | Description                     | Required?
-------------------------------------- | --------------------- | ------------------------------- | ----------
title                                  | null                  | Quote's title                   | false
individual_salary_adjustment           | 30                    | Salary adjustment               | true
individual_salary_adjustment_after_tax | 30                    | Salary adjustment after tax     | false
coverage                               | Depends on quote type | Quote coverage selection        | true
contribution                           | object                | Contribution values container   | false

Check on the right to see an example of a contribution object.

> Here's an example of a contribution object:

```json
"contribution": {
  "medical_input_type": "percent",
  "medical_primary_percentage": 100,
  "medical_spouse_percentage": 100,
  "medical_dependent_percentage": 100,
  "medical_primary_currency": 0,
  "medical_spouse_currency": 0,
  "medical_dependent_currency": 0,
  "medical_single_percentage": 100,
  "medical_single_currency": 0,
  "medical_single_and_spouse_percentage": 100,
  "medical_single_and_spouse_currency": 0,
  "medical_single_and_children_percentage": 100,
  "medical_single_and_children_currency": 0,
  "medical_family_percentage": 100,
  "medical_family_currency": 0
}
```

## Show PlanSelections

```shell
curl -X GET "/api/inquiries/NDQJ3912/plan_selections" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
```

> Response looks like this:

```json
[
  {
    "id": 85868,
    "selected_plan_name": "INS NONDIFF PPO Silver - AKRU",
    "group_plan_id": 18418,
    "individual_plan_id": null,
    "added_to_cart": false,
    "order": 1
  }
]
```

Use this endpoint to retrieve inquiry's plan selections. It could be up to 4 elements / 4 plan selections.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plan_selections`

### Parameters

No parameters required.


## Show IndividualQuotes

```shell
curl -X GET "http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/inquiries/JUWD4521/individual_quotes" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
```

> Response looks like this:

```json
{
  "18639": [
    {
      "household_id": 262858,
      "monthly_price": 0,
      "monthly_credits": 0,
      "monthly_price_after_credit": 0,
      "monthly_price_after_credit_and_salary_adjustment": -100,
      "monthly_price_after_credit_and_salary_adjustment_after_tax": -70,
      "member_ids_to_plan_names": {
          "325137": "Metal"
      }
    },
  {
      "household_id": 262859,
      "monthly_price": 0,
      "monthly_credits": 0,
      "monthly_price_after_credit": 0,
      "monthly_price_after_credit_and_salary_adjustment": -100,
      "monthly_price_after_credit_and_salary_adjustment_after_tax": -70,
      "member_ids_to_plan_names": {
          "325138": "Metal"
      }
    },
    {
      "household_id": 262860,
      "monthly_price": 0,
      "monthly_credits": 0,
      "monthly_price_after_credit": 0,
      "monthly_price_after_credit_and_salary_adjustment": -100,
      "monthly_price_after_credit_and_salary_adjustment_after_tax": -70,
      "member_ids_to_plan_names": {
          "325139": "Metal"
      }
    },
    {
      "household_id": 262861,
      "monthly_price": 0,
      "monthly_credits": 0,
      "monthly_price_after_credit": 0,
      "monthly_price_after_credit_and_salary_adjustment": -100,
      "monthly_price_after_credit_and_salary_adjustment_after_tax": -70,
      "member_ids_to_plan_names": {
          "325140": "Metal",
          "325141": "Metal",
          "325142": "Metal",
          "325143": "Metal"
      }
    },
    {
      "household_id": 262862,
      "monthly_price": 0,
      "monthly_credits": 0,
      "monthly_price_after_credit": 0,
      "monthly_price_after_credit_and_salary_adjustment": -100,
      "monthly_price_after_credit_and_salary_adjustment_after_tax": -70,
      "member_ids_to_plan_names": {
          "325144": "Metal",
          "325145": "Metal"
      }
    }
  ]
}
```

Use this endpoint to retrieve individual plan quotes for those group to individual inquiries comparisons.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/individual_quotes`

### Parameters

No parameters required.


## Create DownloadExcel

```shell
curl -X POST "http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/inquiries/:inquiry_slug/download_excel" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
     -d '{"excel_data":"DATA","excel_file_name":"INS NONDIFF PPO Silver - AKRU - Employee Cost Breakdown","inquiry_slug":"NDQJ3912"}'
```

> Response looks like this:

```json
{
  "file_path": "/xlsx/ins-nondiff-ppo-silver-akru-employee-cost-breakdown.xlsx",
  "status": "ok"
}
```

Use this endpoint to download plans comparison on excel (.xlsx) format.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`POST /api/inquiries/:inquiry_slug/download_excel`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
email        | N/A     | User's email address  | true
password     | N/A     | User's password       | true
