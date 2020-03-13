# Companies

## Get Company Details

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/6uqej6JT9uumY4g41CdLX7Du' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/6uqej6JT9uumY4g41CdLX7Du"
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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/6uqej6JT9uumY4g41CdLX7Du",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/6uqej6JT9uumY4g41CdLX7Du"]
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

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/6uqej6JT9uumY4g41CdLX7Du' -Method 'GET' -Headers $headers -Body $body
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

## Create Company

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/' \
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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/"]
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
curl -X PUT "/api/companies/zcZUuDSkDb7TRzTbPWmj6HSa" \
     -H "Content-Type: application/json" \
     -H "access-token: v5KcdlSSGlCVh_ZYHDo8SA" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: -FPYre3uK1DYkjDYZOuk5A" \
     -d '{"company":{"name":"Test Company","zip_code_input":"07001","contact_name":"Test Owner","contact_email":"testowner1@company.com","using_broker":false,"broker_code":null,"effective_date":"2017-06-01","county_id":34023,"sic_code":"5411"}}'
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ"
  method := "PUT"

  payload := strings.NewReader("{\n  \"company\": {\n    \"name\": \"APIDoc Test4\",\n    \"zip_code_input\": \"10001\",\n    \"contact_name\": \"Test\",\n    \"contact_email\": \"test@test.com\",\n    \"using_broker\": false,\n    \"broker_code\": null,\n    \"county_id\": 36061,\n    \"sic_code\": \"9999\"\n  }\n}")

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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ",
  "method": "PUT",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "ctgocjRjlvrDCak4ls1Dqg",
    "client": "JfGfbdYP5qjFoFul5tD8UQ",
    "expiry": "1583828589",
    "uid": "apidoc+broker@wellthie.com"
  },
  "data": JSON.stringify({"company":{"name":"APIDoc Test4","zip_code_input":"10001","contact_name":"Test","contact_email":"test@test.com","using_broker":false,"broker_code":null,"county_id":36061,"sic_code":"9999"}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ"]
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
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"company\": {\n    \"name\": \"APIDoc Test4\",\n    \"zip_code_input\": \"10001\",\n    \"contact_name\": \"Test\",\n    \"contact_email\": \"test@test.com\",\n    \"using_broker\": false,\n    \"broker_code\": null,\n    \"county_id\": 36061,\n    \"sic_code\": \"9999\"\n  }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22ctgocjRjlvrDCak4ls1Dqg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22JfGfbdYP5qjFoFul5tD8UQ%22%2C%22expiry%22%3A%221583828589%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "ctgocjRjlvrDCak4ls1Dqg")
$headers.Add("client", "JfGfbdYP5qjFoFul5tD8UQ")
$headers.Add("expiry", "1583828589")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = "{`n  `"company`": {`n    `"name`": `"APIDoc Test4`",`n    `"zip_code_input`": `"10001`",`n    `"contact_name`": `"Test`",`n    `"contact_email`": `"test@test.com`",`n    `"using_broker`": false,`n    `"broker_code`": null,`n    `"county_id`": 36061,`n    `"sic_code`": `"9999`"`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ' -Method 'PUT' -Headers $headers -Body $body
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

## Get Company Settings

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/settings' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22aKF3cRUN8JCvJ-LB50Fx8w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22oHiaog8REElQVaA0JUotng%22%2C%22expiry%22%3A%221584092320%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: aKF3cRUN8JCvJ-LB50Fx8w' \
--header 'client: oHiaog8REElQVaA0JUotng' \
--header 'expiry: 1584092320' \
--header 'uid: apidoc+broker@wellthie.com' \
--header 'Authorization: Bearer DT2KcU6A7F9tIvOC1pc3lg' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/settings"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22aKF3cRUN8JCvJ-LB50Fx8w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22oHiaog8REElQVaA0JUotng%22%2C%22expiry%22%3A%221584092320%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "aKF3cRUN8JCvJ-LB50Fx8w")
  req.Header.Add("client", "oHiaog8REElQVaA0JUotng")
  req.Header.Add("expiry", "1584092320")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")
  req.Header.Add("Authorization", "Bearer DT2KcU6A7F9tIvOC1pc3lg")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/settings",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22aKF3cRUN8JCvJ-LB50Fx8w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22oHiaog8REElQVaA0JUotng%22%2C%22expiry%22%3A%221584092320%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "aKF3cRUN8JCvJ-LB50Fx8w",
    "client": "oHiaog8REElQVaA0JUotng",
    "expiry": "1584092320",
    "uid": "apidoc+broker@wellthie.com",
    "Authorization": "Bearer DT2KcU6A7F9tIvOC1pc3lg"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/settings"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22aKF3cRUN8JCvJ-LB50Fx8w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22oHiaog8REElQVaA0JUotng%22%2C%22expiry%22%3A%221584092320%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"aKF3cRUN8JCvJ-LB50Fx8w",
  @"client": @"oHiaog8REElQVaA0JUotng",
  @"expiry": @"1584092320",
  @"uid": @"apidoc+broker@wellthie.com",
  @"Authorization": @"Bearer DT2KcU6A7F9tIvOC1pc3lg"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22aKF3cRUN8JCvJ-LB50Fx8w%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22oHiaog8REElQVaA0JUotng%22%2C%22expiry%22%3A%221584092320%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "aKF3cRUN8JCvJ-LB50Fx8w")
$headers.Add("client", "oHiaog8REElQVaA0JUotng")
$headers.Add("expiry", "1584092320")
$headers.Add("uid", "apidoc+broker@wellthie.com")
$headers.Add("Authorization", "Bearer DT2KcU6A7F9tIvOC1pc3lg")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/companies/shy8pmfek8ZpGKJYneD2g5TJ/settings' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "child_max_age_for_inclusion_in_household": 26,
    "allow_group_and_group_to_individual": true,
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

## Get Company's Current Plan

<aside class="notice">
  Current plan details are sent as part of <a href="#get-company-details">Get Company Details</a>
</aside>

## Create Company's Current Plan

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB7928/current_plan' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D' \
--header 'access-token: ' \
--header 'client: ' \
--header 'expiry: ' \
--header 'uid: ' \
--data-raw '{
  "current_plan": {
    "product_type": "medical",
    "name": "Current Plan Name",
    "current_plan_issuer": "Current Plan Issuer",
    "metal_level_name": "Bronze",
    "employer_monthly_cost": 1000,
    "carrier_plan_identifier": "123",
    "medical_deductible_single": "Deductible Single",
    "medical_deductible_family": "Deductible Single",
    "maximum_out_of_pocket_limit_single": "Deductible Single",
    "specialist": "Specialist",
    "pcp": "Primary Care Physician",
    "maximum_out_of_pocket_limit_family": "Max-Out-of-Pocket Family",
    "network_type": "Network",
    "preventive_care": "Preventive Care",
    "inpatient_facility": "Hospital (Inpatient)",
    "emergency_room": "Emergency Room",
    "ambulance": "Ambulance",
    "urgent_care": "Urgent Care",
    "generic": "Generic Prescription",
    "formulary_brand": "Formulary Prescription",
    "non_formulary_brand": "Non Formulary Brand Prescription",
    "mail_order": "Mail Order (90 day supply)"
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB7928/current_plan"
  method := "POST"

  payload := strings.NewReader("{\n  \"current_plan\": {\n    \"product_type\": \"medical\",\n    \"name\": \"Current Plan Name\",\n    \"current_plan_issuer\": \"Current Plan Issuer\",\n    \"metal_level_name\": \"Bronze\",\n    \"employer_monthly_cost\": 1000,\n    \"carrier_plan_identifier\": \"123\",\n    \"medical_deductible_single\": \"Deductible Single\",\n    \"medical_deductible_family\": \"Deductible Single\",\n    \"maximum_out_of_pocket_limit_single\": \"Deductible Single\",\n    \"specialist\": \"Specialist\",\n    \"pcp\": \"Primary Care Physician\",\n    \"maximum_out_of_pocket_limit_family\": \"Max-Out-of-Pocket Family\",\n    \"network_type\": \"Network\",\n    \"preventive_care\": \"Preventive Care\",\n    \"inpatient_facility\": \"Hospital (Inpatient)\",\n    \"emergency_room\": \"Emergency Room\",\n    \"ambulance\": \"Ambulance\",\n    \"urgent_care\": \"Urgent Care\",\n    \"generic\": \"Generic Prescription\",\n    \"formulary_brand\": \"Formulary Prescription\",\n    \"non_formulary_brand\": \"Non Formulary Brand Prescription\",\n    \"mail_order\": \"Mail Order (90 day supply)\"\n  }\n}")

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

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB7928/current_plan",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D",
    "access-token": "",
    "client": "",
    "expiry": "",
    "uid": ""
  },
  "data": JSON.stringify({"current_plan":{"product_type":"medical","name":"Current Plan Name","current_plan_issuer":"Current Plan Issuer","metal_level_name":"Bronze","employer_monthly_cost":1000,"carrier_plan_identifier":"123","medical_deductible_single":"Deductible Single","medical_deductible_family":"Deductible Single","maximum_out_of_pocket_limit_single":"Deductible Single","specialist":"Specialist","pcp":"Primary Care Physician","maximum_out_of_pocket_limit_family":"Max-Out-of-Pocket Family","network_type":"Network","preventive_care":"Preventive Care","inpatient_facility":"Hospital (Inpatient)","emergency_room":"Emergency Room","ambulance":"Ambulance","urgent_care":"Urgent Care","generic":"Generic Prescription","formulary_brand":"Formulary Prescription","non_formulary_brand":"Non Formulary Brand Prescription","mail_order":"Mail Order (90 day supply)"}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB7928/current_plan"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D",
  @"access-token": @"",
  @"client": @"",
  @"expiry": @"",
  @"uid": @""
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"current_plan\": {\n    \"product_type\": \"medical\",\n    \"name\": \"Current Plan Name\",\n    \"current_plan_issuer\": \"Current Plan Issuer\",\n    \"metal_level_name\": \"Bronze\",\n    \"employer_monthly_cost\": 1000,\n    \"carrier_plan_identifier\": \"123\",\n    \"medical_deductible_single\": \"Deductible Single\",\n    \"medical_deductible_family\": \"Deductible Single\",\n    \"maximum_out_of_pocket_limit_single\": \"Deductible Single\",\n    \"specialist\": \"Specialist\",\n    \"pcp\": \"Primary Care Physician\",\n    \"maximum_out_of_pocket_limit_family\": \"Max-Out-of-Pocket Family\",\n    \"network_type\": \"Network\",\n    \"preventive_care\": \"Preventive Care\",\n    \"inpatient_facility\": \"Hospital (Inpatient)\",\n    \"emergency_room\": \"Emergency Room\",\n    \"ambulance\": \"Ambulance\",\n    \"urgent_care\": \"Urgent Care\",\n    \"generic\": \"Generic Prescription\",\n    \"formulary_brand\": \"Formulary Prescription\",\n    \"non_formulary_brand\": \"Non Formulary Brand Prescription\",\n    \"mail_order\": \"Mail Order (90 day supply)\"\n  }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D")
$headers.Add("access-token", "")
$headers.Add("client", "")
$headers.Add("expiry", "")
$headers.Add("uid", "")

$body = "{`n  `"current_plan`": {`n    `"product_type`": `"medical`",`n    `"name`": `"Current Plan Name`",`n    `"current_plan_issuer`": `"Current Plan Issuer`",`n    `"metal_level_name`": `"Bronze`",`n    `"employer_monthly_cost`": 1000,`n    `"carrier_plan_identifier`": `"123`",`n    `"medical_deductible_single`": `"Deductible Single`",`n    `"medical_deductible_family`": `"Deductible Single`",`n    `"maximum_out_of_pocket_limit_single`": `"Deductible Single`",`n    `"specialist`": `"Specialist`",`n    `"pcp`": `"Primary Care Physician`",`n    `"maximum_out_of_pocket_limit_family`": `"Max-Out-of-Pocket Family`",`n    `"network_type`": `"Network`",`n    `"preventive_care`": `"Preventive Care`",`n    `"inpatient_facility`": `"Hospital (Inpatient)`",`n    `"emergency_room`": `"Emergency Room`",`n    `"ambulance`": `"Ambulance`",`n    `"urgent_care`": `"Urgent Care`",`n    `"generic`": `"Generic Prescription`",`n    `"formulary_brand`": `"Formulary Prescription`",`n    `"non_formulary_brand`": `"Non Formulary Brand Prescription`",`n    `"mail_order`": `"Mail Order (90 day supply)`"`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/AGKB7928/current_plan' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
  "id": 4001,
  "current_plan_issuer": "Current Plan Issuer",
  "name": "Current Plan Name",
  "company_id": 107614,
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
  "employer_monthly_cost": 1000
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

`POST /api/companies/:company_slug/current_plan`

### Parameters

Parameter                                                       | Default   | Description
--------------------------------------------------------------- | --------- | --------------------------
current_plan[current_plan_issuer]                               | N/A       | Issuer for this plan
<strong>current_plan[name]</strong><strong>required</strong>    | N/A       | Plan name
current_plan[company_id]                                        | N/A       | Company's id
current_plan[metal_level_name]                                  | N/A       | Metal level for plan
current_plan[medical_deductible_single]                         | N/A       | Medical deductible single
current_plan[medical_deductible_family]                         | N/A       | Medical deductible family
current_plan[maximum_out_of_pocket_limit_single]                | N/A       | Max out of pocket single
current_plan[maximum_out_of_pocket_limit_family]                | N/A       | Max out of pocket family
current_plan[pcp]                                               | N/A       | PCP
current_plan[specialist]                                        | N/A       | Specialist
current_plan[network_type]                                      | N/A       | Network Type
current_plan[preventive_care]                                   | N/A       | Preventive Care
current_plan[inpatient_facility]                                | N/A       | Inpatient Facility
current_plan[emergency_room]                                    | N/A       | Emergency Room
current_plan[ambulance]                                         | N/A       | Ambulance
current_plan[urgent_care]                                       | N/A       | Urgent Care
current_plan[generic]                                           | N/A       | Generic
current_plan[highlight_1]                                       | N/A       | Highlight 1
current_plan[highlight_2]                                       | N/A       | Highlight 2
current_plan[highlight_3]                                       | N/A       | Highlight 3
current_plan[formulary_brand]                                   | N/A       | Formulary Brand
current_plan[non_formulary_brand]                               | N/A       | Non-Formulary Brand
current_plan[mail_order]                                        | N/A       | Mail Order
current_plan[employer_monthly_cost]                             | N/A       | Employer Monthly Cost