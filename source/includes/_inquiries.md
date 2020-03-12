# Inquiries

## Get an Inquiry

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB79281' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%221bnWtzR2KGvd5TzX3Mv70w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%226p52sJXt9vgkF1j7l0yJMw%22%2C%22expiry%22%3A%221583909942%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: 1bnWtzR2KGvd5TzX3Mv70w' \
--header 'client: 6p52sJXt9vgkF1j7l0yJMw' \
--header 'expiry: 1583909942' \
--header 'uid: apidoc+broker@wellthie.com' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB79281"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%221bnWtzR2KGvd5TzX3Mv70w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%226p52sJXt9vgkF1j7l0yJMw%22%2C%22expiry%22%3A%221583909942%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "1bnWtzR2KGvd5TzX3Mv70w")
  req.Header.Add("client", "6p52sJXt9vgkF1j7l0yJMw")
  req.Header.Add("expiry", "1583909942")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB79281",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%221bnWtzR2KGvd5TzX3Mv70w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%226p52sJXt9vgkF1j7l0yJMw%22%2C%22expiry%22%3A%221583909942%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "1bnWtzR2KGvd5TzX3Mv70w",
    "client": "6p52sJXt9vgkF1j7l0yJMw",
    "expiry": "1583909942",
    "uid": "apidoc+broker@wellthie.com"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB79281"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%221bnWtzR2KGvd5TzX3Mv70w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%226p52sJXt9vgkF1j7l0yJMw%22%2C%22expiry%22%3A%221583909942%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"1bnWtzR2KGvd5TzX3Mv70w",
  @"client": @"6p52sJXt9vgkF1j7l0yJMw",
  @"expiry": @"1583909942",
  @"uid": @"apidoc+broker@wellthie.com"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%221bnWtzR2KGvd5TzX3Mv70w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%226p52sJXt9vgkF1j7l0yJMw%22%2C%22expiry%22%3A%221583909942%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "1bnWtzR2KGvd5TzX3Mv70w")
$headers.Add("client", "6p52sJXt9vgkF1j7l0yJMw")
$headers.Add("expiry", "1583909942")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB79281' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "title": null,
    "slug": "AGKB7928",
    "id": 130131,
    "penalty_for_company_not_providing_insurance": null,
    "is_renewal": false,
    "group_to_individual_selected": false,
    "created_at": "2020-03-06T06:42:46.334-05:00",
    "other_inquiries_with_census": [
        {
            "id": 130134,
            "title": "Quote - 2020-03-06",
            "group_to_individual_selected": true,
            "coverage_trash": null,
            "is_renewal": false,
            "company_id": 107637,
            "available_plan_ids_trash": null,
            "individual_salary_adjustment_trash": null,
            "view_access_token": null,
            "view_access_token_created_at": null,
            "slug": "JQLI9871",
            "archived_at": null,
            "ip_address": null,
            "user_agent": null,
            "created_at": "2020-03-06T08:44:52.001-05:00",
            "updated_at": "2020-03-06T08:46:54.126-05:00",
            "quoting_dental": false,
            "quoting_vision": false,
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
    "effective_date": "2019-04-01",
    "tabs_for_plans_page": [
        "Medical",
        "Dental",
        "Vision"
    ],
    "individual_salary_adjustment_after_tax": 0.0,
    "quoting_composite_rates": false,
    "quoting_limited_medical": false,
    "limited_medical_contribution_strategy": null,
    "monthly_cost_of_individual_plans_for_all_employees_after_credit_and_salary_adjustment": {},
    "company_slug": "shy8pmfek8ZpGKJYneD2g5TJ",
    "formatted_effective_date": "04/01/2019",
    "contribution": {
        "id": 125643,
        "inquiry_id": 130131,
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
        "created_at": "2020-03-06T06:42:46.343-05:00",
        "updated_at": "2020-03-06T06:42:46.343-05:00",
        "individual_salary_adjustment": 0,
        "dbl_household_percentage": 100.0,
        "limited_medical_household_percentage_trash": null,
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
    "current_plan": {
        "id": 4003,
        "current_plan_issuer": "Current Plan Issuer",
        "name": "Current Plan Name",
        "company_id": 107637,
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

Use this endpoint to fetch a particular inquiry.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET /api/inquiries/:slug`

### Parameters

No parameters required.


## Create an Inquiry

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22U5FgbM3skufrrJUTNaCRlQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910013%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: U5FgbM3skufrrJUTNaCRlQ' \
--header 'client: whsAaLkuUQbDUo9O5BJyug' \
--header 'expiry: 1583910013' \
--header 'uid: apidoc+broker@wellthie.com' \
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
    "title": "NEW Quote - 2020-03-06",
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries"
  method := "POST"

  payload := strings.NewReader("{\n  \"inquiry\": {\n    \"effective_date\": \"2020-04-01\",\n    \"quoting_dental\": true,\n    \"quoting_vision\": true,\n    \"quoting_value_add\": true,\n    \"is_renewal\": false,\n    \"quoting_composite_rates\": false,\n    \"dental_contribution_strategy\": \"voluntary\",\n    \"vision_contribution_strategy\": \"voluntary\",\n    \"dental_vision_bundle_contribution_strategy\": \"voluntary\",\n    \"limited_medical_contribution_strategy\": \"voluntary\",\n    \"title\": \"NEW Quote - 2020-03-06\",\n    \"group_to_individual_selected\": false\n  }\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22U5FgbM3skufrrJUTNaCRlQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910013%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "U5FgbM3skufrrJUTNaCRlQ")
  req.Header.Add("client", "whsAaLkuUQbDUo9O5BJyug")
  req.Header.Add("expiry", "1583910013")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22U5FgbM3skufrrJUTNaCRlQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910013%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "U5FgbM3skufrrJUTNaCRlQ",
    "client": "whsAaLkuUQbDUo9O5BJyug",
    "expiry": "1583910013",
    "uid": "apidoc+broker@wellthie.com"
  },
  "data": JSON.stringify({"inquiry":{"effective_date":"2020-04-01","quoting_dental":true,"quoting_vision":true,"quoting_value_add":true,"is_renewal":false,"quoting_composite_rates":false,"dental_contribution_strategy":"voluntary","vision_contribution_strategy":"voluntary","dental_vision_bundle_contribution_strategy":"voluntary","limited_medical_contribution_strategy":"voluntary","title":"NEW Quote - 2020-03-06","group_to_individual_selected":false}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22U5FgbM3skufrrJUTNaCRlQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910013%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"U5FgbM3skufrrJUTNaCRlQ",
  @"client": @"whsAaLkuUQbDUo9O5BJyug",
  @"expiry": @"1583910013",
  @"uid": @"apidoc+broker@wellthie.com"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"inquiry\": {\n    \"effective_date\": \"2020-04-01\",\n    \"quoting_dental\": true,\n    \"quoting_vision\": true,\n    \"quoting_value_add\": true,\n    \"is_renewal\": false,\n    \"quoting_composite_rates\": false,\n    \"dental_contribution_strategy\": \"voluntary\",\n    \"vision_contribution_strategy\": \"voluntary\",\n    \"dental_vision_bundle_contribution_strategy\": \"voluntary\",\n    \"limited_medical_contribution_strategy\": \"voluntary\",\n    \"title\": \"NEW Quote - 2020-03-06\",\n    \"group_to_individual_selected\": false\n  }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22U5FgbM3skufrrJUTNaCRlQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910013%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "U5FgbM3skufrrJUTNaCRlQ")
$headers.Add("client", "whsAaLkuUQbDUo9O5BJyug")
$headers.Add("expiry", "1583910013")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = "{`n  `"inquiry`": {`n    `"effective_date`": `"2020-04-01`",`n    `"quoting_dental`": true,`n    `"quoting_vision`": true,`n    `"quoting_value_add`": true,`n    `"is_renewal`": false,`n    `"quoting_composite_rates`": false,`n    `"dental_contribution_strategy`": `"voluntary`",`n    `"vision_contribution_strategy`": `"voluntary`",`n    `"dental_vision_bundle_contribution_strategy`": `"voluntary`",`n    `"limited_medical_contribution_strategy`": `"voluntary`",`n    `"title`": `"NEW Quote - 2020-03-06`",`n    `"group_to_individual_selected`": false`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "slug": "EYZS4196"
}
```

Use this endpoint to create a new inquiry for a company.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

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

```shell
curl --location --request PUT 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries/AGKB7928' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22Gs6TGSot4p-vjsBchOoiHg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910750%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: Gs6TGSot4p-vjsBchOoiHg' \
--header 'client: whsAaLkuUQbDUo9O5BJyug' \
--header 'expiry: 1583910750' \
--header 'uid: apidoc+broker@wellthie.com' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries/AGKB7928"
  method := "PUT"

  payload := strings.NewReader("{\n  \"inquiry\": {\n    \"effective_date\": \"2020-04-01\",\n    \"quoting_dental\": true,\n    \"quoting_vision\": true,\n    \"quoting_value_add\": true,\n    \"is_renewal\": false,\n    \"quoting_composite_rates\": false,\n    \"dental_contribution_strategy\": \"voluntary\",\n    \"vision_contribution_strategy\": \"voluntary\",\n    \"dental_vision_bundle_contribution_strategy\": \"voluntary\",\n    \"limited_medical_contribution_strategy\": \"voluntary\",\n    \"title\": \"Quote NEW - 2020-03-06\",\n    \"group_to_individual_selected\": false\n  }\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22Gs6TGSot4p-vjsBchOoiHg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910750%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "Gs6TGSot4p-vjsBchOoiHg")
  req.Header.Add("client", "whsAaLkuUQbDUo9O5BJyug")
  req.Header.Add("expiry", "1583910750")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries/AGKB7928",
  "method": "PUT",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22Gs6TGSot4p-vjsBchOoiHg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910750%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "Gs6TGSot4p-vjsBchOoiHg",
    "client": "whsAaLkuUQbDUo9O5BJyug",
    "expiry": "1583910750",
    "uid": "apidoc+broker@wellthie.com"
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries/AGKB7928"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22Gs6TGSot4p-vjsBchOoiHg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910750%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"Gs6TGSot4p-vjsBchOoiHg",
  @"client": @"whsAaLkuUQbDUo9O5BJyug",
  @"expiry": @"1583910750",
  @"uid": @"apidoc+broker@wellthie.com"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22Gs6TGSot4p-vjsBchOoiHg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583910750%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "Gs6TGSot4p-vjsBchOoiHg")
$headers.Add("client", "whsAaLkuUQbDUo9O5BJyug")
$headers.Add("expiry", "1583910750")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = "{`n  `"inquiry`": {`n    `"effective_date`": `"2020-04-01`",`n    `"quoting_dental`": true,`n    `"quoting_vision`": true,`n    `"quoting_value_add`": true,`n    `"is_renewal`": false,`n    `"quoting_composite_rates`": false,`n    `"dental_contribution_strategy`": `"voluntary`",`n    `"vision_contribution_strategy`": `"voluntary`",`n    `"dental_vision_bundle_contribution_strategy`": `"voluntary`",`n    `"limited_medical_contribution_strategy`": `"voluntary`",`n    `"title`": `"Quote NEW - 2020-03-06`",`n    `"group_to_individual_selected`": false`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/inquiries/AGKB7928' -Method 'PUT' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "title": "Quote NEW - 2020-03-06",
    "slug": "AGKB7928",
    "id": 130131,
    "penalty_for_company_not_providing_insurance": null,
    "is_renewal": false,
    "group_to_individual_selected": false,
    "created_at": "2020-03-06T06:42:46.334-05:00",
    "other_inquiries_with_census": [
        {
            "id": 130134,
            "title": "Quote - 2020-03-06",
            "group_to_individual_selected": true,
            "coverage_trash": null,
            "is_renewal": false,
            "company_id": 107637,
            "available_plan_ids_trash": null,
            "individual_salary_adjustment_trash": null,
            "view_access_token": null,
            "view_access_token_created_at": null,
            "slug": "JQLI9871",
            "archived_at": null,
            "ip_address": null,
            "user_agent": null,
            "created_at": "2020-03-06T08:44:52.001-05:00",
            "updated_at": "2020-03-06T08:46:54.126-05:00",
            "quoting_dental": false,
            "quoting_vision": false,
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
    "company_slug": "shy8pmfek8ZpGKJYneD2g5TJ",
    "formatted_effective_date": "04/01/2020",
    "contribution": {
        "id": 125643,
        "inquiry_id": 130131,
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
        "created_at": "2020-03-06T06:42:46.343-05:00",
        "updated_at": "2020-03-06T06:42:46.343-05:00",
        "individual_salary_adjustment": 0,
        "dbl_household_percentage": 100.0,
        "limited_medical_household_percentage_trash": null,
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
    "current_plan": {
        "id": 4003,
        "current_plan_issuer": "Current Plan Issuer",
        "name": "Current Plan Name",
        "company_id": 107637,
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

Use this endpoint to update an inquiry.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

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

## Get Plan Selections

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plan_selections' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22AL96HOb0aqN1gZ9eRRszkg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583911500%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: AL96HOb0aqN1gZ9eRRszkg' \
--header 'client: whsAaLkuUQbDUo9O5BJyug' \
--header 'expiry: 1583911500' \
--header 'uid: apidoc+broker@wellthie.com' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plan_selections"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22AL96HOb0aqN1gZ9eRRszkg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583911500%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "AL96HOb0aqN1gZ9eRRszkg")
  req.Header.Add("client", "whsAaLkuUQbDUo9O5BJyug")
  req.Header.Add("expiry", "1583911500")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plan_selections",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22AL96HOb0aqN1gZ9eRRszkg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583911500%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "AL96HOb0aqN1gZ9eRRszkg",
    "client": "whsAaLkuUQbDUo9O5BJyug",
    "expiry": "1583911500",
    "uid": "apidoc+broker@wellthie.com"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plan_selections"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22AL96HOb0aqN1gZ9eRRszkg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583911500%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"AL96HOb0aqN1gZ9eRRszkg",
  @"client": @"whsAaLkuUQbDUo9O5BJyug",
  @"expiry": @"1583911500",
  @"uid": @"apidoc+broker@wellthie.com"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22AL96HOb0aqN1gZ9eRRszkg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22whsAaLkuUQbDUo9O5BJyug%22%2C%22expiry%22%3A%221583911500%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "AL96HOb0aqN1gZ9eRRszkg")
$headers.Add("client", "whsAaLkuUQbDUo9O5BJyug")
$headers.Add("expiry", "1583911500")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plan_selections' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plan_selections`

### Parameters

No parameters required.


## Get Individual Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/XQEJ2145/individual_quotes' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D' \
--header 'access-token: ' \
--header 'client: ' \
--header 'expiry: ' \
--header 'uid: ' \
--header 'Authorization: Bearer ryMvWXKNIQeaJCDWfwlFNg' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/XQEJ2145/individual_quotes"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D")
  req.Header.Add("access-token", "")
  req.Header.Add("client", "")
  req.Header.Add("expiry", "")
  req.Header.Add("uid", "")
  req.Header.Add("Authorization", "Bearer ryMvWXKNIQeaJCDWfwlFNg")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/XQEJ2145/individual_quotes",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D",
    "access-token": "",
    "client": "",
    "expiry": "",
    "uid": "",
    "Authorization": "Bearer ryMvWXKNIQeaJCDWfwlFNg"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/XQEJ2145/individual_quotes"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D",
  @"access-token": @"",
  @"client": @"",
  @"expiry": @"",
  @"uid": @"",
  @"Authorization": @"Bearer ryMvWXKNIQeaJCDWfwlFNg"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D")
$headers.Add("access-token", "")
$headers.Add("client", "")
$headers.Add("expiry", "")
$headers.Add("uid", "")
$headers.Add("Authorization", "Bearer ryMvWXKNIQeaJCDWfwlFNg")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/XQEJ2145/individual_quotes' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/individual_quotes`

### Parameters

No parameters required.

## Create Download Excel (Pending Refactor)

```shell
curl -X POST "http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/inquiries/:inquiry_slug/download_excel" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
     -d '{"excel_data":"DATA","excel_file_name":"INS NONDIFF PPO Silver - AKRU - Employee Cost Breakdown","inquiry_slug":"NDQJ3912"}'
```

```go
```

```javascript
```

```objective_c
```

```powershell
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`POST /api/inquiries/:inquiry_slug/download_excel`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
email        | N/A     | User's email address  | true
password     | N/A     | User's password       | true
