# Companies

## Show

```shell
curl -X GET "/api/companies/j1Lp7yarNg4F3nGuHhwH7Gr3" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: name.lastname@domain.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A"
```

> Response looks like this:

```json
{
  "slug": "j1Lp7yarNg4F3nGuHhwH7Gr3",
  "name": "Uhc 64 Age Issue",
  "is_renewal": false,
  "zip_code_input": "90210",
  "contact_name": "Sebs",
  "contact_email": "sebs@gmail.com",
  "effective_date": "2017-06-01",
  "formatted_effective_date": "06/01/2017",
  "using_broker": true,
  "broker_code": "SJC1",
  "errors_json": [],
  "county_id": 6037,
  "save_failed_due_to_errors": null,
  "attributes_with_error_messages_in_order": [
    "name",
    "zip_code_input",
    "contact_name",
    "contact_email",
    "effective_date",
    "county_id"
  ],
  "json_key": null,
  "uses_tiers": false,
  "settings": {
    "child_max_age_for_inclusion_in_household": 26,
    "show_group_to_individual": false,
    "default_salary_adjustment": 30,
    "business_large_group_url": "https://www.amerihealthnj.com/html/employers/large_businesses.html?",
    "business_individual_url": "https://www.healthcare.gov/"
  },
  "small_group_max_size": 100,
  "show_group_to_individual": false,
  "include_g2i_inquiry": false,
  "latest_inquiry_slug": "NDQJ3912",
  "sic_code": 111,
  "formatted_sic_code": "0111",
  "show_tobacco_for_census": false,
  "current_plan": null
}
```

Use this endpoint to retrieve information about specific companies.

<aside class="notice">
  This endpoint is secured and requires authentication headers. These include <code>uid</code>, <code>access-token</code> and <code>client</code>.
</aside>

### HTTP Request

`GET /api/companies/:slug`

### Parameters

No parameters required.


## Create

```shell
curl -X POST "/api/companies" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A" \
     -d '{"company":{"name":"Test Company","zip_code_input":"07001","contact_name":"Test Owner","contact_email":"testowner1@company.com","using_broker":false,"broker_code":null,"effective_date":"2017-06-01","county_id":34023,"sic_code":"5411"}}'
```

> Response looks like this:

```json
{
  "slug": "zcZUuDSkDb7TRzTbPWmj6HSa",
  "name": "Test Company",
  "is_renewal": false,
  "zip_code_input": "07001",
  "contact_name": "Test Owner",
  "contact_email": "testowner@company.com",
  "effective_date": "2017-06-01",
  "formatted_effective_date": "06/01/2017",
  "using_broker": true,
  "broker_code": "SJC1",
  "errors_json": [],
  "county_id": 34023,
  "save_failed_due_to_errors": null,
  "attributes_with_error_messages_in_order": [
    "name",
    "zip_code_input",
    "contact_name",
    "contact_email",
    "effective_date",
    "county_id"
  ],
  "json_key": null,
  "uses_tiers": false,
  "settings": {
    "child_max_age_for_inclusion_in_household": 26,
    "show_group_to_individual": null,
    "default_salary_adjustment": 30,
    "business_large_group_url": "https://www.amerihealthnj.com/html/employers/large_businesses.html?",
    "business_individual_url": "https://www.healthcare.gov/"
  },
  "small_group_max_size": 50,
  "show_group_to_individual": null,
  "include_g2i_inquiry": false,
  "latest_inquiry_slug": null,
  "sic_code": 5411,
  "formatted_sic_code": "5411",
  "show_tobacco_for_census": false,
  "current_plan": null
}
```

Use this endpoint to create a new company. Inside the request should be a json object `{}` which describes the parameters below for the company that is to be created.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`POST /api/companies`

### Parameters

Parameter          | Default | Description             | Required?
------------------ | ------- | ----------------------- | ----------
company            | N/A     | Company object          | true
 - name            | N/A     | name                    | true
 - zip_code_input  | N/A     | zipcode                 | true
 - contact_name    | N/A     | contact name            | true
 - contact_email   | N/A     | contact email           | true
 - using_broker    | N/A     | Using broker flag       | false
 - broker_code     | N/A     | Broker code             | true if using_broker, false otherwise
 - effective_date  | N/A     | Effective date          | true
 - county_id       | N/A     | county id               | true
 - sic_code        | N/A     | sic code                | true


## Update

```shell
curl -X PUT "/api/companies/zcZUuDSkDb7TRzTbPWmj6HSa" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A" \
     -d '{"company":{"name":"Test Company","zip_code_input":"07001","contact_name":"Test Owner","contact_email":"testowner1@company.com","using_broker":false,"broker_code":null,"effective_date":"2017-06-01","county_id":34023,"sic_code":"5411"}}'
```

> Response looks like this:

```json
{
  "slug": "zcZUuDSkDb7TRzTbPWmj6HSa",
  "name": "Test Company",
  "is_renewal": false,
  "zip_code_input": "07001",
  "contact_name": "Test Owner",
  "contact_email": "testowner1@company.com",
  "effective_date": "2017-06-01",
  "formatted_effective_date": "06/01/2017",
  "using_broker": false,
  "broker_code": null,
  "errors_json": [],
  "county_id": 34023,
  "save_failed_due_to_errors": null,
  "attributes_with_error_messages_in_order": [
    "name",
    "zip_code_input",
    "contact_name",
    "contact_email",
    "effective_date",
    "county_id"
  ],
  "json_key": null,
  "uses_tiers": false,
  "settings": {
    "child_max_age_for_inclusion_in_household": 26,
    "show_group_to_individual": null,
    "default_salary_adjustment": 30,
    "business_large_group_url": "https://www.amerihealthnj.com/html/employers/large_businesses.html?",
    "business_individual_url": "https://www.healthcare.gov/"
  },
  "small_group_max_size": 50,
  "show_group_to_individual": null,
  "include_g2i_inquiry": false,
  "latest_inquiry_slug": null,
  "sic_code": 5411,
  "formatted_sic_code": "5411",
  "show_tobacco_for_census": false,
  "current_plan": null
}
```

Use this endpoint to update an existing company.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`PUT /api/companies/:slug`

### Parameters

Parameter          | Default | Description             | Required?
------------------ | ------- | ----------------------- | ----------
company            | N/A     | Company object          | true
 - name            | N/A     | name                    | true
 - zip_code_input  | N/A     | zipcode                 | true
 - contact_name    | N/A     | contact name            | true
 - contact_email   | N/A     | contact email           | true
 - using_broker    | N/A     | Using broker flag       | false
 - broker_code     | N/A     | Broker code             | true if using_broker, false otherwise
 - effective_date  | N/A     | Effective date          | true
 - county_id       | N/A     | county id               | true
 - sic_code        | N/A     | sic code                | true


## Settings

```shell
curl -X GET "/api/companies/zcZUuDSkDb7TRzTbPWmj6HSa/settings" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A"
```

> Response looks like this:

```json
{
  "child_max_age_for_inclusion_in_household": 26,
  "show_group_to_individual": null,
  "default_salary_adjustment": 30,
  "business_large_group_url": "https://www.amerihealthnj.com/html/employers/large_businesses.html?",
  "business_individual_url": "https://www.healthcare.gov/"
}
```

Use this endpoint to fetch company's settings.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/companies/:company_slug/settings`

### Parameters

No parameters required.


## Show CurrentPlan

```shell
curl -X GET "http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/companies/syihaNDipEVKDVaMQQxZxATw/current_plan" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A"
```

> Response looks like this for companies who don't have a current plan:

```json
{ }
```

> Response looks like this for companies who have a current plan

```json
{
  "id": 682,
  "current_plan_issuer": "Anthem",
  "name": "Advantage PPO",
  "company_id": 62560,
  "metal_level_name": "Bronze",
  "medical_deductible_single": null,
  "medical_deductible_family": null,
  "maximum_out_of_pocket_limit_single": null,
  "maximum_out_of_pocket_limit_family": null,
  "pcp": null,
  "specialist": null,
  "network_type": null,
  "preventive_care": null,
  "inpatient_facility": null,
  "emergency_room": null,
  "ambulance": null,
  "urgent_care": null,
  "generic": null,
  "highlight_1": {
    "icon": "icon--metal",
    "value": "Bronze"
  },
  "highlight_2": null,
  "highlight_3": null,
  "formulary_brand": null,
  "non_formulary_brand": null,
  "mail_order": null,
  "employer_monthly_cost": 1876,
  "current_plan_issuer_logo": ""
}
```

Use this endpoint to fetch company's current_plan. It'll be available if the company previously ran a renewal quote.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/companies/zcZUuDSkDb7TRzTbPWmj6HSa/current_plan`

### Parameters

No parameters required.


## Create CurrentPlan

```shell
curl -X POST "/api/companies/syihaNDipEVKDVaMQQxZxATw/current_plan" \
     -H "Content-Type: application/json" \
     -H "access-token: e_onQAmbg-Nl15g7DdSHAw" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: U6-SpF_K42Hh3QfmS14Uvg" \
     -d '{"current_plan_issuer":"Anthem","name":"Advantage PPO","company_id":62560,"metal_level_name":"Bronze","medical_deductible_single":null,"medical_deductible_family":null,"maximum_out_of_pocket_limit_single":null,"maximum_out_of_pocket_limit_family":null,"pcp":null,"specialist":null,"network_type":null,"preventive_care":null,"inpatient_facility":null,"emergency_room":null,"ambulance":null,"urgent_care":null,"generic":null,"highlight_1":{"icon":"icon--metal","value":"Bronze"},"highlight_2":null,"highlight_3":null,"formulary_brand":null,"non_formulary_brand":null,"mail_order":null,"employer_monthly_cost":1876}'
```

> Response looks like this:

```json
{
    "id": 682,
    "current_plan_issuer": "Anthem",
    "name": "Advantage PPO",
    "company_id": 62560,
    "metal_level_name": "Bronze",
    "medical_deductible_single": null,
    "medical_deductible_family": null,
    "maximum_out_of_pocket_limit_single": null,
    "maximum_out_of_pocket_limit_family": null,
    "pcp": null,
    "specialist": null,
    "network_type": null,
    "preventive_care": null,
    "inpatient_facility": null,
    "emergency_room": null,
    "ambulance": null,
    "urgent_care": null,
    "generic": null,
    "highlight_1": {
        "icon": "icon--metal",
        "value": "Bronze"
    },
    "highlight_2": null,
    "highlight_3": null,
    "formulary_brand": null,
    "non_formulary_brand": null,
    "mail_order": null,
    "employer_monthly_cost": 1876,
    "current_plan_issuer_logo": ""
}
```

Use this endpoint to create a new current_plan to a company. This is used for renewal quotes.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`POST /api/companies/zcZUuDSkDb7TRzTbPWmj6HSa/current_plan`

### Parameters


Parameter                          | Default   | Description                | Required?
-----------------------------------| --------- | -------------------------- | ----------
current_plan_issuer                | N/A       | Issuer for this plan       | false
name                               | N/A       | Plan name                  | true
company_id                         | N/A       | Company's id               | false
metal_level_name                   | N/A       | Metal level for plan       | false
medical_deductible_single          | N/A       | Medical deductible single  | false
medical_deductible_family          | N/A       | Medical deductible family  | false
maximum_out_of_pocket_limit_single | N/A       | Max out of pocket single   | false
maximum_out_of_pocket_limit_family | N/A       | Max out of pocket family   | false
pcp                                | N/A       | PCP                        | false
specialist                         | N/A       | Specialist                 | false
network_type                       | N/A       | Network Type               | false
preventive_care                    | N/A       | Preventive Care            | false
inpatient_facility                 | N/A       | Inpatient Facility         | false
emergency_room                     | N/A       | Emergency Room             | false
ambulance                          | N/A       | Ambulance                  | false
urgent_care                        | N/A       | Urgent Care                | false
generic                            | N/A       | Generic                    | false
highlight_1                        | N/A       | Highlight 1                | false
highlight_2                        | N/A       | Highlight 2                | false
highlight_3                        | N/A       | Highlight 3                | false
formulary_brand                    | N/A       | Formulary Brand            | false
non_formulary_brand                | N/A       | Non-Formulary Brand        | false
mail_order                         | N/A       | Mail Order                 | false
employer_monthly_cost              | N/A       | Employer Monthly Cost      | false
