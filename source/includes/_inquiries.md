# Inquiries

Inquiry is a quote with one or more plans selected for a the given Employee Census of a Small Business Company.

* An inquiry could have more than one plan (upto 4)
* An inquiry could be a fresh inquiry or a renewal.

Steps include to create an inquiry as follows.

1. Create Inquiry
2. Update Inquiry (if needed)
3. Create Inquiry Census
4. Get plans and pricing
5. Select plans
6. Unselect Plans (if needed)
7. Continue to create proposal

## Get an Inquiry

Use this endpoint to fetch a particular inquiry.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

> Sample Request

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "title": "G2I Quote - 2020-03-11",
    "slug": "LDYA3582",
    "id": 130143,
    "penalty_for_company_not_providing_insurance": 0,
    "is_renewal": false,
    "group_to_individual_selected": true,
    "created_at": "2020-03-16T08:20:58.035-04:00",
    "other_inquiries_with_census": [
        {
            "id": 130144,
            "title": "G2I Quote - 2020-03-11",
            "group_to_individual_selected": true,
            "is_renewal": false,
            "company_id": 107653,
            "slug": "QKJI5486",
            "created_at": "2020-03-17T02:10:48.633-04:00",
            "updated_at": "2020-03-17T02:11:07.418-04:00",
            "quoting_dental": true,
            "quoting_vision": true,
            "quoting_value_add": true,
            "dental_contribution_strategy": "voluntary",
            "vision_contribution_strategy": "voluntary",
            "dental_vision_bundle_contribution_strategy": "voluntary",
            "effective_date": "2020-04-01",
            "quoting_composite_rates": false,
            "quoting_limited_medical": false,
            "limited_medical_contribution_strategy": "voluntary",
            "current_plan_id": null
        }
    ],
    "quoting_dental": true,
    "quoting_vision": true,
    "quoting_value_add": true,
    "dental_contribution_strategy": "voluntary",
    "vision_contribution_strategy": "voluntary",
    "dental_vision_bundle_contribution_strategy": "voluntary",
    "effective_date": "2020-04-01",
    "tabs_for_plans_page": [
        "Medical"
    ],
    "individual_salary_adjustment_after_tax": 0.0,
    "quoting_composite_rates": false,
    "quoting_limited_medical": false,
    "limited_medical_contribution_strategy": "voluntary",
    "monthly_cost_of_individual_plans_for_all_employees_after_credit_and_salary_adjustment": {},
    "company_slug": "P7Kvahp8UmP7TLYXJDnsyZ3y",
    "formatted_effective_date": "04/01/2020",
    "contribution": {
        "id": 125655,
        "inquiry_id": 130143,
        "medical_input_type": "percent",
        "medical_primary_percentage": 100.0,
        "medical_spouse_percentage": 100.0,
        "medical_dependent_percentage": 100.0,
        "medical_primary_currency": 0.0,
        "medical_spouse_currency": 0.0,
        "medical_dependent_currency": 0.0,
        "medical_single_percentage": 100.0,
        "medical_single_currency": 0.0,
        "medical_single_and_spouse_percentage": 100.0,
        "medical_single_and_spouse_currency": 0.0,
        "medical_single_and_children_percentage": 100.0,
        "medical_single_and_children_currency": 0.0,
        "medical_family_percentage": 100.0,
        "medical_family_currency": 0.0,
        "dental_vision_input_type": "percent",
        "dental_household_percentage": 100.0,
        "dental_household_currency": 0.0,
        "vision_household_percentage": 100.0,
        "vision_household_currency": 0.0,
        "dental_and_vision_bundle_household_percentage": 100.0,
        "dental_and_vision_bundle_household_currency": 0.0,
        "accident_household_percentage": 100.0,
        "life_household_percentage": 100.0,
        "telemedicine_household_percentage": 100.0,
        "ad_and_d_household_percentage": 100.0,
        "nurse_helpline_household_percentage": 100.0,
        "identity_theft_household_percentage": 100.0,
        "hospital_cash_household_percentage": 100.0,
        "legal_assistance_household_percentage": 100.0,
        "eap_household_percentage": 100.0,
        "travel_assistance_household_percentage": 100.0,
        "pharmacy_household_percentage": 100.0,
        "value_add_bundle_household_percentage": 100.0,
        "individual_salary_adjustment": 0,
        "dbl_household_percentage": 100.0,
        "composite_medical_input_type": "percent",
        "composite_medical_single_percentage": 100.0,
        "composite_medical_single_currency": 0.0,
        "composite_medical_single_and_spouse_percentage": 100.0,
        "composite_medical_single_and_spouse_currency": 0.0,
        "composite_medical_single_and_children_percentage": 100.0,
        "composite_medical_single_and_children_currency": 0.0,
        "composite_medical_family_percentage": 100.0,
        "composite_medical_family_currency": 0.0,
        "limited_medical_input_type": null,
        "limited_medical_household_percentage": 100.0,
        "limited_medical_household_currency": 0.0
    },
    "plan_selections": [
        {
            "id": 136323,
            "individual_plan_id": null,
            "medical_plan_id": 78717,
            "ancillary_plan_id": null,
            "ancillary_plan_type": null,
            "selected_for_quote": true,
            "selected_for_enrollment": false,
            "order": 1
        },
        {
            "id": 136324,
            "individual_plan_id": null,
            "medical_plan_id": 78720,
            "ancillary_plan_id": null,
            "ancillary_plan_type": null,
            "selected_for_quote": true,
            "selected_for_enrollment": false,
            "order": 1
        },
        {
            "id": 136325,
            "individual_plan_id": null,
            "medical_plan_id": 78714,
            "ancillary_plan_id": null,
            "ancillary_plan_type": null,
            "selected_for_quote": true,
            "selected_for_enrollment": false,
            "order": 2
        }
    ],
    "current_plan": {
        "id": 4006,
        "current_plan_issuer": "Current Plan Issuer",
        "name": "Current Plan Name",
        "company_id": 107653,
        "metal_level_name": "Bronze",
        "medical_deductible_single": "Deductible Single",
        "medical_deductible_family": "Deductible Single",
        "maximum_out_of_pocket_limit_single": "Deductible Single",
        "maximum_out_of_pocket_limit_family": "Max-Out-of-Pocket Family",
        "pcp": "Primary Care Physician",
        "specialist": "Specialist",
        "network_type": "Network",
        "preventive_care": "Preventive Care",
        "inpatient_facility": "Hospital (Inpatient)",
        "emergency_room": "Emergency Room",
        "ambulance": "Ambulance",
        "urgent_care": "Urgent Care",
        "generic": "Generic Prescription",
        "formulary_brand": "Formulary Prescription",
        "non_formulary_brand": "Non Formulary Brand Prescription",
        "mail_order": "Mail Order (90 day supply)",
        "product_type": "medical",
        "carrier_plan_identifier": "123",
        "highlight_1": {
            "icon": "icon--metal",
            "value": "Bronze"
        },
        "highlight_2": {
            "icon": "icon--add-on",
            "value": "Network"
        },
        "highlight_3": {
            "icon": "icon--add-on",
            "value": "Deductible Single"
        },
        "employer_monthly_cost": 1000.0
    }
}
```

### HTTP Request

`GET /api/inquiries/:slug`

### Parameters

No parameters required.

## Create an Inquiry

Use this endpoint to create a new inquiry for a company.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>.
</aside>

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE' \
--data-raw '{
  "inquiry": {
    "effective_date": "2020-04-01",
    "quoting_dental": true,
    "quoting_vision": true,
    "quoting_value_add": true,
    "is_renewal": false,
    "quoting_composite_rates": false,
    "dental_contribution_strategy": "voluntary",
    "vision_contribution_strategy": "voluntary",
    "dental_vision_bundle_contribution_strategy": "voluntary",
    "limited_medical_contribution_strategy": "voluntary",
    "title": "G2I Quote - 2020-03-11",
    "group_to_individual_selected": true
  }
}'
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries"
  method := "POST"

  payload := strings.NewReader("{\n  \"inquiry\": {\n    \"effective_date\": \"2020-04-01\",\n    \"quoting_dental\": true,\n    \"quoting_vision\": true,\n    \"quoting_value_add\": true,\n    \"is_renewal\": false,\n    \"quoting_composite_rates\": false,\n    \"dental_contribution_strategy\": \"voluntary\",\n    \"vision_contribution_strategy\": \"voluntary\",\n    \"dental_vision_bundle_contribution_strategy\": \"voluntary\",\n    \"limited_medical_contribution_strategy\": \"voluntary\",\n    \"title\": \"G2I Quote - 2020-03-11\",\n    \"group_to_individual_selected\": true\n  }\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
  },
  "data": JSON.stringify({"inquiry":{"effective_date":"2020-04-01","quoting_dental":true,"quoting_vision":true,"quoting_value_add":true,"is_renewal":false,"quoting_composite_rates":false,"dental_contribution_strategy":"voluntary","vision_contribution_strategy":"voluntary","dental_vision_bundle_contribution_strategy":"voluntary","limited_medical_contribution_strategy":"voluntary","title":"G2I Quote - 2020-03-11","group_to_individual_selected":true}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"inquiry\": {\n    \"effective_date\": \"2020-04-01\",\n    \"quoting_dental\": true,\n    \"quoting_vision\": true,\n    \"quoting_value_add\": true,\n    \"is_renewal\": false,\n    \"quoting_composite_rates\": false,\n    \"dental_contribution_strategy\": \"voluntary\",\n    \"vision_contribution_strategy\": \"voluntary\",\n    \"dental_vision_bundle_contribution_strategy\": \"voluntary\",\n    \"limited_medical_contribution_strategy\": \"voluntary\",\n    \"title\": \"G2I Quote - 2020-03-11\",\n    \"group_to_individual_selected\": true\n  }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE")

$body = "{`n  `"inquiry`": {`n    `"effective_date`": `"2020-04-01`",`n    `"quoting_dental`": true,`n    `"quoting_vision`": true,`n    `"quoting_value_add`": true,`n    `"is_renewal`": false,`n    `"quoting_composite_rates`": false,`n    `"dental_contribution_strategy`": `"voluntary`",`n    `"vision_contribution_strategy`": `"voluntary`",`n    `"dental_vision_bundle_contribution_strategy`": `"voluntary`",`n    `"limited_medical_contribution_strategy`": `"voluntary`",`n    `"title`": `"G2I Quote - 2020-03-11`",`n    `"group_to_individual_selected`": true`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "slug": "EYZS4196"
}
```

### HTTP Request

`POST /api/companies/:slug/inquiries`

### Parameters

Parameter                                                   | Default   | Description
------------------------------------------------------------| --------- | -----------
<strong>effective_date</strong><strong>required</strong>    | N/A       | Effective Date in mm/dd/yyyy Format
quoting_dental                                              | false     | true / false
quoting_vision                                              | false     | true / false
quoting_value_add                                           | false     | true / false
is_renewal                                                  | false     | true / false
quoting_composite_rates                                     | false     | true / false
dental_contribution_strategy                                | N/A       | voluntary / contributory
vision_contribution_strategy                                | N/A       | voluntary / contributory
dental_vision_bundle_contribution_strategy                  | N/A       | voluntary / contributory
limited_medical_contribution_strategy                       | N/A       | voluntary / contributory
title                                                       | N/A       | Name of the Inquiry
group_to_individual_selected                                | false     | true / false

## Update an Inquiry

Use this endpoint to update an inquiry.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

```shell
curl --location --request PUT 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries/BCWN5429' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE' \
--data-raw '{
  "inquiry": {
    "effective_date": "2020-04-01",
    "quoting_dental": true,
    "quoting_vision": true,
    "quoting_value_add": true,
    "is_renewal": false,
    "quoting_composite_rates": false,
    "dental_contribution_strategy": "voluntary",
    "vision_contribution_strategy": "voluntary",
    "dental_vision_bundle_contribution_strategy": "voluntary",
    "limited_medical_contribution_strategy": "voluntary",
    "title": "Quote NEW - 2020-03-06",
    "group_to_individual_selected": false
  }
}'
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries/BCWN5429"
  method := "PUT"

  payload := strings.NewReader("{\n  \"inquiry\": {\n    \"effective_date\": \"2020-04-01\",\n    \"quoting_dental\": true,\n    \"quoting_vision\": true,\n    \"quoting_value_add\": true,\n    \"is_renewal\": false,\n    \"quoting_composite_rates\": false,\n    \"dental_contribution_strategy\": \"voluntary\",\n    \"vision_contribution_strategy\": \"voluntary\",\n    \"dental_vision_bundle_contribution_strategy\": \"voluntary\",\n    \"limited_medical_contribution_strategy\": \"voluntary\",\n    \"title\": \"Quote NEW - 2020-03-06\",\n    \"group_to_individual_selected\": false\n  }\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries/BCWN5429",
  "method": "PUT",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
  },
  "data": JSON.stringify({"inquiry":{"effective_date":"2020-04-01","quoting_dental":true,"quoting_vision":true,"quoting_value_add":true,"is_renewal":false,"quoting_composite_rates":false,"dental_contribution_strategy":"voluntary","vision_contribution_strategy":"voluntary","dental_vision_bundle_contribution_strategy":"voluntary","limited_medical_contribution_strategy":"voluntary","title":"Quote NEW - 2020-03-06","group_to_individual_selected":false}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries/BCWN5429"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"inquiry\": {\n    \"effective_date\": \"2020-04-01\",\n    \"quoting_dental\": true,\n    \"quoting_vision\": true,\n    \"quoting_value_add\": true,\n    \"is_renewal\": false,\n    \"quoting_composite_rates\": false,\n    \"dental_contribution_strategy\": \"voluntary\",\n    \"vision_contribution_strategy\": \"voluntary\",\n    \"dental_vision_bundle_contribution_strategy\": \"voluntary\",\n    \"limited_medical_contribution_strategy\": \"voluntary\",\n    \"title\": \"Quote NEW - 2020-03-06\",\n    \"group_to_individual_selected\": false\n  }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
[request setHTTPBody:postData];

[request setHTTPMethod:@"PUT"];

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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE")

$body = "{`n  `"inquiry`": {`n    `"effective_date`": `"2020-04-01`",`n    `"quoting_dental`": true,`n    `"quoting_vision`": true,`n    `"quoting_value_add`": true,`n    `"is_renewal`": false,`n    `"quoting_composite_rates`": false,`n    `"dental_contribution_strategy`": `"voluntary`",`n    `"vision_contribution_strategy`": `"voluntary`",`n    `"dental_vision_bundle_contribution_strategy`": `"voluntary`",`n    `"limited_medical_contribution_strategy`": `"voluntary`",`n    `"title`": `"Quote NEW - 2020-03-06`",`n    `"group_to_individual_selected`": false`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp/inquiries/BCWN5429' -Method 'PUT' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "title": "Quote NEW - 2020-03-06",
    "slug": "BCWN5429",
    "id": 130145,
    "penalty_for_company_not_providing_insurance": 0,
    "is_renewal": false,
    "group_to_individual_selected": false,
    "created_at": "2020-03-17T03:02:18.558-04:00",
    "other_inquiries_with_census": [
        {
            "id": 130146,
            "title": "G2I Quote - 2020-03-11",
            "group_to_individual_selected": true,
            "is_renewal": false,
            "company_id": 107654,
            "slug": "INBF8325",
            "created_at": "2020-03-17T03:03:17.556-04:00",
            "updated_at": "2020-03-17T03:03:26.196-04:00",
            "quoting_dental": true,
            "quoting_vision": true,
            "quoting_value_add": true,
            "dental_contribution_strategy": "voluntary",
            "vision_contribution_strategy": "voluntary",
            "dental_vision_bundle_contribution_strategy": "voluntary",
            "effective_date": "2020-04-01",
            "quoting_composite_rates": false,
            "quoting_limited_medical": false,
            "limited_medical_contribution_strategy": "voluntary",
            "current_plan_id": null
        }
    ],
    "quoting_dental": true,
    "quoting_vision": true,
    "quoting_value_add": true,
    "dental_contribution_strategy": "voluntary",
    "vision_contribution_strategy": "voluntary",
    "dental_vision_bundle_contribution_strategy": "voluntary",
    "effective_date": "2020-04-01",
    "tabs_for_plans_page": [
        "Medical",
        "Dental",
        "Vision"
    ],
    "individual_salary_adjustment_after_tax": 0.0,
    "quoting_composite_rates": false,
    "quoting_limited_medical": false,
    "limited_medical_contribution_strategy": "voluntary",
    "monthly_cost_of_individual_plans_for_all_employees_after_credit_and_salary_adjustment": {},
    "company_slug": "yNponia3pn8tpqygHSo8FhSp",
    "formatted_effective_date": "04/01/2020",
    "contribution": {
        "id": 125657,
        "inquiry_id": 130145,
        "medical_input_type": "percent",
        "medical_primary_percentage": 100.0,
        "medical_spouse_percentage": 100.0,
        "medical_dependent_percentage": 100.0,
        "medical_primary_currency": 0.0,
        "medical_spouse_currency": 0.0,
        "medical_dependent_currency": 0.0,
        "medical_single_percentage": 100.0,
        "medical_single_currency": 0.0,
        "medical_single_and_spouse_percentage": 100.0,
        "medical_single_and_spouse_currency": 0.0,
        "medical_single_and_children_percentage": 100.0,
        "medical_single_and_children_currency": 0.0,
        "medical_family_percentage": 100.0,
        "medical_family_currency": 0.0,
        "dental_vision_input_type": "percent",
        "dental_household_percentage": 100.0,
        "dental_household_currency": 0.0,
        "vision_household_percentage": 100.0,
        "vision_household_currency": 0.0,
        "dental_and_vision_bundle_household_percentage": 100.0,
        "dental_and_vision_bundle_household_currency": 0.0,
        "accident_household_percentage": 100.0,
        "life_household_percentage": 100.0,
        "telemedicine_household_percentage": 100.0,
        "ad_and_d_household_percentage": 100.0,
        "nurse_helpline_household_percentage": 100.0,
        "identity_theft_household_percentage": 100.0,
        "hospital_cash_household_percentage": 100.0,
        "legal_assistance_household_percentage": 100.0,
        "eap_household_percentage": 100.0,
        "travel_assistance_household_percentage": 100.0,
        "pharmacy_household_percentage": 100.0,
        "value_add_bundle_household_percentage": 100.0,
        "individual_salary_adjustment": 0,
        "dbl_household_percentage": 100.0,
        "composite_medical_input_type": "percent",
        "composite_medical_single_percentage": 100.0,
        "composite_medical_single_currency": 0.0,
        "composite_medical_single_and_spouse_percentage": 100.0,
        "composite_medical_single_and_spouse_currency": 0.0,
        "composite_medical_single_and_children_percentage": 100.0,
        "composite_medical_single_and_children_currency": 0.0,
        "composite_medical_family_percentage": 100.0,
        "composite_medical_family_currency": 0.0,
        "limited_medical_input_type": null,
        "limited_medical_household_percentage": 100.0,
        "limited_medical_household_currency": 0.0
    },
    "plan_selections": [],
    "current_plan": null
}
```

### HTTP Request

`PUT /api/companies/:company_slug/inquiries/:slug`

### Parameters

Parameter                                                   | Default   | Description
------------------------------------------------------------| --------- | -----------
<strong>effective_date</strong><strong>required</strong>    | N/A       | Effective Date in mm/dd/yyyy Format
quoting_dental                                              | false     | true / false
quoting_vision                                              | false     | true / false
quoting_value_add                                           | false     | true / false
is_renewal                                                  | false     | true / false
quoting_composite_rates                                     | false     | true / false
dental_contribution_strategy                                | N/A       | voluntary / contributory
vision_contribution_strategy                                | N/A       | voluntary / contributory
dental_vision_bundle_contribution_strategy                  | N/A       | voluntary / contributory
limited_medical_contribution_strategy                       | N/A       | voluntary / contributory
title                                                       | N/A       | Name of the Inquiry
group_to_individual_selected                                | false     | true / false

> <aside class="notice"> Note: To update contribution values, use the following example to update inquiry</aside>

```json
{
  "inquiry": {
    "contribution_attributes": {
      "id": 125652,
      "medical_input_type": "percent",
      "dental_vision_input_type": "percent",
      "limited_medical_input_type": "percent",
      "composite_medical_input_type": "percent",
      "medical_primary_percentage": 100,
      "medical_spouse_percentage": 100,
      "medical_dependent_percentage": 100,
      "medical_single_percentage": "50",
      "medical_single_and_spouse_percentage": "50",
      "medical_single_and_children_percentage": "50",
      "medical_family_percentage": "50",
      "dental_household_percentage": 100,
      "vision_household_percentage": 100,
      "limited_medical_household_percentage": 100,
      "dental_and_vision_bundle_household_percentage": 100,
      "value_add_bundle_household_percentage": 100,
      "accident_household_percentage": 100,
      "ad_and_d_household_percentage": 100,
      "eap_household_percentage": 100,
      "dbl_household_percentage": 100,
      "hospital_cash_household_percentage": 100,
      "identity_theft_household_percentage": 100,
      "legal_assistance_household_percentage": 100,
      "life_household_percentage": 100,
      "nurse_helpline_household_percentage": 100,
      "pharmacy_household_percentage": 100,
      "telemedicine_household_percentage": 100,
      "travel_assistance_household_percentage": 100,
      "medical_primary_currency": 0,
      "medical_spouse_currency": 0,
      "medical_dependent_currency": 0,
      "medical_single_currency": 0,
      "medical_single_and_spouse_currency": 0,
      "medical_single_and_children_currency": 0,
      "medical_family_currency": 0,
      "dental_household_currency": 0,
      "vision_household_currency": 0,
      "limited_medical_household_currency": 0,
      "dental_and_vision_bundle_household_currency": 0,
      "composite_medical_single_percentage": 100,
      "composite_medical_single_currency": 0,
      "composite_medical_single_and_spouse_percentage": 100,
      "composite_medical_single_and_spouse_currency": 0,
      "composite_medical_single_and_children_percentage": 100,
      "composite_medical_single_and_children_currency": 0,
      "composite_medical_family_percentage": 100,
      "composite_medical_family_currency": 0
    }
  },
  "request_for": "contributions",
  "return_inquiry": false
}
```
