# Census

## Show

```shell
curl -X GET "/api/companies/j1Lp7yarNg4F3nGuHhwH7Gr3/census" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
```

> Response looks like this:

```json
{
    "save_failed_due_to_errors": null,
    "top_level_errors": null,
    "show_group_to_individual_selected": false,
    "covered_members_count": 3,
    "covered_employees_count": 3,
    "covered_spouses_count": 0,
    "covered_children_count": 0,
    "census_uploaded": null,
    "upload_errors": [],
    "upload_valid": null,
    "covered_singles_count": 3,
    "covered_single_and_spouses_count": 0,
    "covered_single_and_children_count": 0,
    "covered_families_count": 0,
    "households": [
        {
            "id": 262906,
            "coverage_type": "employee_only",
            "row_number": 0,
            "tier": "single",
            "census_household_members_attributes": [
                {
                    "id": 325257,
                    "age": 64,
                    "gender": "M",
                    "annual_salary": 60000,
                    "date_of_birth": "01/01/1953",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Some Guy",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "single",
                    "display_coverage_type": "Employee Only"
                }
            ]
        },
        {
            "id": 262907,
            "coverage_type": "employee_only",
            "row_number": 1,
            "tier": "single",
            "census_household_members_attributes": [
                {
                    "id": 325258,
                    "age": 19,
                    "gender": "M",
                    "annual_salary": 40000,
                    "date_of_birth": "01/01/1998",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "AB",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "single",
                    "display_coverage_type": "Employee Only"
                }
            ]
        },
        {
            "id": 262908,
            "coverage_type": "employee_only",
            "row_number": 2,
            "tier": "single",
            "census_household_members_attributes": [
                {
                    "id": 325259,
                    "age": 63,
                    "gender": "M",
                    "annual_salary": 45000,
                    "date_of_birth": "01/01/1954",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "CD",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "single",
                    "display_coverage_type": "Employee Only"
                }
            ]
        }
    ]
}
```

Use this endpoint to retrieve company's census.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/companies/j1Lp7yarNg4F3nGuHhwH7Gr3/census`

### Parameters

No parameters required.


`POST /api/companies/j1Lp7yarNg4F3nGuHhwH7Gr3/census`

## Create

```shell
curl -X POST "/api/companies/j1Lp7yarNg4F3nGuHhwH7Gr3/census" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q" \
     -d '{"company_renewal":false,"census":{"save_failed_due_to_errors":null,"top_level_errors":null,"show_group_to_individual_selected":false,"covered_members_count":3,"covered_employees_count":3,"covered_spouses_count":0,"covered_children_count":0,"census_uploaded":null,"upload_errors":[],"upload_valid":null,"covered_singles_count":3,"covered_single_and_spouses_count":0,"covered_single_and_children_count":0,"covered_families_count":0,"households":[{"id":262906,"coverage_type":"employee_only","row_number":0,"tier":"single","census_household_members_attributes":[{"id":325257,"age":64,"gender":"M","annual_salary":60000,"date_of_birth":"01/01/1953","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"Some Guy","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only"}]},{"id":262907,"coverage_type":"employee_only","row_number":1,"tier":"single","census_household_members_attributes":[{"id":325258,"age":19,"gender":"M","annual_salary":40000,"date_of_birth":"01/01/1998","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"AB","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only"}]},{"id":262908,"coverage_type":"employee_only","row_number":2,"tier":"single","census_household_members_attributes":[{"id":325259,"age":63,"gender":"M","annual_salary":45000,"date_of_birth":"01/01/1954","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"CD","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only"}]}]}}'
```

> Response looks like this:

```json
{
  "slug": "JZPI8621",
  "is_renewal": false
}
```

Use this endpoint to create a new census.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`POST /api/companies/j1Lp7yarNg4F3nGuHhwH7Gr3/census`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
census       | N/A     | Census object         | true

Check on the right to see an example of the census object.

> Here's an example of the census object:

```json
{
  "company_renewal": false,
  "census": {
    "save_failed_due_to_errors": null,
    "top_level_errors": null,
    "show_group_to_individual_selected": false,
    "covered_members_count": 3,
    "covered_employees_count": 3,
    "covered_spouses_count": 0,
    "covered_children_count": 0,
    "census_uploaded": null,
    "upload_errors": [],
    "upload_valid": null,
    "covered_singles_count": 3,
    "covered_single_and_spouses_count": 0,
    "covered_single_and_children_count": 0,
    "covered_families_count": 0,
    "households": [
      {
        "coverage_type": "employee_only",
        "row_number": 0,
        "tier": "single",
        "census_household_members_attributes": [
          {
            "id": 325257,
            "age": 64,
            "gender": "M",
            "annual_salary": 60000,
            "date_of_birth": "01/01/1953",
            "full_or_part_time": "FT",
            "hourly_rate": null,
            "hours_per_week": null,
            "name_or_initial": "Some Guy",
            "relationship": "primary",
            "smoker": false,
            "phone": null,
            "email": null,
            "household_tier": "single",
            "display_coverage_type": "Employee Only"
          }
        ]
      },
      {
        "coverage_type": "employee_only",
        "row_number": 1,
        "tier": "single",
        "census_household_members_attributes": [
          {
            "id": 325258,
            "age": 19,
            "gender": "M",
            "annual_salary": 40000,
            "date_of_birth": "01/01/1998",
            "full_or_part_time": "FT",
            "hourly_rate": null,
            "hours_per_week": null,
            "name_or_initial": "AB",
            "relationship": "primary",
            "smoker": false,
            "phone": null,
            "email": null,
            "household_tier": "single",
            "display_coverage_type": "Employee Only"
          }
        ]
      },
      {
        "coverage_type": "employee_only",
        "row_number": 2,
        "tier": "single",
        "census_household_members_attributes": [
          {
            "id": 325259,
            "age": 63,
            "gender": "M",
            "annual_salary": 45000,
            "date_of_birth": "01/01/1954",
            "full_or_part_time": "FT",
            "hourly_rate": null,
            "hours_per_week": null,
            "name_or_initial": "CD",
            "relationship": "primary",
            "smoker": false,
            "phone": null,
            "email": null,
            "household_tier": "single",
            "display_coverage_type": "Employee Only"
          }
        ]
      }
    ]
  }
}
```


## Upload Census

```shell
curl -X POST "/api/companies/j1Lp7yarNg4F3nGuHhwH7Gr3/census/create_from_excel" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
     -d '<EXCEL_FILE_DATA>'
```

> Response looks like this:

```json
{
    "save_failed_due_to_errors": null,
    "top_level_errors": null,
    "show_group_to_individual_selected": false,
    "covered_members_count": 26,
    "covered_employees_count": 5,
    "covered_spouses_count": 3,
    "covered_children_count": 18,
    "census_uploaded": true,
    "upload_errors": [],
    "upload_valid": true,
    "covered_singles_count": 0,
    "covered_single_and_spouses_count": 0,
    "covered_single_and_children_count": 0,
    "covered_families_count": 0,
    "households": [
        {
            "id": null,
            "coverage_type": "employee_only",
            "row_number": 1,
            "tier": "single",
            "census_household_members_attributes": [
                {
                    "id": null,
                    "age": 37,
                    "gender": null,
                    "annual_salary": 60000,
                    "date_of_birth": "01/01/1980",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee1",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Employee Only"
                }
            ]
        },
        {
            "id": null,
            "coverage_type": "employee_only",
            "row_number": 2,
            "tier": "single",
            "census_household_members_attributes": [
                {
                    "id": null,
                    "age": 42,
                    "gender": null,
                    "annual_salary": 31200,
                    "date_of_birth": "01/01/1975",
                    "full_or_part_time": "PT",
                    "hourly_rate": "20.0",
                    "hours_per_week": "30.0",
                    "name_or_initial": "Employee2",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Employee Only"
                }
            ]
        },
        {
            "id": null,
            "coverage_type": "family",
            "row_number": 3,
            "tier": "family",
            "census_household_members_attributes": [
                {
                    "id": null,
                    "age": 45,
                    "gender": null,
                    "annual_salary": 80000,
                    "date_of_birth": "01/01/1972",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Employee + Family"
                },
                {
                    "id": null,
                    "age": 49,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/1968",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Spouse",
                    "relationship": "spouse",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Spouse"
                },
                {
                    "id": null,
                    "age": 17,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2000",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child2",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 15,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2002",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child3",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 14,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2003",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child4",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 13,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2004",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child5",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 12,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2005",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child6",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 11,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2006",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child7",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 9,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2008",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child8",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 23,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/1994",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child9",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child 18+"
                },
                {
                    "id": null,
                    "age": 24,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/1993",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Child10",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child 18+"
                }
            ]
        },
        {
            "id": null,
            "coverage_type": "family",
            "row_number": 4,
            "tier": "family",
            "census_household_members_attributes": [
                {
                    "id": null,
                    "age": 45,
                    "gender": null,
                    "annual_salary": 70000,
                    "date_of_birth": "01/01/1972",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Employee + Family"
                },
                {
                    "id": null,
                    "age": 49,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/1968",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Spouse",
                    "relationship": "spouse",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Spouse"
                },
                {
                    "id": null,
                    "age": 19,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/1998",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child1",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child 18+"
                },
                {
                    "id": null,
                    "age": 17,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2000",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child2",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 15,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2002",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child3",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 13,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2004",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child4",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 12,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2005",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child5",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 11,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2006",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child6",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 10,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/2007",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child7",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child Under 18"
                },
                {
                    "id": null,
                    "age": 18,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/1999",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child8",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child 18+"
                },
                {
                    "id": null,
                    "age": 22,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/1995",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee4 Child9",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Child 18+"
                }
            ]
        },
        {
            "id": null,
            "coverage_type": "family",
            "row_number": 5,
            "tier": "single_and_spouse",
            "census_household_members_attributes": [
                {
                    "id": null,
                    "age": 45,
                    "gender": null,
                    "annual_salary": 75000,
                    "date_of_birth": "01/01/1972",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Employee + Family"
                },
                {
                    "id": null,
                    "age": 49,
                    "gender": null,
                    "annual_salary": null,
                    "date_of_birth": "01/01/1968",
                    "full_or_part_time": "",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Employee3 Spouse",
                    "relationship": "spouse",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": null,
                    "display_coverage_type": "Spouse"
                }
            ]
        }
    ]
}
```

Use this endpoint to create a census from an excel file.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`POST /api/companies/j1Lp7yarNg4F3nGuHhwH7Gr3/create_from_excel`

### Parameters

Parameter       | Default | Description           | Required?
--------------- | ------- | --------------------- | ----------
excel_file_data | N/A     | Excel file data       | true
