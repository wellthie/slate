# Census

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

Insurers use an “employee census” to obtain specific information to estimate the health care costs a small group business is likely to incur. The type of information collected is soley used to determining the premium of the employee.

A census does not include the health status, race, religion, sexual orientation (even if applying for domestic partner benefits), Social Security number, or U.S. citizenship/immigration status of the employee.

In order to provide you with a rate quote, insurers need a census form with the following information:

* Name (Optional)
* Age or date of birth (Mandatory)
* Number of dependents (Mandatory)
* Zip code (Mandatory)
* Gender
* Smoker/nonsmoker
* Annual Salary (Mandatory in some cases)

## Get Census

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/census' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU' \
--data-raw ''
```

```go
package main

import (
  "fmt"
  "strings"
  "net/http"
  "io/ioutil"
)

func main() {

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/census"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/census",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/census"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"" dataUsingEncoding:NSUTF8StringEncoding]];
[request setHTTPBody:postData];

[request setHTTPMethod:@"GET"];

NSURLSession *session = [NSURLSession sharedSession];
NSURLSessionDataTask *dataTask = [session dataTaskWithRequest:request
completionHandler:^(NSData *data, NSURLResponse *response, NSError *error) {
  if (error) {
    NSLog(@"%@", error);
  } else {
    NSHTTPURLResponse *httpResponse = (NSHTTPURLResponse *) response;
    NSError *parseError = nil;
    NSDictionary *responseDictionary = [NSJSONSerialization JSONObjectWithData:data options:0 error:&parseError];
    NSLog(@"%@",responseDictionary);
    dispatch_semaphore_signal(sema);
  }
}];
[dataTask resume];
dispatch_semaphore_wait(sema, DISPATCH_TIME_FOREVER);
```

```powershell
$headers = New-Object "System.Collections.Generic.Dictionary[[String],[String]]"
$headers.Add("Content-Type", "application/json")
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/census' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "inquiry_id": 130143,
    "save_failed_due_to_errors": null,
    "covered_employees_count": 4,
    "covered_spouses_count": 2,
    "covered_children_count": 2,
    "census_uploaded": null,
    "upload_errors": [],
    "covered_singles_count": 1,
    "covered_single_and_spouses_count": 1,
    "covered_single_and_children_count": 1,
    "covered_families_count": 1,
    "households": [
        {
            "id": 423022,
            "coverage_type": "employee_only",
            "row_number": 0,
            "tier": "single",
            "opted_dental": true,
            "opted_vision": true,
            "opted_limited_medical": false,
            "medical_plan_id": null,
            "sorted_matching_plan_service_area_ids": [
                4334,
                4982,
                4984,
                4985,
                5066,
                5067
            ],
            "zip_code": "10001",
            "county_id": 36061,
            "attributes_with_error_messages_in_order": [],
            "census_household_members_attributes": [
                {
                    "id": 523270,
                    "age": 39,
                    "gender": "M",
                    "annual_salary": 100000,
                    "date_of_birth": "10/10/1980",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "John Doe",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "single",
                    "display_coverage_type": "Employee Only",
                    "display_member_name": "John Doe"
                }
            ]
        },
        {
            "id": 423023,
            "coverage_type": "family",
            "row_number": 1,
            "tier": "single_and_spouse",
            "opted_dental": true,
            "opted_vision": true,
            "opted_limited_medical": false,
            "medical_plan_id": null,
            "sorted_matching_plan_service_area_ids": [
                4334,
                4982,
                4984,
                4985,
                5066,
                5067
            ],
            "zip_code": "10001",
            "county_id": 36061,
            "attributes_with_error_messages_in_order": [],
            "census_household_members_attributes": [
                {
                    "id": 523271,
                    "age": 34,
                    "gender": "F",
                    "annual_salary": 100000,
                    "date_of_birth": "10/21/1985",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Joe Root",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "single_and_spouse",
                    "display_coverage_type": "Employee + Dependents",
                    "display_member_name": "Joe Root"
                },
                {
                    "id": 523272,
                    "age": 29,
                    "gender": "F",
                    "annual_salary": 100000,
                    "date_of_birth": "12/15/1990",
                    "full_or_part_time": null,
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Tina",
                    "relationship": "spouse",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "single_and_spouse",
                    "display_coverage_type": "Spouse",
                    "display_member_name": "Tina"
                }
            ]
        },
        {
            "id": 423024,
            "coverage_type": "family",
            "row_number": 2,
            "tier": "family",
            "opted_dental": true,
            "opted_vision": true,
            "opted_limited_medical": false,
            "medical_plan_id": null,
            "sorted_matching_plan_service_area_ids": [
                4334,
                4982,
                4984,
                4985,
                5066,
                5067
            ],
            "zip_code": "10001",
            "county_id": 36061,
            "attributes_with_error_messages_in_order": [],
            "census_household_members_attributes": [
                {
                    "id": 523273,
                    "age": 30,
                    "gender": "M",
                    "annual_salary": 100000,
                    "date_of_birth": "01/01/1990",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "James Smith",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "family",
                    "display_coverage_type": "Employee + Dependents",
                    "display_member_name": "James Smith"
                },
                {
                    "id": 523274,
                    "age": 28,
                    "gender": "F",
                    "annual_salary": 100000,
                    "date_of_birth": "12/30/1991",
                    "full_or_part_time": null,
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Maria Garcia",
                    "relationship": "spouse",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "family",
                    "display_coverage_type": "Spouse",
                    "display_member_name": "Maria Garcia"
                },
                {
                    "id": 523275,
                    "age": 6,
                    "gender": "M",
                    "annual_salary": 100000,
                    "date_of_birth": "10/17/2013",
                    "full_or_part_time": null,
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Robert Smith",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "family",
                    "display_coverage_type": "Child Under 18",
                    "display_member_name": "Robert Smith"
                }
            ]
        },
        {
            "id": 423025,
            "coverage_type": "family",
            "row_number": 3,
            "tier": "single_and_children",
            "opted_dental": true,
            "opted_vision": true,
            "opted_limited_medical": false,
            "medical_plan_id": null,
            "sorted_matching_plan_service_area_ids": [
                4334,
                4982,
                4984,
                4985,
                5066,
                5067
            ],
            "zip_code": "10001",
            "county_id": 36061,
            "attributes_with_error_messages_in_order": [],
            "census_household_members_attributes": [
                {
                    "id": 523276,
                    "age": 39,
                    "gender": "F",
                    "annual_salary": 100000,
                    "date_of_birth": "12/11/1980",
                    "full_or_part_time": "FT",
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "Maria Rodriguez",
                    "relationship": "primary",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "single_and_children",
                    "display_coverage_type": "Employee + Dependents",
                    "display_member_name": "Maria Rodriguez"
                },
                {
                    "id": 523277,
                    "age": 13,
                    "gender": "M",
                    "annual_salary": 100000,
                    "date_of_birth": "07/27/2006",
                    "full_or_part_time": null,
                    "hourly_rate": null,
                    "hours_per_week": null,
                    "name_or_initial": "David Rodriguez",
                    "relationship": "child",
                    "smoker": false,
                    "phone": null,
                    "email": null,
                    "household_tier": "single_and_children",
                    "display_coverage_type": "Child Under 18",
                    "display_member_name": "David Rodriguez"
                }
            ]
        }
    ]
}

```

Use this endpoint to retrieve company's census.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/census`

### Parameters

No parameters required.

## Create Census

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/census' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU' \
--data-raw '{"census":{"inquiry_id":130133,"save_failed_due_to_errors":null,"covered_employees_count":4,"covered_spouses_count":0,"covered_children_count":0,"census_uploaded":null,"upload_errors":[],"covered_singles_count":4,"covered_single_and_spouses_count":0,"covered_single_and_children_count":0,"covered_families_count":0,"households":[{"id":422979,"coverage_type":"employee_only","row_number":0,"tier":"single","opted_dental":true,"opted_vision":true,"opted_limited_medical":false,"medical_plan_id":null,"sorted_matching_plan_service_area_ids":[4334,4982,4984,4985,5066,5067],"zip_code":"10001","county_id":36061,"attributes_with_error_messages_in_order":[],"census_household_members_attributes":[{"id":523199,"age":null,"gender":"M","annual_salary":100000,"date_of_birth":"10/10/1980","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"John Doe","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only","display_member_name":"Employee 1","name_or_initial_focus":false,"date_of_birth_focus":false,"gender_focus":false,"full_or_part_time_focus":false}]},{"id":422980,"coverage_type":"family","row_number":1,"tier":"single","opted_dental":true,"opted_vision":true,"opted_limited_medical":false,"medical_plan_id":null,"sorted_matching_plan_service_area_ids":[4334,4982,4984,4985,5066,5067],"zip_code":"10001","county_id":36061,"attributes_with_error_messages_in_order":[],"census_household_members_attributes":[{"id":523200,"age":null,"gender":"F","annual_salary":100000,"date_of_birth":"10/21/1985","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"Joe Root","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only","display_member_name":"Employee 2","name_or_initial_focus":false,"date_of_birth_focus":false,"gender_focus":false},{"relationship":"spouse","name_or_initial":"Tina","date_of_birth":"12/15/1990","gender":"F","age":null,"full_or_part_time":null,"hours_per_week":null,"hourly_rate":null,"annual_salary":100000,"smoker":null,"relationship_focus":false,"name_or_initial_focus":false,"date_of_birth_focus":false}],"coverage_type_focus":false},{"id":422981,"coverage_type":"family","row_number":2,"tier":"single","opted_dental":true,"opted_vision":true,"opted_limited_medical":false,"medical_plan_id":null,"sorted_matching_plan_service_area_ids":[4334,4982,4984,4985,5066,5067],"zip_code":"10001","county_id":36061,"attributes_with_error_messages_in_order":[],"census_household_members_attributes":[{"id":523201,"age":null,"gender":"M","annual_salary":100000,"date_of_birth":"01/01/1990","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"James Smith","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only","display_member_name":"Employee 3","name_or_initial_focus":false,"gender_focus":false,"date_of_birth_focus":false},{"relationship":"spouse","name_or_initial":"Maria Garcia","date_of_birth":"12/30/1991","gender":"F","age":null,"full_or_part_time":null,"hours_per_week":null,"hourly_rate":null,"annual_salary":100000,"smoker":null,"relationship_focus":false,"name_or_initial_focus":false,"date_of_birth_focus":false,"gender_focus":false},{"relationship":"child","name_or_initial":"Robert Smith","date_of_birth":"10/17/2013","gender":"M","age":null,"full_or_part_time":null,"hours_per_week":null,"hourly_rate":null,"annual_salary":100000,"smoker":null,"relationship_focus":false,"name_or_initial_focus":false,"gender_focus":false,"date_of_birth_focus":false}],"coverage_type_focus":false},{"id":422982,"coverage_type":"family","row_number":3,"tier":"single","opted_dental":true,"opted_vision":true,"opted_limited_medical":false,"medical_plan_id":null,"sorted_matching_plan_service_area_ids":[4334,4982,4984,4985,5066,5067],"zip_code":"10001","county_id":36061,"attributes_with_error_messages_in_order":[],"census_household_members_attributes":[{"id":523202,"age":null,"gender":"F","annual_salary":100000,"date_of_birth":"12/11/1980","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"Maria Rodriguez","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only","display_member_name":"Employee 4","name_or_initial_focus":false,"date_of_birth_focus":false},{"relationship":"child","name_or_initial":"David Rodriguez","date_of_birth":"07/27/2006","gender":"M","age":null,"full_or_part_time":null,"hours_per_week":null,"hourly_rate":null,"annual_salary":100000,"smoker":null,"relationship_focus":false,"name_or_initial_focus":false,"gender_focus":false,"date_of_birth_focus":false}],"coverage_type_focus":false}]}}'
```

```go
package main

import (
  "fmt"
  "strings"
  "net/http"
  "io/ioutil"
)

func main() {

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/census"
  method := "POST"

  payload := strings.NewReader("{\"census\":{\"inquiry_id\":130133,\"save_failed_due_to_errors\":null,\"covered_employees_count\":4,\"covered_spouses_count\":0,\"covered_children_count\":0,\"census_uploaded\":null,\"upload_errors\":[],\"covered_singles_count\":4,\"covered_single_and_spouses_count\":0,\"covered_single_and_children_count\":0,\"covered_families_count\":0,\"households\":[{\"id\":422979,\"coverage_type\":\"employee_only\",\"row_number\":0,\"tier\":\"single\",\"opted_dental\":true,\"opted_vision\":true,\"opted_limited_medical\":false,\"medical_plan_id\":null,\"sorted_matching_plan_service_area_ids\":[4334,4982,4984,4985,5066,5067],\"zip_code\":\"10001\",\"county_id\":36061,\"attributes_with_error_messages_in_order\":[],\"census_household_members_attributes\":[{\"id\":523199,\"age\":null,\"gender\":\"M\",\"annual_salary\":100000,\"date_of_birth\":\"10/10/1980\",\"full_or_part_time\":\"FT\",\"hourly_rate\":null,\"hours_per_week\":null,\"name_or_initial\":\"John Doe\",\"relationship\":\"primary\",\"smoker\":false,\"phone\":null,\"email\":null,\"household_tier\":\"single\",\"display_coverage_type\":\"Employee Only\",\"display_member_name\":\"Employee 1\",\"name_or_initial_focus\":false,\"date_of_birth_focus\":false,\"gender_focus\":false,\"full_or_part_time_focus\":false}]},{\"id\":422980,\"coverage_type\":\"family\",\"row_number\":1,\"tier\":\"single\",\"opted_dental\":true,\"opted_vision\":true,\"opted_limited_medical\":false,\"medical_plan_id\":null,\"sorted_matching_plan_service_area_ids\":[4334,4982,4984,4985,5066,5067],\"zip_code\":\"10001\",\"county_id\":36061,\"attributes_with_error_messages_in_order\":[],\"census_household_members_attributes\":[{\"id\":523200,\"age\":null,\"gender\":\"F\",\"annual_salary\":100000,\"date_of_birth\":\"10/21/1985\",\"full_or_part_time\":\"FT\",\"hourly_rate\":null,\"hours_per_week\":null,\"name_or_initial\":\"Joe Root\",\"relationship\":\"primary\",\"smoker\":false,\"phone\":null,\"email\":null,\"household_tier\":\"single\",\"display_coverage_type\":\"Employee Only\",\"display_member_name\":\"Employee 2\",\"name_or_initial_focus\":false,\"date_of_birth_focus\":false,\"gender_focus\":false},{\"relationship\":\"spouse\",\"name_or_initial\":\"Tina\",\"date_of_birth\":\"12/15/1990\",\"gender\":\"F\",\"age\":null,\"full_or_part_time\":null,\"hours_per_week\":null,\"hourly_rate\":null,\"annual_salary\":100000,\"smoker\":null,\"relationship_focus\":false,\"name_or_initial_focus\":false,\"date_of_birth_focus\":false}],\"coverage_type_focus\":false},{\"id\":422981,\"coverage_type\":\"family\",\"row_number\":2,\"tier\":\"single\",\"opted_dental\":true,\"opted_vision\":true,\"opted_limited_medical\":false,\"medical_plan_id\":null,\"sorted_matching_plan_service_area_ids\":[4334,4982,4984,4985,5066,5067],\"zip_code\":\"10001\",\"county_id\":36061,\"attributes_with_error_messages_in_order\":[],\"census_household_members_attributes\":[{\"id\":523201,\"age\":null,\"gender\":\"M\",\"annual_salary\":100000,\"date_of_birth\":\"01/01/1990\",\"full_or_part_time\":\"FT\",\"hourly_rate\":null,\"hours_per_week\":null,\"name_or_initial\":\"James Smith\",\"relationship\":\"primary\",\"smoker\":false,\"phone\":null,\"email\":null,\"household_tier\":\"single\",\"display_coverage_type\":\"Employee Only\",\"display_member_name\":\"Employee 3\",\"name_or_initial_focus\":false,\"gender_focus\":false,\"date_of_birth_focus\":false},{\"relationship\":\"spouse\",\"name_or_initial\":\"Maria Garcia\",\"date_of_birth\":\"12/30/1991\",\"gender\":\"F\",\"age\":null,\"full_or_part_time\":null,\"hours_per_week\":null,\"hourly_rate\":null,\"annual_salary\":100000,\"smoker\":null,\"relationship_focus\":false,\"name_or_initial_focus\":false,\"date_of_birth_focus\":false,\"gender_focus\":false},{\"relationship\":\"child\",\"name_or_initial\":\"Robert Smith\",\"date_of_birth\":\"10/17/2013\",\"gender\":\"M\",\"age\":null,\"full_or_part_time\":null,\"hours_per_week\":null,\"hourly_rate\":null,\"annual_salary\":100000,\"smoker\":null,\"relationship_focus\":false,\"name_or_initial_focus\":false,\"gender_focus\":false,\"date_of_birth_focus\":false}],\"coverage_type_focus\":false},{\"id\":422982,\"coverage_type\":\"family\",\"row_number\":3,\"tier\":\"single\",\"opted_dental\":true,\"opted_vision\":true,\"opted_limited_medical\":false,\"medical_plan_id\":null,\"sorted_matching_plan_service_area_ids\":[4334,4982,4984,4985,5066,5067],\"zip_code\":\"10001\",\"county_id\":36061,\"attributes_with_error_messages_in_order\":[],\"census_household_members_attributes\":[{\"id\":523202,\"age\":null,\"gender\":\"F\",\"annual_salary\":100000,\"date_of_birth\":\"12/11/1980\",\"full_or_part_time\":\"FT\",\"hourly_rate\":null,\"hours_per_week\":null,\"name_or_initial\":\"Maria Rodriguez\",\"relationship\":\"primary\",\"smoker\":false,\"phone\":null,\"email\":null,\"household_tier\":\"single\",\"display_coverage_type\":\"Employee Only\",\"display_member_name\":\"Employee 4\",\"name_or_initial_focus\":false,\"date_of_birth_focus\":false},{\"relationship\":\"child\",\"name_or_initial\":\"David Rodriguez\",\"date_of_birth\":\"07/27/2006\",\"gender\":\"M\",\"age\":null,\"full_or_part_time\":null,\"hours_per_week\":null,\"hourly_rate\":null,\"annual_salary\":100000,\"smoker\":null,\"relationship_focus\":false,\"name_or_initial_focus\":false,\"gender_focus\":false,\"date_of_birth_focus\":false}],\"coverage_type_focus\":false}]}}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/census",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU"
  },
  "data": JSON.stringify({"census":{"inquiry_id":130133,"save_failed_due_to_errors":null,"covered_employees_count":4,"covered_spouses_count":0,"covered_children_count":0,"census_uploaded":null,"upload_errors":[],"covered_singles_count":4,"covered_single_and_spouses_count":0,"covered_single_and_children_count":0,"covered_families_count":0,"households":[{"id":422979,"coverage_type":"employee_only","row_number":0,"tier":"single","opted_dental":true,"opted_vision":true,"opted_limited_medical":false,"medical_plan_id":null,"sorted_matching_plan_service_area_ids":[4334,4982,4984,4985,5066,5067],"zip_code":"10001","county_id":36061,"attributes_with_error_messages_in_order":[],"census_household_members_attributes":[{"id":523199,"age":null,"gender":"M","annual_salary":100000,"date_of_birth":"10/10/1980","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"John Doe","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only","display_member_name":"Employee 1","name_or_initial_focus":false,"date_of_birth_focus":false,"gender_focus":false,"full_or_part_time_focus":false}]},{"id":422980,"coverage_type":"family","row_number":1,"tier":"single","opted_dental":true,"opted_vision":true,"opted_limited_medical":false,"medical_plan_id":null,"sorted_matching_plan_service_area_ids":[4334,4982,4984,4985,5066,5067],"zip_code":"10001","county_id":36061,"attributes_with_error_messages_in_order":[],"census_household_members_attributes":[{"id":523200,"age":null,"gender":"F","annual_salary":100000,"date_of_birth":"10/21/1985","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"Joe Root","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only","display_member_name":"Employee 2","name_or_initial_focus":false,"date_of_birth_focus":false,"gender_focus":false},{"relationship":"spouse","name_or_initial":"Tina","date_of_birth":"12/15/1990","gender":"F","age":null,"full_or_part_time":null,"hours_per_week":null,"hourly_rate":null,"annual_salary":100000,"smoker":null,"relationship_focus":false,"name_or_initial_focus":false,"date_of_birth_focus":false}],"coverage_type_focus":false},{"id":422981,"coverage_type":"family","row_number":2,"tier":"single","opted_dental":true,"opted_vision":true,"opted_limited_medical":false,"medical_plan_id":null,"sorted_matching_plan_service_area_ids":[4334,4982,4984,4985,5066,5067],"zip_code":"10001","county_id":36061,"attributes_with_error_messages_in_order":[],"census_household_members_attributes":[{"id":523201,"age":null,"gender":"M","annual_salary":100000,"date_of_birth":"01/01/1990","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"James Smith","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only","display_member_name":"Employee 3","name_or_initial_focus":false,"gender_focus":false,"date_of_birth_focus":false},{"relationship":"spouse","name_or_initial":"Maria Garcia","date_of_birth":"12/30/1991","gender":"F","age":null,"full_or_part_time":null,"hours_per_week":null,"hourly_rate":null,"annual_salary":100000,"smoker":null,"relationship_focus":false,"name_or_initial_focus":false,"date_of_birth_focus":false,"gender_focus":false},{"relationship":"child","name_or_initial":"Robert Smith","date_of_birth":"10/17/2013","gender":"M","age":null,"full_or_part_time":null,"hours_per_week":null,"hourly_rate":null,"annual_salary":100000,"smoker":null,"relationship_focus":false,"name_or_initial_focus":false,"gender_focus":false,"date_of_birth_focus":false}],"coverage_type_focus":false},{"id":422982,"coverage_type":"family","row_number":3,"tier":"single","opted_dental":true,"opted_vision":true,"opted_limited_medical":false,"medical_plan_id":null,"sorted_matching_plan_service_area_ids":[4334,4982,4984,4985,5066,5067],"zip_code":"10001","county_id":36061,"attributes_with_error_messages_in_order":[],"census_household_members_attributes":[{"id":523202,"age":null,"gender":"F","annual_salary":100000,"date_of_birth":"12/11/1980","full_or_part_time":"FT","hourly_rate":null,"hours_per_week":null,"name_or_initial":"Maria Rodriguez","relationship":"primary","smoker":false,"phone":null,"email":null,"household_tier":"single","display_coverage_type":"Employee Only","display_member_name":"Employee 4","name_or_initial_focus":false,"date_of_birth_focus":false},{"relationship":"child","name_or_initial":"David Rodriguez","date_of_birth":"07/27/2006","gender":"M","age":null,"full_or_part_time":null,"hours_per_week":null,"hourly_rate":null,"annual_salary":100000,"smoker":null,"relationship_focus":false,"name_or_initial_focus":false,"gender_focus":false,"date_of_birth_focus":false}],"coverage_type_focus":false}]}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/census"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\"census\":{\"inquiry_id\":130133,\"save_failed_due_to_errors\":null,\"covered_employees_count\":4,\"covered_spouses_count\":0,\"covered_children_count\":0,\"census_uploaded\":null,\"upload_errors\":[],\"covered_singles_count\":4,\"covered_single_and_spouses_count\":0,\"covered_single_and_children_count\":0,\"covered_families_count\":0,\"households\":[{\"id\":422979,\"coverage_type\":\"employee_only\",\"row_number\":0,\"tier\":\"single\",\"opted_dental\":true,\"opted_vision\":true,\"opted_limited_medical\":false,\"medical_plan_id\":null,\"sorted_matching_plan_service_area_ids\":[4334,4982,4984,4985,5066,5067],\"zip_code\":\"10001\",\"county_id\":36061,\"attributes_with_error_messages_in_order\":[],\"census_household_members_attributes\":[{\"id\":523199,\"age\":null,\"gender\":\"M\",\"annual_salary\":100000,\"date_of_birth\":\"10/10/1980\",\"full_or_part_time\":\"FT\",\"hourly_rate\":null,\"hours_per_week\":null,\"name_or_initial\":\"John Doe\",\"relationship\":\"primary\",\"smoker\":false,\"phone\":null,\"email\":null,\"household_tier\":\"single\",\"display_coverage_type\":\"Employee Only\",\"display_member_name\":\"Employee 1\",\"name_or_initial_focus\":false,\"date_of_birth_focus\":false,\"gender_focus\":false,\"full_or_part_time_focus\":false}]},{\"id\":422980,\"coverage_type\":\"family\",\"row_number\":1,\"tier\":\"single\",\"opted_dental\":true,\"opted_vision\":true,\"opted_limited_medical\":false,\"medical_plan_id\":null,\"sorted_matching_plan_service_area_ids\":[4334,4982,4984,4985,5066,5067],\"zip_code\":\"10001\",\"county_id\":36061,\"attributes_with_error_messages_in_order\":[],\"census_household_members_attributes\":[{\"id\":523200,\"age\":null,\"gender\":\"F\",\"annual_salary\":100000,\"date_of_birth\":\"10/21/1985\",\"full_or_part_time\":\"FT\",\"hourly_rate\":null,\"hours_per_week\":null,\"name_or_initial\":\"Joe Root\",\"relationship\":\"primary\",\"smoker\":false,\"phone\":null,\"email\":null,\"household_tier\":\"single\",\"display_coverage_type\":\"Employee Only\",\"display_member_name\":\"Employee 2\",\"name_or_initial_focus\":false,\"date_of_birth_focus\":false,\"gender_focus\":false},{\"relationship\":\"spouse\",\"name_or_initial\":\"Tina\",\"date_of_birth\":\"12/15/1990\",\"gender\":\"F\",\"age\":null,\"full_or_part_time\":null,\"hours_per_week\":null,\"hourly_rate\":null,\"annual_salary\":100000,\"smoker\":null,\"relationship_focus\":false,\"name_or_initial_focus\":false,\"date_of_birth_focus\":false}],\"coverage_type_focus\":false},{\"id\":422981,\"coverage_type\":\"family\",\"row_number\":2,\"tier\":\"single\",\"opted_dental\":true,\"opted_vision\":true,\"opted_limited_medical\":false,\"medical_plan_id\":null,\"sorted_matching_plan_service_area_ids\":[4334,4982,4984,4985,5066,5067],\"zip_code\":\"10001\",\"county_id\":36061,\"attributes_with_error_messages_in_order\":[],\"census_household_members_attributes\":[{\"id\":523201,\"age\":null,\"gender\":\"M\",\"annual_salary\":100000,\"date_of_birth\":\"01/01/1990\",\"full_or_part_time\":\"FT\",\"hourly_rate\":null,\"hours_per_week\":null,\"name_or_initial\":\"James Smith\",\"relationship\":\"primary\",\"smoker\":false,\"phone\":null,\"email\":null,\"household_tier\":\"single\",\"display_coverage_type\":\"Employee Only\",\"display_member_name\":\"Employee 3\",\"name_or_initial_focus\":false,\"gender_focus\":false,\"date_of_birth_focus\":false},{\"relationship\":\"spouse\",\"name_or_initial\":\"Maria Garcia\",\"date_of_birth\":\"12/30/1991\",\"gender\":\"F\",\"age\":null,\"full_or_part_time\":null,\"hours_per_week\":null,\"hourly_rate\":null,\"annual_salary\":100000,\"smoker\":null,\"relationship_focus\":false,\"name_or_initial_focus\":false,\"date_of_birth_focus\":false,\"gender_focus\":false},{\"relationship\":\"child\",\"name_or_initial\":\"Robert Smith\",\"date_of_birth\":\"10/17/2013\",\"gender\":\"M\",\"age\":null,\"full_or_part_time\":null,\"hours_per_week\":null,\"hourly_rate\":null,\"annual_salary\":100000,\"smoker\":null,\"relationship_focus\":false,\"name_or_initial_focus\":false,\"gender_focus\":false,\"date_of_birth_focus\":false}],\"coverage_type_focus\":false},{\"id\":422982,\"coverage_type\":\"family\",\"row_number\":3,\"tier\":\"single\",\"opted_dental\":true,\"opted_vision\":true,\"opted_limited_medical\":false,\"medical_plan_id\":null,\"sorted_matching_plan_service_area_ids\":[4334,4982,4984,4985,5066,5067],\"zip_code\":\"10001\",\"county_id\":36061,\"attributes_with_error_messages_in_order\":[],\"census_household_members_attributes\":[{\"id\":523202,\"age\":null,\"gender\":\"F\",\"annual_salary\":100000,\"date_of_birth\":\"12/11/1980\",\"full_or_part_time\":\"FT\",\"hourly_rate\":null,\"hours_per_week\":null,\"name_or_initial\":\"Maria Rodriguez\",\"relationship\":\"primary\",\"smoker\":false,\"phone\":null,\"email\":null,\"household_tier\":\"single\",\"display_coverage_type\":\"Employee Only\",\"display_member_name\":\"Employee 4\",\"name_or_initial_focus\":false,\"date_of_birth_focus\":false},{\"relationship\":\"child\",\"name_or_initial\":\"David Rodriguez\",\"date_of_birth\":\"07/27/2006\",\"gender\":\"M\",\"age\":null,\"full_or_part_time\":null,\"hours_per_week\":null,\"hourly_rate\":null,\"annual_salary\":100000,\"smoker\":null,\"relationship_focus\":false,\"name_or_initial_focus\":false,\"gender_focus\":false,\"date_of_birth_focus\":false}],\"coverage_type_focus\":false}]}}" dataUsingEncoding:NSUTF8StringEncoding]];
[request setHTTPBody:postData];

[request setHTTPMethod:@"POST"];

NSURLSession *session = [NSURLSession sharedSession];
NSURLSessionDataTask *dataTask = [session dataTaskWithRequest:request
completionHandler:^(NSData *data, NSURLResponse *response, NSError *error) {
  if (error) {
    NSLog(@"%@", error);
  } else {
    NSHTTPURLResponse *httpResponse = (NSHTTPURLResponse *) response;
    NSError *parseError = nil;
    NSDictionary *responseDictionary = [NSJSONSerialization JSONObjectWithData:data options:0 error:&parseError];
    NSLog(@"%@",responseDictionary);
    dispatch_semaphore_signal(sema);
  }
}];
[dataTask resume];
dispatch_semaphore_wait(sema, DISPATCH_TIME_FOREVER);
```

```powershell
$headers = New-Object "System.Collections.Generic.Dictionary[[String],[String]]"
$headers.Add("Content-Type", "application/json")
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiWWFyZ1RzdDR6Y1M2ZXB0Q2UzeEQ0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MDU3ODh9.Xig16GNdsxp4mM1ueuhaBlw6803s3PR_tztOjbiGAoU")

$body = "{`"census`":{`"inquiry_id`":130133,`"save_failed_due_to_errors`":null,`"covered_employees_count`":4,`"covered_spouses_count`":0,`"covered_children_count`":0,`"census_uploaded`":null,`"upload_errors`":[],`"covered_singles_count`":4,`"covered_single_and_spouses_count`":0,`"covered_single_and_children_count`":0,`"covered_families_count`":0,`"households`":[{`"id`":422979,`"coverage_type`":`"employee_only`",`"row_number`":0,`"tier`":`"single`",`"opted_dental`":true,`"opted_vision`":true,`"opted_limited_medical`":false,`"medical_plan_id`":null,`"sorted_matching_plan_service_area_ids`":[4334,4982,4984,4985,5066,5067],`"zip_code`":`"10001`",`"county_id`":36061,`"attributes_with_error_messages_in_order`":[],`"census_household_members_attributes`":[{`"id`":523199,`"age`":null,`"gender`":`"M`",`"annual_salary`":100000,`"date_of_birth`":`"10/10/1980`",`"full_or_part_time`":`"FT`",`"hourly_rate`":null,`"hours_per_week`":null,`"name_or_initial`":`"John Doe`",`"relationship`":`"primary`",`"smoker`":false,`"phone`":null,`"email`":null,`"household_tier`":`"single`",`"display_coverage_type`":`"Employee Only`",`"display_member_name`":`"Employee 1`",`"name_or_initial_focus`":false,`"date_of_birth_focus`":false,`"gender_focus`":false,`"full_or_part_time_focus`":false}]},{`"id`":422980,`"coverage_type`":`"family`",`"row_number`":1,`"tier`":`"single`",`"opted_dental`":true,`"opted_vision`":true,`"opted_limited_medical`":false,`"medical_plan_id`":null,`"sorted_matching_plan_service_area_ids`":[4334,4982,4984,4985,5066,5067],`"zip_code`":`"10001`",`"county_id`":36061,`"attributes_with_error_messages_in_order`":[],`"census_household_members_attributes`":[{`"id`":523200,`"age`":null,`"gender`":`"F`",`"annual_salary`":100000,`"date_of_birth`":`"10/21/1985`",`"full_or_part_time`":`"FT`",`"hourly_rate`":null,`"hours_per_week`":null,`"name_or_initial`":`"Joe Root`",`"relationship`":`"primary`",`"smoker`":false,`"phone`":null,`"email`":null,`"household_tier`":`"single`",`"display_coverage_type`":`"Employee Only`",`"display_member_name`":`"Employee 2`",`"name_or_initial_focus`":false,`"date_of_birth_focus`":false,`"gender_focus`":false},{`"relationship`":`"spouse`",`"name_or_initial`":`"Tina`",`"date_of_birth`":`"12/15/1990`",`"gender`":`"F`",`"age`":null,`"full_or_part_time`":null,`"hours_per_week`":null,`"hourly_rate`":null,`"annual_salary`":100000,`"smoker`":null,`"relationship_focus`":false,`"name_or_initial_focus`":false,`"date_of_birth_focus`":false}],`"coverage_type_focus`":false},{`"id`":422981,`"coverage_type`":`"family`",`"row_number`":2,`"tier`":`"single`",`"opted_dental`":true,`"opted_vision`":true,`"opted_limited_medical`":false,`"medical_plan_id`":null,`"sorted_matching_plan_service_area_ids`":[4334,4982,4984,4985,5066,5067],`"zip_code`":`"10001`",`"county_id`":36061,`"attributes_with_error_messages_in_order`":[],`"census_household_members_attributes`":[{`"id`":523201,`"age`":null,`"gender`":`"M`",`"annual_salary`":100000,`"date_of_birth`":`"01/01/1990`",`"full_or_part_time`":`"FT`",`"hourly_rate`":null,`"hours_per_week`":null,`"name_or_initial`":`"James Smith`",`"relationship`":`"primary`",`"smoker`":false,`"phone`":null,`"email`":null,`"household_tier`":`"single`",`"display_coverage_type`":`"Employee Only`",`"display_member_name`":`"Employee 3`",`"name_or_initial_focus`":false,`"gender_focus`":false,`"date_of_birth_focus`":false},{`"relationship`":`"spouse`",`"name_or_initial`":`"Maria Garcia`",`"date_of_birth`":`"12/30/1991`",`"gender`":`"F`",`"age`":null,`"full_or_part_time`":null,`"hours_per_week`":null,`"hourly_rate`":null,`"annual_salary`":100000,`"smoker`":null,`"relationship_focus`":false,`"name_or_initial_focus`":false,`"date_of_birth_focus`":false,`"gender_focus`":false},{`"relationship`":`"child`",`"name_or_initial`":`"Robert Smith`",`"date_of_birth`":`"10/17/2013`",`"gender`":`"M`",`"age`":null,`"full_or_part_time`":null,`"hours_per_week`":null,`"hourly_rate`":null,`"annual_salary`":100000,`"smoker`":null,`"relationship_focus`":false,`"name_or_initial_focus`":false,`"gender_focus`":false,`"date_of_birth_focus`":false}],`"coverage_type_focus`":false},{`"id`":422982,`"coverage_type`":`"family`",`"row_number`":3,`"tier`":`"single`",`"opted_dental`":true,`"opted_vision`":true,`"opted_limited_medical`":false,`"medical_plan_id`":null,`"sorted_matching_plan_service_area_ids`":[4334,4982,4984,4985,5066,5067],`"zip_code`":`"10001`",`"county_id`":36061,`"attributes_with_error_messages_in_order`":[],`"census_household_members_attributes`":[{`"id`":523202,`"age`":null,`"gender`":`"F`",`"annual_salary`":100000,`"date_of_birth`":`"12/11/1980`",`"full_or_part_time`":`"FT`",`"hourly_rate`":null,`"hours_per_week`":null,`"name_or_initial`":`"Maria Rodriguez`",`"relationship`":`"primary`",`"smoker`":false,`"phone`":null,`"email`":null,`"household_tier`":`"single`",`"display_coverage_type`":`"Employee Only`",`"display_member_name`":`"Employee 4`",`"name_or_initial_focus`":false,`"date_of_birth_focus`":false},{`"relationship`":`"child`",`"name_or_initial`":`"David Rodriguez`",`"date_of_birth`":`"07/27/2006`",`"gender`":`"M`",`"age`":null,`"full_or_part_time`":null,`"hours_per_week`":null,`"hourly_rate`":null,`"annual_salary`":100000,`"smoker`":null,`"relationship_focus`":false,`"name_or_initial_focus`":false,`"gender_focus`":false,`"date_of_birth_focus`":false}],`"coverage_type_focus`":false}]}}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/census' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`POST /api/companies/:company_slug/census`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
census       | N/A     | Census object         | true

Check on the right to see an example of the census object.
