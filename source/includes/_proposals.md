# Proposals

## Get Selected Inquiries of a company

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/inquiries?selected_inquiries=JXID6718,JQLI9871' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22ftj2xIRsDvprSBzBAEZc1w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923117%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: ftj2xIRsDvprSBzBAEZc1w' \
--header 'client: pkevB8VD4yONukgbtPUFFw' \
--header 'expiry: 1583923117' \
--header 'uid: apidoc+broker@wellthie.com' \
--header 'Authorization: Bearer PfjWVebzEivqQZd4Y19ljw' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/inquiries?selected_inquiries=JXID6718,JQLI9871"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22ftj2xIRsDvprSBzBAEZc1w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923117%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "ftj2xIRsDvprSBzBAEZc1w")
  req.Header.Add("client", "pkevB8VD4yONukgbtPUFFw")
  req.Header.Add("expiry", "1583923117")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")
  req.Header.Add("Authorization", "Bearer PfjWVebzEivqQZd4Y19ljw")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/inquiries?selected_inquiries=JXID6718,JQLI9871",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22ftj2xIRsDvprSBzBAEZc1w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923117%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "ftj2xIRsDvprSBzBAEZc1w",
    "client": "pkevB8VD4yONukgbtPUFFw",
    "expiry": "1583923117",
    "uid": "apidoc+broker@wellthie.com",
    "Authorization": "Bearer PfjWVebzEivqQZd4Y19ljw"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/inquiries?selected_inquiries=JXID6718,JQLI9871"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22ftj2xIRsDvprSBzBAEZc1w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923117%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"ftj2xIRsDvprSBzBAEZc1w",
  @"client": @"pkevB8VD4yONukgbtPUFFw",
  @"expiry": @"1583923117",
  @"uid": @"apidoc+broker@wellthie.com",
  @"Authorization": @"Bearer PfjWVebzEivqQZd4Y19ljw"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22ftj2xIRsDvprSBzBAEZc1w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923117%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "ftj2xIRsDvprSBzBAEZc1w")
$headers.Add("client", "pkevB8VD4yONukgbtPUFFw")
$headers.Add("expiry", "1583923117")
$headers.Add("uid", "apidoc+broker@wellthie.com")
$headers.Add("Authorization", "Bearer PfjWVebzEivqQZd4Y19ljw")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/inquiries?selected_inquiries=JXID6718,JQLI9871' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
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
                "updated_at": "2020-03-17T03:09:10.487-04:00",
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
        "plan_selections": [
            {
                "id": 136327,
                "individual_plan_id": null,
                "medical_plan_id": 78720,
                "ancillary_plan_id": null,
                "ancillary_plan_type": null,
                "selected_for_quote": true,
                "selected_for_enrollment": false,
                "order": 1
            }
        ],
        "current_plan": null
    },
    {
        "title": "G2I Quote - 2020-03-11",
        "slug": "INBF8325",
        "id": 130146,
        "penalty_for_company_not_providing_insurance": 0,
        "is_renewal": false,
        "group_to_individual_selected": true,
        "created_at": "2020-03-17T03:03:17.556-04:00",
        "other_inquiries_with_census": [
            {
                "id": 130145,
                "title": "Quote NEW - 2020-03-06",
                "group_to_individual_selected": false,
                "is_renewal": false,
                "company_id": 107654,
                "slug": "BCWN5429",
                "created_at": "2020-03-17T03:02:18.558-04:00",
                "updated_at": "2020-03-17T03:09:19.867-04:00",
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
        "company_slug": "yNponia3pn8tpqygHSo8FhSp",
        "formatted_effective_date": "04/01/2020",
        "contribution": {
            "id": 125658,
            "inquiry_id": 130146,
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
                "id": 136326,
                "individual_plan_id": null,
                "medical_plan_id": 78720,
                "ancillary_plan_id": null,
                "ancillary_plan_type": null,
                "selected_for_quote": true,
                "selected_for_enrollment": false,
                "order": 1
            }
        ],
        "current_plan": null
    }
]
```

Use this endpoint to retrieve details of selected inquiries of a company.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET            /api/proposals/:company_slug/inquiries?selected_inquiries=:inquiry_slug,:inquiry_slug`

### Parameters

No parameters required.

## Get Group Plans for inquiries

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans?selected_inquiries=JXID6718,JQLI9871' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22XsT2kpRKu9D3EanAwyNCFw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923305%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: XsT2kpRKu9D3EanAwyNCFw' \
--header 'client: pkevB8VD4yONukgbtPUFFw' \
--header 'expiry: 1583923305' \
--header 'uid: apidoc+broker@wellthie.com' \
--header 'Authorization: Bearer ftj2xIRsDvprSBzBAEZc1w' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans?selected_inquiries=JXID6718,JQLI9871"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22XsT2kpRKu9D3EanAwyNCFw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923305%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "XsT2kpRKu9D3EanAwyNCFw")
  req.Header.Add("client", "pkevB8VD4yONukgbtPUFFw")
  req.Header.Add("expiry", "1583923305")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")
  req.Header.Add("Authorization", "Bearer ftj2xIRsDvprSBzBAEZc1w")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans?selected_inquiries=JXID6718,JQLI9871",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22XsT2kpRKu9D3EanAwyNCFw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923305%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "XsT2kpRKu9D3EanAwyNCFw",
    "client": "pkevB8VD4yONukgbtPUFFw",
    "expiry": "1583923305",
    "uid": "apidoc+broker@wellthie.com",
    "Authorization": "Bearer ftj2xIRsDvprSBzBAEZc1w"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans?selected_inquiries=JXID6718,JQLI9871"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22XsT2kpRKu9D3EanAwyNCFw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923305%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"XsT2kpRKu9D3EanAwyNCFw",
  @"client": @"pkevB8VD4yONukgbtPUFFw",
  @"expiry": @"1583923305",
  @"uid": @"apidoc+broker@wellthie.com",
  @"Authorization": @"Bearer ftj2xIRsDvprSBzBAEZc1w"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22XsT2kpRKu9D3EanAwyNCFw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923305%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "XsT2kpRKu9D3EanAwyNCFw")
$headers.Add("client", "pkevB8VD4yONukgbtPUFFw")
$headers.Add("expiry", "1583923305")
$headers.Add("uid", "apidoc+broker@wellthie.com")
$headers.Add("Authorization", "Bearer ftj2xIRsDvprSBzBAEZc1w")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans?selected_inquiries=JXID6718,JQLI9871' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "JXID6718": [
        {
            "promotional_label": null,
            "issuer_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/173/main/oscar_logo_blue_2020-wg39.png?1573759981",
            "id": 78717,
            "name": "Oscar Circle Bronze $8150 (No FP)",
            "service_area_id": 4334,
            "highlight_1": {
                "icon": "icon--metal",
                "value": "Bronze"
            },
            "highlight_2": {
                "icon": "icon--network",
                "value": "EPO"
            },
            "highlight_3": {
                "icon": "icon--add-on",
                "value": "PCP $0"
            },
            "highlight_4": null,
            "highlight_5": null,
            "highlight_6": null,
            "available_exchanges": {
                "icon": "icon--exchange-type",
                "value": "Available Off Exchange"
            },
            "sbc_download_url": null,
            "network_url": "https://www.hioscar.com/search/",
            "formulary_url": "https://www.hioscar.com/search/",
            "hios_plan_identifier": "74289NY2780024",
            "plan_year": 2020,
            "tags": [
                "bronze",
                "epo",
                "off_exchange"
            ],
            "group_or_individual_plan_type": "Group",
            "metal_level_name": "Bronze",
            "on_exchange": false,
            "off_exchange": true,
            "plan_description": null,
            "plan_detail_header": null,
            "plan_detail_items": null,
            "plan_detail_footer": null,
            "composite_rating": false,
            "hsa_eligible": false,
            "issuer": {
                "id": 173,
                "name": "Oscar",
                "parameterized_name": "oscar",
                "composite_ee_factor": null,
                "composite_es_factor": null,
                "composite_ec_factor": null,
                "composite_ef_factor": null,
                "enrollment_content_area_name": "Enrollment Instructions: Oscar Plans",
                "main_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/173/main/oscar_logo_blue_2020-wg39.png?1573759981",
                "issuer_enrollment_resources": [
                    {
                        "name": "Oscar Business Broker Login",
                        "product_type": "Medical",
                        "resource_type": "link",
                        "display_link_url": "https://business.hioscar.com/login",
                        "sort_order": 10
                    },
                    {
                        "name": "Oscar Auto-Renewal Business Enrollment Form",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/805/original/o4b_-_ny_2017_2018_business_enrollment_form__auto-renewal__v04-ao6.pdf?1509036239",
                        "sort_order": 30
                    },
                    {
                        "name": "Oscar Business Enrollment Form",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/806/original/o4b_businessenrollmentform_ny_2017-db81.pdf?1509036301",
                        "sort_order": 20
                    },
                    {
                        "name": "Oscar Employee Enrollment Form",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/803/original/oscar-xa19.pdf?1509036019",
                        "sort_order": 40
                    },
                    {
                        "name": "Oscar Auto-Renewal Employee Enrollment Form",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/804/original/oscar%20employee%20auto-renewal%20form-hy63.pdf?1509036116",
                        "sort_order": 50
                    },
                    {
                        "name": "Oscar for Business Underwriting Guidelines",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/934/original/sgunderwriting03-2017_v9-hd83.pdf?1512419195",
                        "sort_order": 60
                    }
                ]
            },
            "medical_plan_benefit": {
                "medical_plan_id": 78717,
                "medical_deductible_single": "$8,150",
                "medical_deductible_family": "$16,300",
                "maximum_out_of_pocket_limit_single": "$8,150",
                "maximum_out_of_pocket_limit_family": "$16,300",
                "pcp": "$0",
                "specialist": "$0",
                "preventive_care": "$0",
                "inpatient_facility": "$0",
                "outpatient_facility": "$0",
                "outpatient_physician_surgeon": "$0",
                "imaging": "$0",
                "durable_medical_equipment": "$0",
                "diagnostic": "$0",
                "emergency_room": "$0",
                "urgent_care": "$0",
                "ambulance": "$0",
                "rx_deductible": null,
                "generic": "$0",
                "formulary_brand": "$0",
                "non_formulary_brand": "$0",
                "mail_order": "2.5x",
                "adult_vision_exam": null,
                "adult_preventive_dental": null,
                "adult_major_dental": null,
                "adult_eyewear": null,
                "adult_emergency_dental": null,
                "eyewear": null,
                "pediatric_vision_exam": null,
                "pediatric_preventive_dental": null,
                "pediatric_orthodontics": null,
                "pediatric_major_dental": null,
                "pediatric_eyewear": null,
                "pediatric_emergency_dental": null,
                "pcp_telemedicine": null,
                "nutritionist_telemedicine": null,
                "deductible_single_number": 8150,
                "deductible_family_number": 16300,
                "moop_single_number": 8150,
                "moop_family_number": 16300,
                "benefit_rows_with_header": {
                    "Main Benefits": {
                        "Deductible - Single": "medical_deductible_single",
                        "Deductible - Family": "medical_deductible_family",
                        "Out of Pocket Max - Single": "maximum_out_of_pocket_limit_single",
                        "Out of Pocket Max - Family": "maximum_out_of_pocket_limit_family"
                    },
                    "Outpatient & Inpatient Services": {
                        "Primary Care Visit": "pcp",
                        "Specialist Visit": "specialist",
                        "Preventive Care": "preventive_care",
                        "Inpatient Facility": "inpatient_facility",
                        "Outpatient Facility": "outpatient_facility",
                        "Outpatient Surgery": "outpatient_physician_surgeon"
                    },
                    "Medical Equipment & Tests": {
                        "Imaging": "imaging",
                        "Durable Medical Equipment": "durable_medical_equipment",
                        "Diagnostic": "diagnostic"
                    },
                    "Emergency Services": {
                        "Emergency Room Visit": "emergency_room",
                        "Urgent Care": "urgent_care",
                        "Ambulance": "ambulance"
                    },
                    "Prescription Drug Coverage": {
                        "RX Code": "rx_code",
                        "Prescription Drug Deductible": "rx_deductible",
                        "Generic Brand Prescriptions": "generic",
                        "Formulary Brand Prescriptions": "formulary_brand",
                        "Non-Formulary Brand Prescriptions": "non_formulary_brand",
                        "Mail Order": "mail_order"
                    },
                    "Add-on Dental and Vision": {
                        "Adult Vision Exam": "adult_vision_exam",
                        "Adult Preventive Dental": "adult_preventive_dental",
                        "Adult Major Dental": "adult_major_dental",
                        "Adult Eyewear": "adult_eyewear",
                        "Adult Emergency Dental": "adult_emergency_dental",
                        "Eyewear": "eyewear",
                        "Pediatric Vision Exam": "pediatric_vision_exam",
                        "Pediatric Preventive Dental": "pediatric_preventive_dental",
                        "Pediatric Orthodontics": "pediatric_orthodontics",
                        "Pediatric Major Dental": "pediatric_major_dental",
                        "Pediatric Eyewear": "pediatric_eyewear",
                        "Pediatric Emergency Dental": "pediatric_emergency_dental",
                        "PCP Telemedicine": "pcp_telemedicine",
                        "Nutritionist Telemedicine": "nutritionist_telemedicine"
                    }
                },
                "view_detail_benefits": [
                    "pcp",
                    "imaging",
                    "formulary_brand",
                    "specialist",
                    "generic",
                    "non_formulary_brand"
                ],
                "out_of_network_benfit_row_header": {
                    "Main Benefits": {
                        "Deductible - Single": "medical_deductible_single_out_network",
                        "Deductible - Family": "medical_deductible_family_out_network",
                        "Out of Pocket Max - Single": "maximum_out_of_pocket_limit_single_out_network",
                        "Out of Pocket Max - Family": "maximum_out_of_pocket_limit_family_out_network"
                    },
                    "Outpatient & Inpatient Services": {
                        "Primary Care Visit": "pcp_out_network",
                        "Specialist Visit": "specialist_out_network",
                        "Preventive Care": "preventive_care_out_network",
                        "Inpatient Facility": "inpatient_facility_out_network",
                        "Outpatient Facility": "outpatient_facility_out_network",
                        "Outpatient Surgery": "outpatient_physician_surgeon_out_network"
                    },
                    "Medical Equipment & Tests": {
                        "Imaging": "imaging_out_network",
                        "Durable Medical Equipment": "durable_medical_equipment_out_network",
                        "Diagnostic": "diagnostic_out_network"
                    },
                    "Emergency Services": {
                        "Emergency Room Visit": "emergency_room_out_network",
                        "Urgent Care": "urgent_care_out_network",
                        "Ambulance": "ambulance_out_network"
                    },
                    "Prescription Drug Coverage": {
                        "RX Code": "rx_code",
                        "Prescription Drug Deductible": "rx_deductible_out_network",
                        "Generic Brand Prescriptions": "generic_out_network",
                        "Formulary Brand Prescriptions": "formulary_brand_out_network",
                        "Non-Formulary Brand Prescriptions": "non_formulary_brand_out_network",
                        "Mail Order": "mail_order_out_network"
                    },
                    "Add-on Dental and Vision": {
                        "Adult Vision Exam": "adult_vision_exam_out_network",
                        "Adult Preventive Dental": "adult_preventive_dental_out_network",
                        "Adult Major Dental": "adult_major_dental_out_network",
                        "Adult Eyewear": "adult_eyewear_out_network",
                        "Adult Emergency Dental": "adult_emergency_dental_out_network",
                        "Eyewear": "",
                        "Pediatric Vision Exam": "pediatric_vision_exam_out_network",
                        "Pediatric Preventive Dental": "pediatric_preventive_dental_out_network",
                        "Pediatric Orthodontics": "pediatric_orthodontics_out_network",
                        "Pediatric Major Dental": "pediatric_major_dental_out_network",
                        "Pediatric Eyewear": "pediatric_eyewear_out_network",
                        "Pediatric Emergency Dental": "pediatric_emergency_dental_out_network",
                        "PCP Telemedicine": "pcp_telemedicine_out_network",
                        "Nutritionist Telemedicine": "nutritionist_telemedicine_out_network"
                    }
                },
                "maximum_out_of_pocket_limit_single_out_network": "Not Covered",
                "maximum_out_of_pocket_limit_family_out_network": "Not Covered",
                "medical_deductible_single_out_network": "Not Covered",
                "medical_deductible_family_out_network": "Not Covered",
                "pcp_out_network": "Not Covered",
                "specialist_out_network": "Not Covered",
                "preventive_care_out_network": "Not Covered",
                "generic_out_network": "Not Covered",
                "formulary_brand_out_network": "Not Covered",
                "non_formulary_brand_out_network": "Not Covered",
                "non_preferred_generic_out_network": null,
                "non_preferred_brand_out_network": null,
                "rx_deductible_out_network": null,
                "rx_initial_coverage_limit_out_network": null,
                "adult_emergency_dental_out_network": null,
                "adult_eyewear_out_network": null,
                "adult_major_dental_out_network": null,
                "adult_preventive_dental_out_network": null,
                "adult_vision_exam_out_network": null,
                "ambulance_out_network": "Not Covered",
                "ambulatory_surgery_center_out_network": null,
                "chiropractor_out_network": null,
                "clinical_diagnostic_lab_out_network": null,
                "clinical_diagnostic_mri_out_network": "Not Covered",
                "clinical_diagnostic_radiation_out_network": null,
                "clinical_diagnostic_xray_out_network": "Not Covered",
                "diabetic_supplies_out_network": null,
                "diagnostic_out_network": "Not Covered",
                "durable_medical_equipment_out_network": "Not Covered",
                "emergency_room_out_network": "Not Covered",
                "imaging_out_network": "Not Covered",
                "inpatient_acute_out_network": null,
                "inpatient_facility_out_network": "Not Covered",
                "inpatient_mental_health_out_network": null,
                "inpatient_physician_surgeon_out_network": "Not Covered",
                "mail_order_out_network": null,
                "nutritionist_telemedicine_out_network": null,
                "outpatient_facility_out_network": "Not Covered",
                "outpatient_mental_behavior_health_out_network": null,
                "outpatient_physician_surgeon_out_network": "Not Covered",
                "pcp_telemedicine_out_network": null,
                "pediatric_emergency_dental_out_network": null,
                "pediatric_eyewear_out_network": null,
                "pediatric_major_dental_out_network": null,
                "pediatric_orthodontics_out_network": null,
                "pediatric_preventive_dental_out_network": null,
                "pediatric_vision_exam_out_network": null,
                "physical_occupational_speech_out_network": null,
                "preferred_brand_out_network": null,
                "preferred_generic_out_network": null,
                "preventive_dental_out_network": null,
                "prosthetics_out_network": null,
                "routine_eye_exam_out_network": null,
                "skilled_nursing_facility_out_network": "Not Covered",
                "specialty_out_network": "Not Covered",
                "urgent_care_out_network": "Not Covered",
                "pcp_percentage_number_after_deductible": null,
                "pcp_amount_number_after_deductible": null,
                "pcp_percentage_number_before_deductible": null,
                "pcp_amount_number_before_deductible": 0
            },
            "carrier_plan_identifier": null,
            "model_name": "medical_plans"
        }
    ],
    "JQLI9871": [
        {
            "promotional_label": null,
            "issuer_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/173/main/oscar_logo_blue_2020-wg39.png?1573759981",
            "id": 78717,
            "name": "Oscar Circle Bronze $8150 (No FP)",
            "service_area_id": 4334,
            "highlight_1": {
                "icon": "icon--metal",
                "value": "Bronze"
            },
            "highlight_2": {
                "icon": "icon--network",
                "value": "EPO"
            },
            "highlight_3": {
                "icon": "icon--add-on",
                "value": "PCP $0"
            },
            "highlight_4": null,
            "highlight_5": null,
            "highlight_6": null,
            "available_exchanges": {
                "icon": "icon--exchange-type",
                "value": "Available Off Exchange"
            },
            "sbc_download_url": null,
            "network_url": "https://www.hioscar.com/search/",
            "formulary_url": "https://www.hioscar.com/search/",
            "hios_plan_identifier": "74289NY2780024",
            "plan_year": 2020,
            "tags": [
                "bronze",
                "epo",
                "off_exchange"
            ],
            "group_or_individual_plan_type": "Group",
            "metal_level_name": "Bronze",
            "on_exchange": false,
            "off_exchange": true,
            "plan_description": null,
            "plan_detail_header": null,
            "plan_detail_items": null,
            "plan_detail_footer": null,
            "composite_rating": false,
            "hsa_eligible": false,
            "issuer": {
                "id": 173,
                "name": "Oscar",
                "parameterized_name": "oscar",
                "composite_ee_factor": null,
                "composite_es_factor": null,
                "composite_ec_factor": null,
                "composite_ef_factor": null,
                "enrollment_content_area_name": "Enrollment Instructions: Oscar Plans",
                "main_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/173/main/oscar_logo_blue_2020-wg39.png?1573759981",
                "issuer_enrollment_resources": [
                    {
                        "name": "Oscar Business Broker Login",
                        "product_type": "Medical",
                        "resource_type": "link",
                        "display_link_url": "https://business.hioscar.com/login",
                        "sort_order": 10
                    },
                    {
                        "name": "Oscar Auto-Renewal Business Enrollment Form",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/805/original/o4b_-_ny_2017_2018_business_enrollment_form__auto-renewal__v04-ao6.pdf?1509036239",
                        "sort_order": 30
                    },
                    {
                        "name": "Oscar Business Enrollment Form",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/806/original/o4b_businessenrollmentform_ny_2017-db81.pdf?1509036301",
                        "sort_order": 20
                    },
                    {
                        "name": "Oscar Employee Enrollment Form",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/803/original/oscar-xa19.pdf?1509036019",
                        "sort_order": 40
                    },
                    {
                        "name": "Oscar Auto-Renewal Employee Enrollment Form",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/804/original/oscar%20employee%20auto-renewal%20form-hy63.pdf?1509036116",
                        "sort_order": 50
                    },
                    {
                        "name": "Oscar for Business Underwriting Guidelines",
                        "product_type": "Medical",
                        "resource_type": "file",
                        "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/934/original/sgunderwriting03-2017_v9-hd83.pdf?1512419195",
                        "sort_order": 60
                    }
                ]
            },
            "medical_plan_benefit": {
                "medical_plan_id": 78717,
                "medical_deductible_single": "$8,150",
                "medical_deductible_family": "$16,300",
                "maximum_out_of_pocket_limit_single": "$8,150",
                "maximum_out_of_pocket_limit_family": "$16,300",
                "pcp": "$0",
                "specialist": "$0",
                "preventive_care": "$0",
                "inpatient_facility": "$0",
                "outpatient_facility": "$0",
                "outpatient_physician_surgeon": "$0",
                "imaging": "$0",
                "durable_medical_equipment": "$0",
                "diagnostic": "$0",
                "emergency_room": "$0",
                "urgent_care": "$0",
                "ambulance": "$0",
                "rx_deductible": null,
                "generic": "$0",
                "formulary_brand": "$0",
                "non_formulary_brand": "$0",
                "mail_order": "2.5x",
                "adult_vision_exam": null,
                "adult_preventive_dental": null,
                "adult_major_dental": null,
                "adult_eyewear": null,
                "adult_emergency_dental": null,
                "eyewear": null,
                "pediatric_vision_exam": null,
                "pediatric_preventive_dental": null,
                "pediatric_orthodontics": null,
                "pediatric_major_dental": null,
                "pediatric_eyewear": null,
                "pediatric_emergency_dental": null,
                "pcp_telemedicine": null,
                "nutritionist_telemedicine": null,
                "deductible_single_number": 8150,
                "deductible_family_number": 16300,
                "moop_single_number": 8150,
                "moop_family_number": 16300,
                "benefit_rows_with_header": {
                    "Main Benefits": {
                        "Deductible - Single": "medical_deductible_single",
                        "Deductible - Family": "medical_deductible_family",
                        "Out of Pocket Max - Single": "maximum_out_of_pocket_limit_single",
                        "Out of Pocket Max - Family": "maximum_out_of_pocket_limit_family"
                    },
                    "Outpatient & Inpatient Services": {
                        "Primary Care Visit": "pcp",
                        "Specialist Visit": "specialist",
                        "Preventive Care": "preventive_care",
                        "Inpatient Facility": "inpatient_facility",
                        "Outpatient Facility": "outpatient_facility",
                        "Outpatient Surgery": "outpatient_physician_surgeon"
                    },
                    "Medical Equipment & Tests": {
                        "Imaging": "imaging",
                        "Durable Medical Equipment": "durable_medical_equipment",
                        "Diagnostic": "diagnostic"
                    },
                    "Emergency Services": {
                        "Emergency Room Visit": "emergency_room",
                        "Urgent Care": "urgent_care",
                        "Ambulance": "ambulance"
                    },
                    "Prescription Drug Coverage": {
                        "RX Code": "rx_code",
                        "Prescription Drug Deductible": "rx_deductible",
                        "Generic Brand Prescriptions": "generic",
                        "Formulary Brand Prescriptions": "formulary_brand",
                        "Non-Formulary Brand Prescriptions": "non_formulary_brand",
                        "Mail Order": "mail_order"
                    },
                    "Add-on Dental and Vision": {
                        "Adult Vision Exam": "adult_vision_exam",
                        "Adult Preventive Dental": "adult_preventive_dental",
                        "Adult Major Dental": "adult_major_dental",
                        "Adult Eyewear": "adult_eyewear",
                        "Adult Emergency Dental": "adult_emergency_dental",
                        "Eyewear": "eyewear",
                        "Pediatric Vision Exam": "pediatric_vision_exam",
                        "Pediatric Preventive Dental": "pediatric_preventive_dental",
                        "Pediatric Orthodontics": "pediatric_orthodontics",
                        "Pediatric Major Dental": "pediatric_major_dental",
                        "Pediatric Eyewear": "pediatric_eyewear",
                        "Pediatric Emergency Dental": "pediatric_emergency_dental",
                        "PCP Telemedicine": "pcp_telemedicine",
                        "Nutritionist Telemedicine": "nutritionist_telemedicine"
                    }
                },
                "view_detail_benefits": [
                    "pcp",
                    "imaging",
                    "formulary_brand",
                    "specialist",
                    "generic",
                    "non_formulary_brand"
                ],
                "out_of_network_benfit_row_header": {
                    "Main Benefits": {
                        "Deductible - Single": "medical_deductible_single_out_network",
                        "Deductible - Family": "medical_deductible_family_out_network",
                        "Out of Pocket Max - Single": "maximum_out_of_pocket_limit_single_out_network",
                        "Out of Pocket Max - Family": "maximum_out_of_pocket_limit_family_out_network"
                    },
                    "Outpatient & Inpatient Services": {
                        "Primary Care Visit": "pcp_out_network",
                        "Specialist Visit": "specialist_out_network",
                        "Preventive Care": "preventive_care_out_network",
                        "Inpatient Facility": "inpatient_facility_out_network",
                        "Outpatient Facility": "outpatient_facility_out_network",
                        "Outpatient Surgery": "outpatient_physician_surgeon_out_network"
                    },
                    "Medical Equipment & Tests": {
                        "Imaging": "imaging_out_network",
                        "Durable Medical Equipment": "durable_medical_equipment_out_network",
                        "Diagnostic": "diagnostic_out_network"
                    },
                    "Emergency Services": {
                        "Emergency Room Visit": "emergency_room_out_network",
                        "Urgent Care": "urgent_care_out_network",
                        "Ambulance": "ambulance_out_network"
                    },
                    "Prescription Drug Coverage": {
                        "RX Code": "rx_code",
                        "Prescription Drug Deductible": "rx_deductible_out_network",
                        "Generic Brand Prescriptions": "generic_out_network",
                        "Formulary Brand Prescriptions": "formulary_brand_out_network",
                        "Non-Formulary Brand Prescriptions": "non_formulary_brand_out_network",
                        "Mail Order": "mail_order_out_network"
                    },
                    "Add-on Dental and Vision": {
                        "Adult Vision Exam": "adult_vision_exam_out_network",
                        "Adult Preventive Dental": "adult_preventive_dental_out_network",
                        "Adult Major Dental": "adult_major_dental_out_network",
                        "Adult Eyewear": "adult_eyewear_out_network",
                        "Adult Emergency Dental": "adult_emergency_dental_out_network",
                        "Eyewear": "",
                        "Pediatric Vision Exam": "pediatric_vision_exam_out_network",
                        "Pediatric Preventive Dental": "pediatric_preventive_dental_out_network",
                        "Pediatric Orthodontics": "pediatric_orthodontics_out_network",
                        "Pediatric Major Dental": "pediatric_major_dental_out_network",
                        "Pediatric Eyewear": "pediatric_eyewear_out_network",
                        "Pediatric Emergency Dental": "pediatric_emergency_dental_out_network",
                        "PCP Telemedicine": "pcp_telemedicine_out_network",
                        "Nutritionist Telemedicine": "nutritionist_telemedicine_out_network"
                    }
                },
                "maximum_out_of_pocket_limit_single_out_network": "Not Covered",
                "maximum_out_of_pocket_limit_family_out_network": "Not Covered",
                "medical_deductible_single_out_network": "Not Covered",
                "medical_deductible_family_out_network": "Not Covered",
                "pcp_out_network": "Not Covered",
                "specialist_out_network": "Not Covered",
                "preventive_care_out_network": "Not Covered",
                "generic_out_network": "Not Covered",
                "formulary_brand_out_network": "Not Covered",
                "non_formulary_brand_out_network": "Not Covered",
                "non_preferred_generic_out_network": null,
                "non_preferred_brand_out_network": null,
                "rx_deductible_out_network": null,
                "rx_initial_coverage_limit_out_network": null,
                "adult_emergency_dental_out_network": null,
                "adult_eyewear_out_network": null,
                "adult_major_dental_out_network": null,
                "adult_preventive_dental_out_network": null,
                "adult_vision_exam_out_network": null,
                "ambulance_out_network": "Not Covered",
                "ambulatory_surgery_center_out_network": null,
                "chiropractor_out_network": null,
                "clinical_diagnostic_lab_out_network": null,
                "clinical_diagnostic_mri_out_network": "Not Covered",
                "clinical_diagnostic_radiation_out_network": null,
                "clinical_diagnostic_xray_out_network": "Not Covered",
                "diabetic_supplies_out_network": null,
                "diagnostic_out_network": "Not Covered",
                "durable_medical_equipment_out_network": "Not Covered",
                "emergency_room_out_network": "Not Covered",
                "imaging_out_network": "Not Covered",
                "inpatient_acute_out_network": null,
                "inpatient_facility_out_network": "Not Covered",
                "inpatient_mental_health_out_network": null,
                "inpatient_physician_surgeon_out_network": "Not Covered",
                "mail_order_out_network": null,
                "nutritionist_telemedicine_out_network": null,
                "outpatient_facility_out_network": "Not Covered",
                "outpatient_mental_behavior_health_out_network": null,
                "outpatient_physician_surgeon_out_network": "Not Covered",
                "pcp_telemedicine_out_network": null,
                "pediatric_emergency_dental_out_network": null,
                "pediatric_eyewear_out_network": null,
                "pediatric_major_dental_out_network": null,
                "pediatric_orthodontics_out_network": null,
                "pediatric_preventive_dental_out_network": null,
                "pediatric_vision_exam_out_network": null,
                "physical_occupational_speech_out_network": null,
                "preferred_brand_out_network": null,
                "preferred_generic_out_network": null,
                "preventive_dental_out_network": null,
                "prosthetics_out_network": null,
                "routine_eye_exam_out_network": null,
                "skilled_nursing_facility_out_network": "Not Covered",
                "specialty_out_network": "Not Covered",
                "urgent_care_out_network": "Not Covered",
                "pcp_percentage_number_after_deductible": null,
                "pcp_amount_number_after_deductible": null,
                "pcp_percentage_number_before_deductible": null,
                "pcp_amount_number_before_deductible": 0
            },
            "carrier_plan_identifier": null,
            "model_name": "medical_plans"
        },
        {
            "promotional_label": null,
            "issuer_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/173/main/oscar_logo_blue_2020-wg39.png?1573759981",
            "id": 78720,
            .....,
            "carrier_plan_identifier": null,
            "model_name": "medical_plans"
        }
    ]
}
```

Use this endpoint to retrieve details of selected inquiries group plans.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET            /api/proposals/:company_slug/group_plans?selected_inquiries=:inquiry_slug,:inquiry_slug`

### Parameters

No parameters required.

## Group Plans Pricing

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans_pricing?selected_inquiries=JXID6718,JQLI9871' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%225dy4Dom_xiZZO2_bae6gWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923733%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: 5dy4Dom_xiZZO2_bae6gWw' \
--header 'client: pkevB8VD4yONukgbtPUFFw' \
--header 'expiry: 1583923733' \
--header 'uid: apidoc+broker@wellthie.com' \
--header 'Authorization: Bearer XsT2kpRKu9D3EanAwyNCFw' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans_pricing?selected_inquiries=JXID6718,JQLI9871"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%225dy4Dom_xiZZO2_bae6gWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923733%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "5dy4Dom_xiZZO2_bae6gWw")
  req.Header.Add("client", "pkevB8VD4yONukgbtPUFFw")
  req.Header.Add("expiry", "1583923733")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")
  req.Header.Add("Authorization", "Bearer XsT2kpRKu9D3EanAwyNCFw")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans_pricing?selected_inquiries=JXID6718,JQLI9871",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%225dy4Dom_xiZZO2_bae6gWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923733%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "5dy4Dom_xiZZO2_bae6gWw",
    "client": "pkevB8VD4yONukgbtPUFFw",
    "expiry": "1583923733",
    "uid": "apidoc+broker@wellthie.com",
    "Authorization": "Bearer XsT2kpRKu9D3EanAwyNCFw"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans_pricing?selected_inquiries=JXID6718,JQLI9871"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%225dy4Dom_xiZZO2_bae6gWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923733%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"5dy4Dom_xiZZO2_bae6gWw",
  @"client": @"pkevB8VD4yONukgbtPUFFw",
  @"expiry": @"1583923733",
  @"uid": @"apidoc+broker@wellthie.com",
  @"Authorization": @"Bearer XsT2kpRKu9D3EanAwyNCFw"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%225dy4Dom_xiZZO2_bae6gWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583923733%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "5dy4Dom_xiZZO2_bae6gWw")
$headers.Add("client", "pkevB8VD4yONukgbtPUFFw")
$headers.Add("expiry", "1583923733")
$headers.Add("uid", "apidoc+broker@wellthie.com")
$headers.Add("Authorization", "Bearer XsT2kpRKu9D3EanAwyNCFw")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/group_plans_pricing?selected_inquiries=JXID6718,JQLI9871' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "JXID6718": [
        {
            "id": 78717,
            "carrier_plan_identifier": null,
            "premiums": {
                "member_prices": {
                    "households": {
                        "423007": 535.88,
                        "423008": 1071.77,
                        "423009": 1527.27,
                        "423010": 911.0
                    },
                    "members": {
                        "523247": 535.88,
                        "523248": 1071.77,
                        "523249": 0.0,
                        "523250": 1527.27,
                        "523251": 0.0,
                        "523252": 0.0,
                        "523253": 911.0,
                        "523254": 0.0
                    }
                },
                "total_monthly_premium": 4045.92,
                "total_annual_premium": 48551.04
            }
        }
    ],
    "JQLI9871": [
        {
            "id": 78717,
            "carrier_plan_identifier": null,
            "premiums": {
                "member_prices": {
                    "households": {
                        "422991": 535.88,
                        "422992": 1071.77,
                        "422993": 1527.27,
                        "422994": 911.0
                    },
                    "members": {
                        "523219": 535.88,
                        "523220": 1071.77,
                        "523221": 0.0,
                        "523222": 1527.27,
                        "523223": 0.0,
                        "523224": 0.0,
                        "523225": 911.0,
                        "523226": 0.0
                    }
                },
                "total_monthly_premium": 4045.92,
                "total_annual_premium": 48551.04
            }
        },
        {
            "id": 78720,
            "carrier_plan_identifier": null,
            "premiums": {
                "member_prices": {
                    "households": {
                        "422991": 535.88,
                        "422992": 1071.77,
                        "422993": 1527.27,
                        "422994": 911.0
                    },
                    "members": {
                        "523219": 535.88,
                        "523220": 1071.77,
                        "523221": 0.0,
                        "523222": 1527.27,
                        "523223": 0.0,
                        "523224": 0.0,
                        "523225": 911.0,
                        "523226": 0.0
                    }
                },
                "total_monthly_premium": 4045.92,
                "total_annual_premium": 48551.04
            }
        }
    ]
}
```

Use this endpoint to retrieve details of selected inquiries group plans pricings.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET            /api/proposals/:company_slug/group_plans_pricing?selected_inquiries=:inquiry_slug,:inquiry_slug`

### Parameters

No parameters required.

## Plan Selections

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/plan_selections?selected_inquiries=JXID6718,JQLI9871' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22V7kA-QUpMdlGf2uYPiZLWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22DpkpkKwhcLgIuwbo4fiWnQ%22%2C%22expiry%22%3A%221583924575%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: V7kA-QUpMdlGf2uYPiZLWw' \
--header 'client: DpkpkKwhcLgIuwbo4fiWnQ' \
--header 'expiry: 1583924575' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/plan_selections?selected_inquiries=JXID6718,JQLI9871"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22V7kA-QUpMdlGf2uYPiZLWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22DpkpkKwhcLgIuwbo4fiWnQ%22%2C%22expiry%22%3A%221583924575%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "V7kA-QUpMdlGf2uYPiZLWw")
  req.Header.Add("client", "DpkpkKwhcLgIuwbo4fiWnQ")
  req.Header.Add("expiry", "1583924575")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/plan_selections?selected_inquiries=JXID6718,JQLI9871",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22V7kA-QUpMdlGf2uYPiZLWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22DpkpkKwhcLgIuwbo4fiWnQ%22%2C%22expiry%22%3A%221583924575%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "V7kA-QUpMdlGf2uYPiZLWw",
    "client": "DpkpkKwhcLgIuwbo4fiWnQ",
    "expiry": "1583924575",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/plan_selections?selected_inquiries=JXID6718,JQLI9871"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22V7kA-QUpMdlGf2uYPiZLWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22DpkpkKwhcLgIuwbo4fiWnQ%22%2C%22expiry%22%3A%221583924575%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"V7kA-QUpMdlGf2uYPiZLWw",
  @"client": @"DpkpkKwhcLgIuwbo4fiWnQ",
  @"expiry": @"1583924575",
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22V7kA-QUpMdlGf2uYPiZLWw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22DpkpkKwhcLgIuwbo4fiWnQ%22%2C%22expiry%22%3A%221583924575%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "V7kA-QUpMdlGf2uYPiZLWw")
$headers.Add("client", "DpkpkKwhcLgIuwbo4fiWnQ")
$headers.Add("expiry", "1583924575")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/shy8pmfek8ZpGKJYneD2g5TJ/plan_selections?selected_inquiries=JXID6718,JQLI9871' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "JXID6718": [
        {
            "id": 136304,
            "individual_plan_id": null,
            "medical_plan_id": 78717,
            "ancillary_plan_id": null,
            "ancillary_plan_type": null,
            "selected_for_quote": true,
            "selected_for_enrollment": false,
            "order": 0
        },
        {
            "id": 136306,
            "individual_plan_id": null,
            "medical_plan_id": 78717,
            "ancillary_plan_id": null,
            "ancillary_plan_type": null,
            "selected_for_quote": true,
            "selected_for_enrollment": false,
            "order": 0
        },
        {
            "id": 136307,
            "individual_plan_id": null,
            "medical_plan_id": 78717,
            "ancillary_plan_id": null,
            "ancillary_plan_type": null,
            "selected_for_quote": true,
            "selected_for_enrollment": false,
            "order": 1
        }
    ],
    "JQLI9871": [
        {
            "id": 136309,
            "individual_plan_id": null,
            "medical_plan_id": 78717,
            "ancillary_plan_id": null,
            "ancillary_plan_type": null,
            "selected_for_quote": true,
            "selected_for_enrollment": false,
            "order": 0
        },
        {
            "id": 136310,
            "individual_plan_id": null,
            "medical_plan_id": 78720,
            "ancillary_plan_id": null,
            "ancillary_plan_type": null,
            "selected_for_quote": true,
            "selected_for_enrollment": false,
            "order": 1
        }
    ]
}
```

Use this endpoint to retrieve details of selected inquiries group plans.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET            /api/proposals/:company_slug/plan_selections?selected_inquiries=:inquiry_slug,:inquiry_slug`

### Parameters

No parameters required.

## Individual Quotes

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/epQ1xdE1NQcQ8TWj3Cq7Ca42/individual_quotes?selected_inquiries=ZVTD8453,ZIWA4138' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22MQ3ov8p1gbY-GCrhIblmRQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22c3nNGXEB2hLVOa2BbXymVA%22%2C%22expiry%22%3A%221583924795%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: MQ3ov8p1gbY-GCrhIblmRQ' \
--header 'client: c3nNGXEB2hLVOa2BbXymVA' \
--header 'expiry: 1583924795' \
--header 'uid: apidoc+broker@wellthie.com' \
--header 'Authorization: Bearer NoGjq4aQfoLLiwoNv1uRVQ' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/epQ1xdE1NQcQ8TWj3Cq7Ca42/individual_quotes?selected_inquiries=ZVTD8453,ZIWA4138"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22MQ3ov8p1gbY-GCrhIblmRQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22c3nNGXEB2hLVOa2BbXymVA%22%2C%22expiry%22%3A%221583924795%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "MQ3ov8p1gbY-GCrhIblmRQ")
  req.Header.Add("client", "c3nNGXEB2hLVOa2BbXymVA")
  req.Header.Add("expiry", "1583924795")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")
  req.Header.Add("Authorization", "Bearer NoGjq4aQfoLLiwoNv1uRVQ")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/epQ1xdE1NQcQ8TWj3Cq7Ca42/individual_quotes?selected_inquiries=ZVTD8453,ZIWA4138",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22MQ3ov8p1gbY-GCrhIblmRQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22c3nNGXEB2hLVOa2BbXymVA%22%2C%22expiry%22%3A%221583924795%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "MQ3ov8p1gbY-GCrhIblmRQ",
    "client": "c3nNGXEB2hLVOa2BbXymVA",
    "expiry": "1583924795",
    "uid": "apidoc+broker@wellthie.com",
    "Authorization": "Bearer NoGjq4aQfoLLiwoNv1uRVQ"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/epQ1xdE1NQcQ8TWj3Cq7Ca42/individual_quotes?selected_inquiries=ZVTD8453,ZIWA4138"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22MQ3ov8p1gbY-GCrhIblmRQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22c3nNGXEB2hLVOa2BbXymVA%22%2C%22expiry%22%3A%221583924795%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"MQ3ov8p1gbY-GCrhIblmRQ",
  @"client": @"c3nNGXEB2hLVOa2BbXymVA",
  @"expiry": @"1583924795",
  @"uid": @"apidoc+broker@wellthie.com",
  @"Authorization": @"Bearer NoGjq4aQfoLLiwoNv1uRVQ"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22MQ3ov8p1gbY-GCrhIblmRQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22c3nNGXEB2hLVOa2BbXymVA%22%2C%22expiry%22%3A%221583924795%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "MQ3ov8p1gbY-GCrhIblmRQ")
$headers.Add("client", "c3nNGXEB2hLVOa2BbXymVA")
$headers.Add("expiry", "1583924795")
$headers.Add("uid", "apidoc+broker@wellthie.com")
$headers.Add("Authorization", "Bearer NoGjq4aQfoLLiwoNv1uRVQ")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/proposals/epQ1xdE1NQcQ8TWj3Cq7Ca42/individual_quotes?selected_inquiries=ZVTD8453,ZIWA4138' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "ZVTD8453": {
        "58130": [
            {
                "household_id": 409759,
                "monthly_price": 420.55,
                "monthly_credits": 0.0,
                "monthly_price_after_credit": 420.55,
                "monthly_price_after_credit_and_salary_adjustment": 420.55,
                "monthly_price_after_credit_and_salary_adjustment_after_tax": 420.55,
                "member_ids_to_plan_names": {
                    "506247": "Metal"
                }
            },
            {
                "household_id": 409760,
                "monthly_price": 420.55,
                "monthly_credits": 0.0,
                "monthly_price_after_credit": 420.55,
                "monthly_price_after_credit_and_salary_adjustment": 420.55,
                "monthly_price_after_credit_and_salary_adjustment_after_tax": 420.55,
                "member_ids_to_plan_names": {
                    "506248": "Metal"
                }
            }
        ],
        "58131": [
            {
                "household_id": 409759,
                "monthly_price": 713.76,
                "monthly_credits": 0.0,
                "monthly_price_after_credit": 713.76,
                "monthly_price_after_credit_and_salary_adjustment": 713.76,
                "monthly_price_after_credit_and_salary_adjustment_after_tax": 713.76,
                "member_ids_to_plan_names": {
                    "506247": "Metal"
                }
            },
            {
                "household_id": 409760,
                "monthly_price": 713.76,
                "monthly_credits": 0.0,
                "monthly_price_after_credit": 713.76,
                "monthly_price_after_credit_and_salary_adjustment": 713.76,
                "monthly_price_after_credit_and_salary_adjustment_after_tax": 713.76,
                "member_ids_to_plan_names": {
                    "506248": "Metal"
                }
            }
        ],
        "58132": [
            {
                "household_id": 409759,
                "monthly_price": 864.8,
                "monthly_credits": 0.0,
                "monthly_price_after_credit": 864.8,
                "monthly_price_after_credit_and_salary_adjustment": 864.8,
                "monthly_price_after_credit_and_salary_adjustment_after_tax": 864.8,
                "member_ids_to_plan_names": {
                    "506247": "Metal"
                }
            },
            {
                "household_id": 409760,
                "monthly_price": 864.8,
                "monthly_credits": 0.0,
                "monthly_price_after_credit": 864.8,
                "monthly_price_after_credit_and_salary_adjustment": 864.8,
                "monthly_price_after_credit_and_salary_adjustment_after_tax": 864.8,
                "member_ids_to_plan_names": {
                    "506248": "Metal"
                }
            }
        ],
        "58133": [
            {
                "household_id": 409759,
                "monthly_price": 597.85,
                "monthly_credits": 0.0,
                "monthly_price_after_credit": 597.85,
                "monthly_price_after_credit_and_salary_adjustment": 597.85,
                "monthly_price_after_credit_and_salary_adjustment_after_tax": 597.85,
                "member_ids_to_plan_names": {
                    "506247": "Metal"
                }
            },
            {
                "household_id": 409760,
                "monthly_price": 597.85,
                "monthly_credits": 0.0,
                "monthly_price_after_credit": 597.85,
                "monthly_price_after_credit_and_salary_adjustment": 597.85,
                "monthly_price_after_credit_and_salary_adjustment_after_tax": 597.85,
                "member_ids_to_plan_names": {
                    "506248": "Metal"
                }
            }
        ]
    }
}
```

Use this endpoint to retrieve details of selected inquiries group plans.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET            /api/proposals/:company_slug/individual_quotes?selected_inquiries=:inquiry_slug,:inquiry_slug`

### Parameters

No parameters required.
