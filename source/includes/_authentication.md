# Authentication

## Register a Broker User

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth' \
--header 'Content-Type: application/json' \
--data-raw '{
  "email": "apidoc+broker@wellthie.com",
  "first_name": "firstName",
  "last_name": "lastName",
  "npn": "123456",
  "password": "Password123",
  "password_confirmation": "Password123"
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth"
  method := "POST"

  payload := strings.NewReader("{\n  \"email\": \"apidoc+broker@wellthie.com\",\n  \"first_name\": \"firstName\",\n  \"last_name\": \"lastName\",\n  \"npn\": \"123456\",\n  \"password\": \"Password123\",\n  \"password_confirmation\": \"Password123\"\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json"
  },
  "data": JSON.stringify({"email":"apidoc+broker@wellthie.com","first_name":"firstName","last_name":"lastName","npn":"123456","password":"Password123","password_confirmation":"Password123"}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"email\": \"apidoc+broker@wellthie.com\",\n  \"first_name\": \"firstName\",\n  \"last_name\": \"lastName\",\n  \"npn\": \"123456\",\n  \"password\": \"Password123\",\n  \"password_confirmation\": \"Password123\"\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

$body = "{`n  `"email`": `"apidoc+broker@wellthie.com`",`n  `"first_name`": `"firstName`",`n  `"last_name`": `"lastName`",`n  `"npn`": `"123456`",`n  `"password`": `"Password123`",`n  `"password_confirmation`": `"Password123`"`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "data": {
        "id": 58464,
        "slug": "abdxoCCvz6oLyHcmpR3Z9wG5",
        "first_name": "firstName",
        "last_name": "lastName",
        "email": "apidoc+broker1@wellthie.com",
        "provider": "email",
        "uid": "apidoc+broker1@wellthie.com",
        "password_changed_at": "2020-03-16T03:03:19.589-04:00",
        "organization_id": 23,
        "team_id": null,
        "role": "broker",
        "user_type": null,
        "npn_trash": null,
        "broker_code": "123456",
        "phone_number": null,
        "account_expiration_date": null,
        "created_by_user_id": null,
        "time_zone": "Eastern Time (US & Canada)",
        "deleted_at": null,
        "salesforce_email": null,
        "salesforce_access_token": null,
        "salesforce_refresh_token": null,
        "salesforce_lock": false,
        "company_id": null,
        "allow_password_change": false,
        "is_any_broker_type": true,
        "access_token": "eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ2NCwiY2xpZW50IjoiSEszeWNlOEY3VF95UXdBalhQMlR6dyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZTgzYzY2NjhmM2YwMmJlODg5OWIxODQwYjQwNzViOGEiLCJleHAiOjE1ODQ0Mjg2MDB9.dWrw41qnHA224Dn8cN3dYM0RzXKx2yPkzMwZS_xtWIs"
    }
}
```

Use this endpoint to Register a new Individual User.

### HTTP Request

`POST /api/auth`

### Parameters

Parameter                                                         | Default   | Description
----------------------------------------------------------------- | --------- | -------------------
<strong>email</strong><strong>required</strong>                   | N/A       | Email Address
<strong>first_name</strong><strong>required</strong>               | N/A       | First Name
<strong>last_name</strong><strong>required</strong>               | N/A       | Last Name
<strong>password</strong><strong>required</strong>                | N/A       | Password
<strong>password_confirmation</strong><strong>required</strong>    | N/A       | Password Confirmation

## Register a Employer User

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth' \
--header 'Content-Type: application/json' \
--data-raw '{
  "email": "apidoc+employer@wellthie.com",
  "first_name": "Kannan",
  "last_name": "Ramakrishnan",
  "password": "Password123",
  "password_confirmation": "Password123"
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth"
  method := "POST"

  payload := strings.NewReader("{\n  \"email\": \"apidoc+employer@wellthie.com\",\n  \"first_name\": \"Kannan\",\n  \"last_name\": \"Ramakrishnan\",\n  \"password\": \"Password123\",\n  \"password_confirmation\": \"Password123\"\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json"
  },
  "data": JSON.stringify({"email":"apidoc+employer@wellthie.com","first_name":"Kannan","last_name":"Ramakrishnan","password":"Password123","password_confirmation":"Password123"}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"email\": \"apidoc+employer@wellthie.com\",\n  \"first_name\": \"Kannan\",\n  \"last_name\": \"Ramakrishnan\",\n  \"password\": \"Password123\",\n  \"password_confirmation\": \"Password123\"\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

$body = "{`n  `"email`": `"apidoc+employer@wellthie.com`",`n  `"first_name`": `"Kannan`",`n  `"last_name`": `"Ramakrishnan`",`n  `"password`": `"Password123`",`n  `"password_confirmation`": `"Password123`"`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "data": {
        "id": 58465,
        "slug": "miB7r7pw2jYXRez6sYyhWptW",
        "first_name": "Kannan",
        "last_name": "Ramakrishnan",
        "email": "apidoc+employer1@wellthie.com",
        "provider": "email",
        "uid": "apidoc+employer1@wellthie.com",
        "password_changed_at": "2020-03-16T03:03:31.002-04:00",
        "organization_id": 23,
        "team_id": null,
        "role": "business_owner",
        "user_type": null,
        "npn_trash": null,
        "broker_code": null,
        "phone_number": null,
        "account_expiration_date": null,
        "created_by_user_id": null,
        "time_zone": "Eastern Time (US & Canada)",
        "deleted_at": null,
        "salesforce_email": null,
        "salesforce_access_token": null,
        "salesforce_refresh_token": null,
        "salesforce_lock": false,
        "company_id": null,
        "allow_password_change": false,
        "is_any_broker_type": false,
        "access_token": "eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ2NSwiY2xpZW50IjoiU1FxSVJ6d09pRmJlR2U1Umk0LUlvdyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiMDYyMGQwNGExYzdlZTg4NDM4NmMzODEwNjYwODU3ZjAiLCJleHAiOjE1ODQ0Mjg2MTF9.QmKsEp-TWFgXR8_Z_wNDykBbiCeLSQXVAZv3r4nx7pE"
    }
}
```

Use this endpoint to Register a new Individual User.

### HTTP Request

`POST /api/auth`

### Parameters

Parameter                                                         | Default   | Description
----------------------------------------------------------------- | --------- | -------------------
<strong>email</strong><strong>required</strong>                   | N/A       | Email Address
<strong>first_name</strong><strong>required</strong>               | N/A       | First Name
<strong>last_name</strong><strong>required</strong>               | N/A       | Last Name
<strong>password</strong><strong>required</strong>                | N/A       | Password
<strong>password_confirmation</strong><strong>required</strong>    | N/A       | Password Confirmation

## Sign In

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_in' \
--header 'Content-Type: application/json' \
--data-raw '{ "email":"apidoc+broker@wellthie.com", "password":"Password123" }'
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_in"
  method := "POST"

  payload := strings.NewReader("{\n	\"email\":\"apidoc+broker@wellthie.com\",\n	\"password\":\"Password123\"\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_in",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json"
  },
  "data": JSON.stringify({"email":"apidoc+broker@wellthie.com","password":"Password123"}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_in"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n	\"email\":\"apidoc+broker@wellthie.com\",\n	\"password\":\"Password123\"\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

$body = "{`n	`"email`":`"apidoc+broker@wellthie.com`",`n	`"password`":`"Password123`"`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_in' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "data": {
        "id": 58463,
        "slug": "poVcXdGc35qERs1ngPTXgsZ1",
        "first_name": "firstName",
        "last_name": "lastName",
        "email": "apidoc+broker@wellthie.com",
        "provider": "email",
        "uid": "apidoc+broker@wellthie.com",
        "password_changed_at": "2020-03-05T07:38:17.526-05:00",
        "organization_id": 23,
        "team_id": null,
        "role": "broker",
        "user_type": null,
        "broker_code": "123456",
        "phone_number": null,
        "account_expiration_date": null,
        "created_by_user_id": null,
        "time_zone": "Eastern Time (US & Canada)",
        "deleted_at": null,
        "company_id": null,
        "allow_password_change": false,
        "is_any_broker_type": true,
        "access_token": "eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ2MywiY2xpZW50Ijoiem82VnJxYTRhZ0ZQVkhITS1jTnA0USIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiMGY4ZTg5YmFkOGY4YjMzZjFlNjc0MjVlMjE3NzVjYmQiLCJleHAiOjE1ODQ0Mjg4MDF9.XJP8sJVUX2mxwQ_MkryQbB8AUPcuQMvr65Dxrsvp7PA"
    }
}
```

This endpoint allows you to get a session token.

### HTTP Request

`POST /api/auth/sign_in`

### Parameters

Parameter                                                         | Default   | Description
----------------------------------------------------------------- | --------- | -------------------
<strong>email</strong><strong>required</strong>                   | N/A       | Email Address
<strong>password</strong><strong>required</strong>               | N/A       | First Name

## Sign out

```shell
curl --location --request DELETE 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_out' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22zEqWCx7JuXrpJKE5g1etDw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22kDskePSCU9pGO1asU5dbGA%22%2C%22expiry%22%3A%221584033471%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: zEqWCx7JuXrpJKE5g1etDw' \
--header 'client: kDskePSCU9pGO1asU5dbGA' \
--header 'expiry: 1584033471' \
--header 'uid: apidoc+broker@wellthie.com'
```

```go
package main

import (
  "fmt"
  "net/http"
  "io/ioutil"
)

func main() {

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_out"
  method := "DELETE"

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, nil)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22zEqWCx7JuXrpJKE5g1etDw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22kDskePSCU9pGO1asU5dbGA%22%2C%22expiry%22%3A%221584033471%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "zEqWCx7JuXrpJKE5g1etDw")
  req.Header.Add("client", "kDskePSCU9pGO1asU5dbGA")
  req.Header.Add("expiry", "1584033471")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_out",
  "method": "DELETE",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22zEqWCx7JuXrpJKE5g1etDw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22kDskePSCU9pGO1asU5dbGA%22%2C%22expiry%22%3A%221584033471%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "zEqWCx7JuXrpJKE5g1etDw",
    "client": "kDskePSCU9pGO1asU5dbGA",
    "expiry": "1584033471",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_out"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22zEqWCx7JuXrpJKE5g1etDw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22kDskePSCU9pGO1asU5dbGA%22%2C%22expiry%22%3A%221584033471%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"zEqWCx7JuXrpJKE5g1etDw",
  @"client": @"kDskePSCU9pGO1asU5dbGA",
  @"expiry": @"1584033471",
  @"uid": @"apidoc+broker@wellthie.com"
};

[request setAllHTTPHeaderFields:headers];

[request setHTTPMethod:@"DELETE"];

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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22zEqWCx7JuXrpJKE5g1etDw%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22kDskePSCU9pGO1asU5dbGA%22%2C%22expiry%22%3A%221584033471%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "zEqWCx7JuXrpJKE5g1etDw")
$headers.Add("client", "kDskePSCU9pGO1asU5dbGA")
$headers.Add("expiry", "1584033471")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/auth/sign_out' -Method 'DELETE' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
  "success": true
}
```

Use this endpoint to finish the session and discard the access-token acquired on the sign in API call

### HTTP Request

`POST /api/auth/sign_out`

### Parameters

This API doesnot require any parameter.
