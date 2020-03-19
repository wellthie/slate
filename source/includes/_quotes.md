# Quotes

Quote is an inquiry made for an individual where one or more Health insurance plans selected for a the given Individual.

* An inquiry could have more than one plan (upto 4)

Steps include to create an inquiry as follows.

1. Create Quote
2. Update Quote (if needed)
3. Get plans and pricing
4. Select plans
5. Unselect Plans (if needed)

## Create a Quote

```shell
curl --location --request POST 'https://wellthie-qa.affordablecareadvisor.net/api/quotes' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs' \
--data-raw '{
    "quote": {
        "zip_code": "10011",
        "county_id": 36061,
        "income": 40000,
        "entered_additional_hh_members": 0,
        "effective_date": "2020-03-01",
        "broker_code": "1234567890",
        "family_members_attributes": [
            {
                "first_name": "John",
                "last_name": "Doe",
                "email": "jdoe@email.com",
                "date_of_birth": "01/01/1970",
                "relationship": "Primary",
                "smoker": false,
                "declared_medicare": false,
                "declared_dependent": false
            },
            {
                "first_name": "Jane Doe",
                "last_name": null,
                "email": null,
                "date_of_birth": "01/01/1970",
                "relationship": "Spouse",
                "smoker": false,
                "declared_medicare": false,
                "declared_dependent": false
            },
            {
                "first_name": "Jim Doe",
                "last_name": null,
                "email": null,
                "date_of_birth": "01/01/2010",
                "relationship": "Child",
                "smoker": false,
                "declared_medicare": false,
                "declared_dependent": false
            }
        ]
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

  url := "https://wellthie-qa.affordablecareadvisor.net/api/quotes"
  method := "POST"

  payload := strings.NewReader("{\n    \"quote\": {\n        \"zip_code\": \"10011\",\n        \"county_id\": 36061,\n        \"income\": 40000,\n        \"entered_additional_hh_members\": 0,\n        \"effective_date\": \"2020-03-01\",\n        \"broker_code\": \"1234567890\",\n        \"family_members_attributes\": [\n            {\n                \"first_name\": \"John\",\n                \"last_name\": \"Doe\",\n                \"email\": \"jdoe@email.com\",\n                \"date_of_birth\": \"01/01/1970\",\n                \"relationship\": \"Primary\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            },\n            {\n                \"first_name\": \"Jane Doe\",\n                \"last_name\": null,\n                \"email\": null,\n                \"date_of_birth\": \"01/01/1970\",\n                \"relationship\": \"Spouse\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            },\n            {\n                \"first_name\": \"Jim Doe\",\n                \"last_name\": null,\n                \"email\": null,\n                \"date_of_birth\": \"01/01/2010\",\n                \"relationship\": \"Child\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            }\n        ]\n    }\n}")

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
  "url": "https://wellthie-qa.affordablecareadvisor.net/api/quotes",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
  },
  "data": JSON.stringify({"quote":{"zip_code":"10011","county_id":36061,"income":40000,"entered_additional_hh_members":0,"effective_date":"2020-03-01","broker_code":"1234567890","family_members_attributes":[{"first_name":"John","last_name":"Doe","email":"jdoe@email.com","date_of_birth":"01/01/1970","relationship":"Primary","smoker":false,"declared_medicare":false,"declared_dependent":false},{"first_name":"Jane Doe","last_name":null,"email":null,"date_of_birth":"01/01/1970","relationship":"Spouse","smoker":false,"declared_medicare":false,"declared_dependent":false},{"first_name":"Jim Doe","last_name":null,"email":null,"date_of_birth":"01/01/2010","relationship":"Child","smoker":false,"declared_medicare":false,"declared_dependent":false}]}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthie-qa.affordablecareadvisor.net/api/quotes"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n    \"quote\": {\n        \"zip_code\": \"10011\",\n        \"county_id\": 36061,\n        \"income\": 40000,\n        \"entered_additional_hh_members\": 0,\n        \"effective_date\": \"2020-03-01\",\n        \"broker_code\": \"1234567890\",\n        \"family_members_attributes\": [\n            {\n                \"first_name\": \"John\",\n                \"last_name\": \"Doe\",\n                \"email\": \"jdoe@email.com\",\n                \"date_of_birth\": \"01/01/1970\",\n                \"relationship\": \"Primary\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            },\n            {\n                \"first_name\": \"Jane Doe\",\n                \"last_name\": null,\n                \"email\": null,\n                \"date_of_birth\": \"01/01/1970\",\n                \"relationship\": \"Spouse\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            },\n            {\n                \"first_name\": \"Jim Doe\",\n                \"last_name\": null,\n                \"email\": null,\n                \"date_of_birth\": \"01/01/2010\",\n                \"relationship\": \"Child\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            }\n        ]\n    }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

$body = "{`n    `"quote`": {`n        `"zip_code`": `"10011`",`n        `"county_id`": 36061,`n        `"income`": 40000,`n        `"entered_additional_hh_members`": 0,`n        `"effective_date`": `"2020-03-01`",`n        `"broker_code`": `"1234567890`",`n        `"family_members_attributes`": [`n            {`n                `"first_name`": `"John`",`n                `"last_name`": `"Doe`",`n                `"email`": `"jdoe@email.com`",`n                `"date_of_birth`": `"01/01/1970`",`n                `"relationship`": `"Primary`",`n                `"smoker`": false,`n                `"declared_medicare`": false,`n                `"declared_dependent`": false`n            },`n            {`n                `"first_name`": `"Jane Doe`",`n                `"last_name`": null,`n                `"email`": null,`n                `"date_of_birth`": `"01/01/1970`",`n                `"relationship`": `"Spouse`",`n                `"smoker`": false,`n                `"declared_medicare`": false,`n                `"declared_dependent`": false`n            },`n            {`n                `"first_name`": `"Jim Doe`",`n                `"last_name`": null,`n                `"email`": null,`n                `"date_of_birth`": `"01/01/2010`",`n                `"relationship`": `"Child`",`n                `"smoker`": false,`n                `"declared_medicare`": false,`n                `"declared_dependent`": false`n            }`n        ]`n    }`n}"

$response = Invoke-RestMethod 'https://wellthie-qa.affordablecareadvisor.net/api/quotes' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "id": "GC-176549",
    "zip_code": "10011",
    "county_id": 36061,
    "rating_zone_id": 1322,
    "income": 40000.0,
    "entered_additional_hh_members": 0,
    "effective_date": "2020-03-01",
    "fpl": "1.875293014533520863",
    "tax_penalty": 1737.5,
    "broker_code": "1234567890",
    "sep_qualifying_event": null,
    "sep_qualifying_event_date": null,
    "active_enrollment": false,
    "family_members": [
        {
            "id": 68650,
            "first_name": "John",
            "email": "jdoe@email.com",
            "last_name": "Doe",
            "date_of_birth": "01/01/1970",
            "age": 50,
            "relationship": "Primary",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        },
        {
            "id": 68651,
            "first_name": "Jane Doe",
            "email": null,
            "last_name": null,
            "date_of_birth": "01/01/1970",
            "age": 50,
            "relationship": "Spouse",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        },
        {
            "id": 68652,
            "first_name": "Jim Doe",
            "email": null,
            "last_name": null,
            "date_of_birth": "01/01/2010",
            "age": 10,
            "relationship": "Child",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        }
    ]
}
```

Use this endpoint to create a new quote.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>

### HTTP Request

`POST /api/quotes`

### Parameters

Parameter                                                                    | Default   | Description
-----------------------------------------------------------------------------| --------- | -----------
<strong>effective_date</strong><strong>required</strong>                     | N/A       |
<strong>zip_code</strong><strong>required</strong>                           | N/A       |
<strong>county_code</strong><strong>required</strong>                        | N/A       |
<strong>income</strong><strong>required</strong>                             | N/A       |
<strong>family_members_attributes</strong><strong>required</strong>          | N/A       | Array of { "first_name": "", "last_name": "", "email": "", "date_of_birth": "mm/dd/yyyy", "relationship": "Primary", "smoker": boolean, "declared_medicare": boolean, "declared_dependent": boolean }

## Update a Quote

```shell
curl --location --request PUT 'https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs' \
--data-raw '{
    "quote": {
        "zip_code": "10011",
        "county_id": 36061,
        "income": 140000,
        "entered_additional_hh_members": 0,
        "effective_date": "2020-03-01",
        "broker_code": "1234567890",
        "family_members_attributes": [
            {
                "first_name": "John",
                "last_name": "Doe",
                "email": "jdoe@email.com",
                "date_of_birth": "01/01/1970",
                "relationship": "Primary",
                "smoker": false,
                "declared_medicare": false,
                "declared_dependent": false
            },
            {
                "first_name": "Jane Doe",
                "last_name": null,
                "email": null,
                "date_of_birth": "01/01/1970",
                "relationship": "Spouse",
                "smoker": false,
                "declared_medicare": false,
                "declared_dependent": false
            },
            {
                "first_name": "Jim Doe",
                "last_name": null,
                "email": null,
                "date_of_birth": "01/01/2010",
                "relationship": "Child",
                "smoker": false,
                "declared_medicare": false,
                "declared_dependent": false
            }
        ]
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

  url := "https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864"
  method := "PUT"

  payload := strings.NewReader("{\n    \"quote\": {\n        \"zip_code\": \"10011\",\n        \"county_id\": 36061,\n        \"income\": 140000,\n        \"entered_additional_hh_members\": 0,\n        \"effective_date\": \"2020-03-01\",\n        \"broker_code\": \"1234567890\",\n        \"family_members_attributes\": [\n            {\n                \"first_name\": \"John\",\n                \"last_name\": \"Doe\",\n                \"email\": \"jdoe@email.com\",\n                \"date_of_birth\": \"01/01/1970\",\n                \"relationship\": \"Primary\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            },\n            {\n                \"first_name\": \"Jane Doe\",\n                \"last_name\": null,\n                \"email\": null,\n                \"date_of_birth\": \"01/01/1970\",\n                \"relationship\": \"Spouse\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            },\n            {\n                \"first_name\": \"Jim Doe\",\n                \"last_name\": null,\n                \"email\": null,\n                \"date_of_birth\": \"01/01/2010\",\n                \"relationship\": \"Child\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            }\n        ]\n    }\n}")

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
  "url": "https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864",
  "method": "PUT",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
  },
  "data": JSON.stringify({"quote":{"zip_code":"10011","county_id":36061,"income":140000,"entered_additional_hh_members":0,"effective_date":"2020-03-01","broker_code":"1234567890","family_members_attributes":[{"first_name":"John","last_name":"Doe","email":"jdoe@email.com","date_of_birth":"01/01/1970","relationship":"Primary","smoker":false,"declared_medicare":false,"declared_dependent":false},{"first_name":"Jane Doe","last_name":null,"email":null,"date_of_birth":"01/01/1970","relationship":"Spouse","smoker":false,"declared_medicare":false,"declared_dependent":false},{"first_name":"Jim Doe","last_name":null,"email":null,"date_of_birth":"01/01/2010","relationship":"Child","smoker":false,"declared_medicare":false,"declared_dependent":false}]}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n    \"quote\": {\n        \"zip_code\": \"10011\",\n        \"county_id\": 36061,\n        \"income\": 140000,\n        \"entered_additional_hh_members\": 0,\n        \"effective_date\": \"2020-03-01\",\n        \"broker_code\": \"1234567890\",\n        \"family_members_attributes\": [\n            {\n                \"first_name\": \"John\",\n                \"last_name\": \"Doe\",\n                \"email\": \"jdoe@email.com\",\n                \"date_of_birth\": \"01/01/1970\",\n                \"relationship\": \"Primary\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            },\n            {\n                \"first_name\": \"Jane Doe\",\n                \"last_name\": null,\n                \"email\": null,\n                \"date_of_birth\": \"01/01/1970\",\n                \"relationship\": \"Spouse\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            },\n            {\n                \"first_name\": \"Jim Doe\",\n                \"last_name\": null,\n                \"email\": null,\n                \"date_of_birth\": \"01/01/2010\",\n                \"relationship\": \"Child\",\n                \"smoker\": false,\n                \"declared_medicare\": false,\n                \"declared_dependent\": false\n            }\n        ]\n    }\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

$body = "{`n    `"quote`": {`n        `"zip_code`": `"10011`",`n        `"county_id`": 36061,`n        `"income`": 140000,`n        `"entered_additional_hh_members`": 0,`n        `"effective_date`": `"2020-03-01`",`n        `"broker_code`": `"1234567890`",`n        `"family_members_attributes`": [`n            {`n                `"first_name`": `"John`",`n                `"last_name`": `"Doe`",`n                `"email`": `"jdoe@email.com`",`n                `"date_of_birth`": `"01/01/1970`",`n                `"relationship`": `"Primary`",`n                `"smoker`": false,`n                `"declared_medicare`": false,`n                `"declared_dependent`": false`n            },`n            {`n                `"first_name`": `"Jane Doe`",`n                `"last_name`": null,`n                `"email`": null,`n                `"date_of_birth`": `"01/01/1970`",`n                `"relationship`": `"Spouse`",`n                `"smoker`": false,`n                `"declared_medicare`": false,`n                `"declared_dependent`": false`n            },`n            {`n                `"first_name`": `"Jim Doe`",`n                `"last_name`": null,`n                `"email`": null,`n                `"date_of_birth`": `"01/01/2010`",`n                `"relationship`": `"Child`",`n                `"smoker`": false,`n                `"declared_medicare`": false,`n                `"declared_dependent`": false`n            }`n        ]`n    }`n}"

$response = Invoke-RestMethod 'https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864' -Method 'PUT' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "id": "SW-759864",
    "zip_code": "10011",
    "county_id": 36061,
    "rating_zone_id": 1322,
    "income": 140000.0,
    "entered_additional_hh_members": 0,
    "effective_date": "2020-03-01",
    "fpl": "6.563525550867323019",
    "tax_penalty": "2982.5",
    "broker_code": "1234567890",
    "sep_qualifying_event": null,
    "sep_qualifying_event_date": null,
    "active_enrollment": true,
    "family_members": [
        {
            "id": 68653,
            "first_name": "John",
            "email": "jdoe@email.com",
            "last_name": "Doe",
            "date_of_birth": "01/01/1970",
            "age": 50,
            "relationship": "Primary",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        },
        {
            "id": 68654,
            "first_name": "Jane Doe",
            "email": null,
            "last_name": null,
            "date_of_birth": "01/01/1970",
            "age": 50,
            "relationship": "Spouse",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        },
        {
            "id": 68655,
            "first_name": "Jim Doe",
            "email": null,
            "last_name": null,
            "date_of_birth": "01/01/2010",
            "age": 10,
            "relationship": "Child",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        }
    ]
}
```

Use this endpoint to update an quote.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>


### HTTP Request

`PUT /api/quotes/:quote_id`

### Parameters

Parameter                                                                    | Default   | Description
-----------------------------------------------------------------------------| --------- | -----------
<strong>effective_date</strong><strong>required</strong>                     | N/A       |
<strong>zip_code</strong><strong>required</strong>                           | N/A       |
<strong>county_code</strong><strong>required</strong>                        | N/A       |
<strong>income</strong><strong>required</strong>                             | N/A       |
<strong>family_members_attributes</strong><strong>required</strong>          | N/A       | Array of { "first_name": "", "last_name": "", "email": "", "date_of_birth": "mm/dd/yyyy", "relationship": "Primary", "smoker": boolean, "declared_medicare": boolean, "declared_dependent": boolean }

## Get a Quote

```shell
curl --location --request GET 'https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864' \
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

  url := "https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864"
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
  "url": "https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864"]
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

$response = Invoke-RestMethod 'https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-759864' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "id": "SW-759864",
    "zip_code": "10011",
    "county_id": 36061,
    "rating_zone_id": 1322,
    "income": 140000.0,
    "entered_additional_hh_members": 0,
    "effective_date": "2020-03-01",
    "fpl": "6.563525550867323019",
    "tax_penalty": "2982.5",
    "broker_code": "1234567890",
    "sep_qualifying_event": null,
    "sep_qualifying_event_date": null,
    "active_enrollment": true,
    "family_members": [
        {
            "id": 68641,
            "first_name": "John",
            "email": "jdoe@email.com",
            "last_name": "Doe",
            "date_of_birth": "01/01/1970",
            "age": 50,
            "relationship": "Primary",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        },
        {
            "id": 68642,
            "first_name": "Jane Doe",
            "email": null,
            "last_name": null,
            "date_of_birth": "01/01/1970",
            "age": 50,
            "relationship": "Spouse",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        },
        {
            "id": 68643,
            "first_name": "Jim Doe",
            "email": null,
            "last_name": null,
            "date_of_birth": "01/01/2010",
            "age": 10,
            "relationship": "Child",
            "smoker": false,
            "declared_medicare": false,
            "declared_dependent": false
        }
    ]
}
```

Use this endpoint to fetch a particular quote.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>

### HTTP Request

`GET /api/quotes/:quote_id`

### Parameters

No parameters required.

## Review a Quote

```shell
curl --location --request GET 'https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-284971/review' \
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

  url := "https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-284971/review"
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
  "url": "https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-284971/review",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-284971/review"]
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

$response = Invoke-RestMethod 'https://wellthie-qa.affordablecareadvisor.net/api/quotes/SW-284971/review' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
    {
        "medical_plan_id": 11676,
        "redirect_url": "https://nystateofhealth.ny.gov",
        "redirect_url_title": "",
        "enroll_path": "use-3rd-party-integration",
        "post_data_to_3rd_party": true,
        "post_data_to_url": "https://portals4.emblemhealth.com/Stg-CAEnrollment-Med/uiEnrollmentWellthieRedirect.aspx",
        "on_exchange": false,
        "off_exchange": true,
        "exchange_type": "state",
        "enrollment_content": "QHP Off Exchange Pre-Enrollment Information"
    },
    {
        "medical_plan_id": 11693,
        "redirect_url": "http://www.emblemhealth.com/Our-Plans/Medicare/Enroll-In-a-Plan.aspx",
        "redirect_url_title": "Enrollment",
        "enroll_path": "redirect",
        "post_data_to_3rd_party": true,
        "post_data_to_url": "https://portals4.emblemhealth.com/Stg-CAEnrollment-Med/uiEnrollmentWellthieRedirect.aspx",
        "on_exchange": false,
        "off_exchange": false,
        "exchange_type": "state",
        "enrollment_content": "Medicare Pre-Enrollment Information"
    }
]
```

Use this endpoint to fetch a particular quote.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i> Authorization headers</i></strong>. 
</aside>

### HTTP Request

`GET /api/quotes/:quote_id/review`

### Parameters

No parameters required.
