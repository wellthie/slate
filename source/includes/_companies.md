# Companies

Company is the small group for which the Inquiry / Quote is being created for.

<aside class="notice">A Small Group Business / Company can have up to 50 employees. In California, Colorado, New York and Vermont the total Full Time Employees count can go up to 100.</aside>

<aside class="notice">For companies with only one employee, Wellthie has another Individual Platform</aside>

## Get Company Details

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp"
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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp"]
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

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/yNponia3pn8tpqygHSo8FhSp' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "slug": "6uqej6JT9uumY4g41CdLX7Du",
    "name": "Company Name",
    "zip_code_input": "10001",
    "contact_name": "Contact Name",
    "contact_email": "person@company.com",
    "using_broker": true,
    "broker_code": "ValidBrokerCode",
    "errors_json": [],
    "county_id": 36061,
    "save_failed_due_to_errors": null,
    "small_group_max_size": 100,
    "sic_code": 9999,
    "uses_tiers": true,
    "allow_group_and_group_to_individual": true,
    "attributes_with_error_messages_in_order": [
        "name",
        "zip_code_input",
        "contact_name",
        "contact_email",
        "county_id"
    ],
    "formatted_sic_code": "9999",
    "show_tobacco_for_census": false,
    "state": {
        "abbr": "NY",
        "plan_notice_content_area_header": null,
        "plan_notice_content_area_body": null,
        "display_employee_zip": false
    },
    "current_plan": null,
    "current_plans": []
}
```

> In case of Unauthorized

```json
{
    "message": "Unauthorized"
}
```

Use this endpoint to retrieve information about a specific company.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`GET /api/companies/:slug`

### Parameters

No parameters required.

## Create Company

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE' \
--data-raw '{
  "company": {
    "name": "APIDocTest4",
    "zip_code_input": "10001",
    "contact_name": "Test",
    "contact_email": "test@test.com",
    "using_broker": false,
    "broker_code": null,
    "county_id": 36061,
    "sic_code": "9999"
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/"
  method := "POST"

  payload := strings.NewReader("{\n  \"company\": {\n    \"name\": \"APIDocTest4\",\n    \"zip_code_input\": \"10001\",\n    \"contact_name\": \"Test\",\n    \"contact_email\": \"test@test.com\",\n    \"using_broker\": false,\n    \"broker_code\": null,\n    \"county_id\": 36061,\n    \"sic_code\": \"9999\"\n  }\n}")

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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
  },
  "data": JSON.stringify({"company":{"name":"APIDocTest4","zip_code_input":"10001","contact_name":"Test","contact_email":"test@test.com","using_broker":false,"broker_code":null,"county_id":36061,"sic_code":"9999"}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"company\": {\n    \"name\": \"APIDocTest4\",\n    \"zip_code_input\": \"10001\",\n    \"contact_name\": \"Test\",\n    \"contact_email\": \"test@test.com\",\n    \"using_broker\": false,\n    \"broker_code\": null,\n    \"county_id\": 36061,\n    \"sic_code\": \"9999\"\n  }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

$body = "{`n  `"company`": {`n    `"name`": `"APIDocTest4`",`n    `"zip_code_input`": `"10001`",`n    `"contact_name`": `"Test`",`n    `"contact_email`": `"test@test.com`",`n    `"using_broker`": false,`n    `"broker_code`": null,`n    `"county_id`": 36061,`n    `"sic_code`": `"9999`"`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Company Object

```json
{
  "company": {
    "name": "Company Name",
    "zip_code_input": "10001",
    "contact_name": "Test",
    "contact_email": "test@test.com",
    "using_broker": false,
    "broker_code": null,
    "county_id": 36061,
    "sic_code": "9999"
  }
}
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

> If there is an error processing a message the server will reply with an error. For example:

```json

{
    "zip_code_input": [ "can't be blank", "is invalid" ],
    "name": [
        "is too short (minimum is 1 character)",
        "is too long (maximum is 255 characters)"
    ]
}

```

Use this endpoint to create a new company.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`POST /api/companies`

### Parameters

Parameter                                                                                        | Default      | Description
------------------------------------------------------------------------------------------------ | ------------ | -----------------------
<strong>company</strong><strong>required</strong>                                                | N/A          | Company object 

### Detailed Company Object Parameters

Parameter                                                                                        | Default      | Description
------------------------------------------------------------------------------------------------ | ------------ | -----------------------
<strong>company[name]</strong><strong>required</strong>                                          | N/A          | name
<strong>company[zip_code_input]</strong><strong>required</strong>                                | N/A          | zipcode
<strong>company[contact_name]</strong><strong>required</strong>                                  | N/A          | contact name
<strong>company[contact_email]</strong><strong>required</strong>                                 | N/A          | contact email
<strong>company[effective_date]</strong><strong>required</strong>                                | N/A          | Effective date
<strong>company[county_id]</strong><strong>required</strong>                                     | N/A          | county id
<strong>company[sic_code]</strong><strong>required</strong>                                      | N/A          | sic code
<strong>company[broker_code]</strong><strong>required if using_broker,  false otherwise</strong> | N/A          | Broker code
company[using_broker]                                                                            | N/A          | Using broker flag

## Update Company

```shell
curl --location --request PUT 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/P7Kvahp8UmP7TLYXJDnsyZ3y' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE' \
--data-raw '{
  "company": {
    "name": "APIDoc Company",
    "zip_code_input": "10001",
    "contact_name": "Test",
    "contact_email": "test@test.com",
    "effective_date": "04/01/2020",
    "using_broker": false,
    "broker_code": null,
    "county_id": 36061,
    "sic_code": "9999"
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/P7Kvahp8UmP7TLYXJDnsyZ3y"
  method := "PUT"

  payload := strings.NewReader("{\n  \"company\": {\n    \"name\": \"APIDoc Company\",\n    \"zip_code_input\": \"10001\",\n    \"contact_name\": \"Test\",\n    \"contact_email\": \"test@test.com\",\n    \"using_broker\": false,\n    \"broker_code\": null,\n    \"county_id\": 36061,\n    \"sic_code\": \"9999\"\n  }\n}")

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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/P7Kvahp8UmP7TLYXJDnsyZ3y",
  "method": "PUT",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
  },
  "data": JSON.stringify({"company":{"name":"APIDoc Company","zip_code_input":"10001","contact_name":"Test","contact_email":"test@test.com","using_broker":false,"broker_code":null,"county_id":36061,"sic_code":"9999"}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/P7Kvahp8UmP7TLYXJDnsyZ3y"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"company\": {\n    \"name\": \"APIDoc Company\",\n    \"zip_code_input\": \"10001\",\n    \"contact_name\": \"Test\",\n    \"contact_email\": \"test@test.com\",\n    \"using_broker\": false,\n    \"broker_code\": null,\n    \"county_id\": 36061,\n    \"sic_code\": \"9999\"\n  }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

$body = "{`n  `"company`": {`n    `"name`": `"APIDoc Company`",`n    `"zip_code_input`": `"10001`",`n    `"contact_name`": `"Test`",`n    `"contact_email`": `"test@test.com`",`n    `"using_broker`": false,`n    `"broker_code`": null,`n    `"county_id`": 36061,`n    `"sic_code`": `"9999`"`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/P7Kvahp8UmP7TLYXJDnsyZ3y' -Method 'PUT' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Company Object

```json
{
  "company": {
    "name": "Company Name",
    "zip_code_input": "10001",
    "contact_name": "Test",
    "contact_email": "test@test.com",
    "effective_date": "04/01/2020",
    "using_broker": false,
    "broker_code": null,
    "county_id": 36061,
    "sic_code": "9999"
  }
}
```

> Successful response looks like this:

```json
{
    "slug": "wXri....",
    "name": "APIDocTest4Update",
    "zip_code_input": "10001",
    "contact_name": "Test",
    "contact_email": "test@test.com",
    "using_broker": true,
    "broker_code": "123456",
    "errors_json": [],
    "county_id": 36061,
    "save_failed_due_to_errors": null,
    "small_group_max_size": 100,
    "sic_code": 9999,
    "uses_tiers": true,
    "allow_group_and_group_to_individual": true,
    "attributes_with_error_messages_in_order": [
        "name",
        "zip_code_input",
        "contact_name",
        "contact_email",
        "county_id"
    ],
    "formatted_sic_code": "9999",
    "show_tobacco_for_census": false,
    "state": {
        "abbr": "NY",
        "plan_notice_content_area_header": null,
        "plan_notice_content_area_body": null,
        "display_employee_zip": false
    },
    "current_plan": null,
    "current_plans": []
}
```

> If there is an error processing a message the server will reply with an error. For example:

```json

{
    "zip_code_input": [ "can't be blank", "is invalid" ],
    "name": [
        "is too short (minimum is 1 character)",
        "is too long (maximum is 255 characters)"
    ]
}
```

Use this endpoint to update an existing company.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`PUT /api/companies/:slug`

### Parameters

Parameter     | Default      | Description
------------- | ------------ | -----------------------
company       | N/A          | Company object 

### Detailed Company Object Parameters

Parameter                | Default      | Description
------------------------ | ------------ | -----------------------
company[name]            | N/A          | name
company[zip_code_input]  | N/A          | zipcode
company[contact_name]    | N/A          | contact name
company[contact_email]   | N/A          | contact email
company[effective_date]  | N/A          | Effective date
company[county_id]       | N/A          | county id
company[sic_code]        | N/A          | sic code
company[broker_code]     | N/A          | Broker code
company[using_broker]    | N/A          | Using broker flag
