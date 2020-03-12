# Plans

## Get Available Plans

```shell
curl --location --request GET 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs' \
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

  url := "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

$body = ""

$response = Invoke-RestMethod 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
    {
        "id": 11649,
        "type": "MetalPlan",
        "name": "EmblemHealth Bronze D",
        "plan_description": "<p><br></p>",
        "metal_level_name": "Bronze",
        "hios_plan_identifier": "88582NY0350001",
        "on_exchange": false,
        "off_exchange": true,
        "sbc_download_url": "",
        "medical_deductible": null,
        "maximum_out_of_pocket_limit": null,
        "medical_deductible_single": "$4,425",
        "maximum_out_of_pocket_limit_single": "$8,150",
        "medical_deductible_family": "$8,850",
        "maximum_out_of_pocket_limit_family": "$16,300",
        "group_or_individual_plan_type": "Individual",
        "pcp": "3 free visits, then 50% after deductible",
        "specialist": "50% after deductible",
        "formulary_url": "https://www.emblemhealth.com/resources/pharmacy",
        "network_url": "https://portals.emblemhealth.com/ProviderSearchEHHIP/Default.aspx?Plan=SCGVD&Network=SELC&ShowPlan=no",
        "treatment_cost_calculator_url": "",
        "part_b_deductible": null,
        "flex_benefit": null,
        "part_d_prescription_coverage": null,
        "highlight_1": {
            "icon": "icon--metal",
            "value": "Bronze"
        },
        "highlight_2": {
            "icon": "icon--add-on",
            "value": "3 free PCP visits, then 50% after deductible"
        },
        "highlight_3": {
            "icon": "icon--add-on",
            "value": "Pediatric Dental and Vision"
        },
        "promotional_label": "",
        "benefits": [
            {
                "row_key": "main_benefits_heading",
                "display_key": "Plan Attribute Display Name: Medical: main_benefits_heading",
                "tooltip_key": "Plan Attribute Tooltip: main_benefits_heading",
                "content": "Plan Attribute Display Name: Medical: main_benefits_heading",
                "heading_row": true,
                "details_view": false
            },
            {
                "row_key": "preventive_care",
                "display_key": "Plan Attribute Display Name: Medical: preventive_care",
                "tooltip_key": "Plan Attribute Tooltip: preventive_care",
                "content": "Covered in full",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "medical_deductible_single",
                "display_key": "Plan Attribute Display Name: Medical: medical_deductible_single",
                "tooltip_key": "Plan Attribute Tooltip: medical_deductible_single",
                "content": "$4,425",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "medical_deductible_family",
                "display_key": "Plan Attribute Display Name: Medical: medical_deductible_family",
                "tooltip_key": "Plan Attribute Tooltip: medical_deductible_family",
                "content": "$8,850",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "maximum_out_of_pocket_limit_single",
                "display_key": "Plan Attribute Display Name: Medical: maximum_out_of_pocket_limit_single",
                "tooltip_key": "Plan Attribute Tooltip: maximum_out_of_pocket_limit_single",
                "content": "$8,150",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "maximum_out_of_pocket_limit_family",
                "display_key": "Plan Attribute Display Name: Medical: maximum_out_of_pocket_limit_family",
                "tooltip_key": "Plan Attribute Tooltip: maximum_out_of_pocket_limit_family",
                "content": "$16,300",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "what_you_will_pay",
                "display_key": "Plan Attribute Display Name: Medical: what_you_will_pay",
                "tooltip_key": "Plan Attribute Tooltip: what_you_will_pay",
                "content": "Plan Attribute Display Name: Medical: what_you_will_pay",
                "heading_row": true,
                "details_view": false
            },
            {
                "row_key": "pcp",
                "display_key": "Plan Attribute Display Name: Medical: pcp",
                "tooltip_key": "Plan Attribute Tooltip: pcp",
                "content": "3 free visits, then 50% after deductible",
                "heading_row": false,
                "details_view": true
            },
            {
                "row_key": "specialist",
                "display_key": "Plan Attribute Display Name: Medical: specialist",
                "tooltip_key": "Plan Attribute Tooltip: specialist",
                "content": "50% after deductible",
                "heading_row": false,
                "details_view": true
            },
            {
                "row_key": "urgent_care",
                "display_key": "Plan Attribute Display Name: Medical: urgent_care",
                "tooltip_key": "Plan Attribute Tooltip: urgent_care",
                "content": "50% after deductible",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "emergency_room",
                "display_key": "Plan Attribute Display Name: Medical: emergency_room",
                "tooltip_key": "Plan Attribute Tooltip: emergency_room",
                "content": "50% after deductible",
                "heading_row": false,
                "details_view": true
            },
            {
                "row_key": "inpatient_facility",
                "display_key": "Plan Attribute Display Name: Medical: inpatient_facility",
                "tooltip_key": "Plan Attribute Tooltip: inpatient_facility",
                "content": "50% after deductible",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "ambulance",
                "display_key": "Plan Attribute Display Name: Medical: ambulance",
                "tooltip_key": "Plan Attribute Tooltip: ambulance",
                "content": "50% after deductible",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "durable_medical_equipment",
                "display_key": "Plan Attribute Display Name: Medical: durable_medical_equipment",
                "tooltip_key": "Plan Attribute Tooltip: durable_medical_equipment",
                "content": "50% after deductible",
                "heading_row": false,
                "details_view": false
            },
            {
                "row_key": "prescription_drugs",
                "display_key": "Plan Attribute Display Name: Medical: prescription_drugs",
                "tooltip_key": "Plan Attribute Tooltip: prescription_drugs",
                "content": "Plan Attribute Display Name: Medical: prescription_drugs",
                "heading_row": true,
                "details_view": false
            },
            {
                "row_key": "generic",
                "display_key": "Plan Attribute Display Name: Medical: generic",
                "tooltip_key": "Plan Attribute Tooltip: generic",
                "content": "$10 after deductible",
                "heading_row": false,
                "details_view": true
            },
            {
                "row_key": "formulary_brand",
                "display_key": "Plan Attribute Display Name: Medical: formulary_brand",
                "tooltip_key": "Plan Attribute Tooltip: formulary_brand",
                "content": "$35 after deductible",
                "heading_row": false,
                "details_view": true
            },
            {
                "row_key": "non_formulary_brand",
                "display_key": "Plan Attribute Display Name: Medical: non_formulary_brand",
                "tooltip_key": "Plan Attribute Tooltip: non_formulary_brand",
                "content": "$70 after deductible",
                "heading_row": false,
                "details_view": true
            },
            {
                "row_key": "adult_dental_and_vision_benefits_heading",
                "display_key": "Plan Attribute Display Name: Medical: adult_dental_and_vision_benefits_heading",
                "tooltip_key": "Plan Attribute Tooltip: adult_dental_and_vision_benefits_heading",
                "content": "Plan Attribute Display Name: Medical: adult_dental_and_vision_benefits_heading",
                "heading_row": true,
                "details_view": false
            }
        ],
        "tags": [
            "bronze",
            "hmo",
            "off_exchange"
        ],
        "price_period": "Monthly",
        "price_note": null,
        "issuer_id": 375,
        "issuer_logo": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/375/main/emblem%20health%20logo-kg81.png?1567585867",
        "issuer_name": "EmblemHealth",
        "issuer_individual_broker_portal_url": "",
        "is_age_29_plan": false,
        "is_csr": false,
        "plan_detail_header": "<p><br></p>",
        "plan_detail_items": [],
        "plan_detail_footer": "<p><br></p>",
        "original_medicare": null,
        "default_bhp": false,
        "sort_order": 6,
        "deductible_single_number": 4425,
        "deductible_family_number": 8850,
        "issuer": {
            "id": 375,
            "name": "EmblemHealth"
        },
        "moop_single_number": 8150,
        "moop_family_number": 16300,
        "plan_procedures": []
    }
]
```

Use this endpoint to get all the available plans for the quote. A list of plans should be returned. In the example there's only one plan, since the json is pretty long, but usually there are several plans.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>


### HTTP Request

`GET /api/quotes/:quote_id/plans`

### Parameters

No parameters required.

## Get Pricing for Available Plans

```shell
curl --location --request GET 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plan_pricing' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs' \
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

  url := "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plan_pricing"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plan_pricing",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plan_pricing"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

$body = ""

$response = Invoke-RestMethod 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plan_pricing' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
    {
        "medical_plan_id": 11649,
        "price": 1945.3,
        "monthly_credit": 0.0,
        "child_only": false
    }
]
```

Use this endpoint to list the prices for the plans. A list of prices should be returned. In the example there's only one price, since the json is pretty long, but usually there are several prices.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>

### HTTP Request

`GET /api/quotes/:quote_id/plan_pricing`

### Parameters

No parameters required.

## Get Selected Plans of a Quote

```shell
curl --location --request GET 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-284971/plans/retrieve_selections' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs' \
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

  url := "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-284971/plans/retrieve_selections"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-284971/plans/retrieve_selections",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-284971/plans/retrieve_selections"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

$body = ""

$response = Invoke-RestMethod 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-284971/plans/retrieve_selections' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
    {
        "family_member_id": 68649,
        "medical_plan_ids": [
            11676
        ]
    },
    {
        "family_member_id": 68647,
        "medical_plan_ids": [
            11676
        ]
    },
    {
        "family_member_id": 68648,
        "medical_plan_ids": [
            11693
        ]
    }
]
```

Use this endpoint to retrieve quote's plan selections. It could be up to 4 elements / 4 plan selections.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>

### HTTP Request

`GET /api/quotes/:quote_id/plans/retrieve_selections`

### Parameters

No parameters required.

## Select a Plan for Quote

```shell
curl --location --request POST 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs' \
--data-raw '{
    "family_members_plans": [
        {
            "family_member_id": 68649,
            "medical_plan_ids": [
                11676
            ]
        },
        {
            "family_member_id": 68647,
            "medical_plan_ids": [
                11676
            ]
        },
        {
            "family_member_id": 68648,
            "medical_plan_ids": [
                11693
            ]
        }
    ]
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

  url := "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select"
  method := "POST"

  payload := strings.NewReader("{\n    \"family_members_plans\": [\n        {\n            \"family_member_id\": 68649,\n            \"medical_plan_ids\": [\n                11676\n            ]\n        },\n        {\n            \"family_member_id\": 68647,\n            \"medical_plan_ids\": [\n                11676\n            ]\n        },\n        {\n            \"family_member_id\": 68648,\n            \"medical_plan_ids\": [\n                11693\n            ]\n        }\n    ]\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
  },
  "data": JSON.stringify({"family_members_plans":[{"family_member_id":68649,"medical_plan_ids":[11676]},{"family_member_id":68647,"medical_plan_ids":[11676]},{"family_member_id":68648,"medical_plan_ids":[11693]}]}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n    \"family_members_plans\": [\n        {\n            \"family_member_id\": 68649,\n            \"medical_plan_ids\": [\n                11676\n            ]\n        },\n        {\n            \"family_member_id\": 68647,\n            \"medical_plan_ids\": [\n                11676\n            ]\n        },\n        {\n            \"family_member_id\": 68648,\n            \"medical_plan_ids\": [\n                11693\n            ]\n        }\n    ]\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

$body = "{`n    `"family_members_plans`": [`n        {`n            `"family_member_id`": 68649,`n            `"medical_plan_ids`": [`n                11676`n            ]`n        },`n        {`n            `"family_member_id`": 68647,`n            `"medical_plan_ids`": [`n                11676`n            ]`n        },`n        {`n            `"family_member_id`": 68648,`n            `"medical_plan_ids`": [`n                11693`n            ]`n        }`n    ]`n}"

$response = Invoke-RestMethod 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this: HTTP response code would be 200 for success response.

```json
{}
```

Use this endpoint to select a plan for quote.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>

### HTTP Request

`POST           /api/quotes/:quote_id/plans/select`

### Parameters

No parameters required.

## UnSelect Plan from Quote

```shell
curl --location --request POST 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs' \
--data-raw '{ "family_members_plans": [ { "family_member_id": 68649, "medical_plan_ids": [ ] }, { "family_member_id": 68647, "medical_plan_ids": [ ] }, { "family_member_id": 68648, "medical_plan_ids": [ 11693 ] } ] }'
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

  url := "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select"
  method := "POST"

  payload := strings.NewReader("{ \"family_members_plans\": [ { \"family_member_id\": 68649, \"medical_plan_ids\": [ ] }, { \"family_member_id\": 68647, \"medical_plan_ids\": [ ] }, { \"family_member_id\": 68648, \"medical_plan_ids\": [ 11693 ] } ] }")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
  },
  "data": JSON.stringify({"family_members_plans":[{"family_member_id":68649,"medical_plan_ids":[]},{"family_member_id":68647,"medical_plan_ids":[]},{"family_member_id":68648,"medical_plan_ids":[11693]}]}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{ \"family_members_plans\": [ { \"family_member_id\": 68649, \"medical_plan_ids\": [ ] }, { \"family_member_id\": 68647, \"medical_plan_ids\": [ ] }, { \"family_member_id\": 68648, \"medical_plan_ids\": [ 11693 ] } ] }" dataUsingEncoding:NSUTF8StringEncoding]];
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

$body = "{ `"family_members_plans`": [ { `"family_member_id`": 68649, `"medical_plan_ids`": [ ] }, { `"family_member_id`": 68647, `"medical_plan_ids`": [ ] }, { `"family_member_id`": 68648, `"medical_plan_ids`": [ 11693 ] } ] }"

$response = Invoke-RestMethod 'http://emblemhealth-qa.lvh.me:3030/api/quotes/SW-759864/plans/select' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> This request doesn't contain any response. Http response code would be 200.

```json
{}
```

Use this endpoint to select / unselect a plan for quote.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>

### HTTP Request

`POST           /api/quotes/:quote_id/plans/select`

### Parameters

No parameters required.
