# Companies

## Get Company Details

```shell
curl --location --request GET 'http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/6uqej6JT9uumY4g41CdLX7Du' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: ctgocjRjlvrDCak4ls1Dqg' \
--header 'client: JfGfbdYP5qjFoFul5tD8UQ' \
--header 'expiry: 1583828589' \
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

  url := "http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/6uqej6JT9uumY4g41CdLX7Du"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "ctgocjRjlvrDCak4ls1Dqg")
  req.Header.Add("client", "JfGfbdYP5qjFoFul5tD8UQ")
  req.Header.Add("expiry", "1583828589")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/6uqej6JT9uumY4g41CdLX7Du",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "ctgocjRjlvrDCak4ls1Dqg",
    "client": "JfGfbdYP5qjFoFul5tD8UQ",
    "expiry": "1583828589",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/6uqej6JT9uumY4g41CdLX7Du"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"ctgocjRjlvrDCak4ls1Dqg",
  @"client": @"JfGfbdYP5qjFoFul5tD8UQ",
  @"expiry": @"1583828589",
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "ctgocjRjlvrDCak4ls1Dqg")
$headers.Add("client", "JfGfbdYP5qjFoFul5tD8UQ")
$headers.Add("expiry", "1583828589")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = ""

$response = Invoke-RestMethod 'http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/6uqej6JT9uumY4g41CdLX7Du' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
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

Use this endpoint to retrieve information about specific company.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET /api/companies/:slug`

### Parameters

No parameters required.


## Create

```shell
curl --location --request POST 'http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: ctgocjRjlvrDCak4ls1Dqg' \
--header 'client: JfGfbdYP5qjFoFul5tD8UQ' \
--header 'expiry: 1583828589' \
--header 'uid: apidoc+broker@wellthie.com' \
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

  url := "http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/"
  method := "POST"

  payload := strings.NewReader("{\n  \"company\": {\n    \"name\": \"APIDocTest4\",\n    \"zip_code_input\": \"10001\",\n    \"contact_name\": \"Test\",\n    \"contact_email\": \"test@test.com\",\n    \"using_broker\": false,\n    \"broker_code\": null,\n    \"county_id\": 36061,\n    \"sic_code\": \"9999\"\n  }\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "ctgocjRjlvrDCak4ls1Dqg")
  req.Header.Add("client", "JfGfbdYP5qjFoFul5tD8UQ")
  req.Header.Add("expiry", "1583828589")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "ctgocjRjlvrDCak4ls1Dqg",
    "client": "JfGfbdYP5qjFoFul5tD8UQ",
    "expiry": "1583828589",
    "uid": "apidoc+broker@wellthie.com"
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"ctgocjRjlvrDCak4ls1Dqg",
  @"client": @"JfGfbdYP5qjFoFul5tD8UQ",
  @"expiry": @"1583828589",
  @"uid": @"apidoc+broker@wellthie.com"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "ctgocjRjlvrDCak4ls1Dqg")
$headers.Add("client", "JfGfbdYP5qjFoFul5tD8UQ")
$headers.Add("expiry", "1583828589")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = "{`n  `"company`": {`n    `"name`": `"APIDocTest4`",`n    `"zip_code_input`": `"10001`",`n    `"contact_name`": `"Test`",`n    `"contact_email`": `"test@test.com`",`n    `"using_broker`": false,`n    `"broker_code`": null,`n    `"county_id`": 36061,`n    `"sic_code`": `"9999`"`n  }`n}"

$response = Invoke-RestMethod 'http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/companies/' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
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

Use this endpoint to create a new company. Inside the request should be a json object `{}` which describes the parameters below for the company that is to be created.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`POST /api/companies`

### Parameters

Parameter          | Default | Description             | Required?
------------------ | ------- | ----------------------- | ----------
company            | N/A     | Company object          | true
name               | N/A     | name                    | true
zip_code_input     | N/A     | zipcode                 | true
contact_name       | N/A     | contact name            | true
contact_email      | N/A     | contact email           | true
using_broker       | N/A     | Using broker flag        | false
broker_code        | N/A     | Broker code             | true if using_broker, false otherwise
effective_date     | N/A     | Effective date          | true
county_id          | N/A     | county id               | true
sic_code           | N/A     | sic code                | true


## Update

```shell
curl -X PUT "/api/companies/zcZUuDSkDb7TRzTbPWmj6HSa" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A" \
     -d '{"company":{"name":"Test Company","zip_code_input":"07001","contact_name":"Test Owner","contact_email":"testowner1@company.com","using_broker":false,"broker_code":null,"effective_date":"2017-06-01","county_id":34023,"sic_code":"5411"}}'
```


```go
```

```javascript
```

```objective_c
```

```powershell
```

> Successful response looks like this:

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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`PUT /api/companies/:slug`

### Parameters

Parameter          | Default | Description             | Required?
------------------ | ------- | ----------------------- | ----------
company            | N/A     | Company object          | true
name               | N/A     | name                    | true
zip_code_input     | N/A     | zipcode                 | true
contact_name       | N/A     | contact name            | true
contact_email      | N/A     | contact email           | true
using_broker       | N/A     | Using broker flag        | false
broker_code        | N/A     | Broker code             | true if using_broker, false otherwise
effective_date     | N/A     | Effective date          | true
county_id          | N/A     | county id               | true
sic_code           | N/A     | sic code                | true


## Settings

```shell
curl -X GET "/api/companies/zcZUuDSkDb7TRzTbPWmj6HSa/settings" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A"
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
  "child_max_age_for_inclusion_in_household": 26,
  "show_group_to_individual": null,
  "default_salary_adjustment": 30,
  "business_large_group_url": "https://www.amerihealthnj.com/html/employers/large_businesses.html?",
  "business_individual_url": "https://www.healthcare.gov/"
}
```

Use this endpoint to fetch company's settings.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
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

```go
```

```javascript
```

```objective_c
```

```powershell
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
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
