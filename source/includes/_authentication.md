# Authentication

## Register

```shell
curl --location --request POST 'http://emblemhealth-qa.lvh.me:3030/api/auth' \
--header 'Content-Type: application/json' \
--data-raw '{
  "email": "apiuser@domain.com",
  "first_name": "FirstName",
  "last_name": "LastName",
  "password": "StrongSecurePassword123",
  "password_confirmation": "StrongSecurePassword123"
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

  url := "http://emblemhealth-qa.lvh.me:3030/api/auth"
  method := "POST"

  payload := strings.NewReader("{\n  \"email\": \"apiuser@domain.com\",\n  \"first_name\": \"FirstName\",\n  \"last_name\": \"LastName\",\n  \"password\": \"StrongSecurePassword123\",\n  \"password_confirmation\": \"StrongSecurePassword123\"\n}")

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
  "url": "http://emblemhealth-qa.lvh.me:3030/api/auth",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json"
  },
  "data": JSON.stringify({"email":"apiuser@domain.com","first_name":"FirstName","last_name":"LastName","password":"StrongSecurePassword123","password_confirmation":"StrongSecurePassword123"}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://emblemhealth-qa.lvh.me:3030/api/auth"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n  \"email\": \"apiuser@domain.com\",\n  \"first_name\": \"FirstName\",\n  \"last_name\": \"LastName\",\n  \"password\": \"StrongSecurePassword123\",\n  \"password_confirmation\": \"StrongSecurePassword123\"\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

$body = "{`n  `"email`": `"apiuser@domain.com`",`n  `"first_name`": `"FirstName`",`n  `"last_name`": `"LastName`",`n  `"password`": `"StrongSecurePassword123`",`n  `"password_confirmation`": `"StrongSecurePassword123`"`n}"

$response = Invoke-RestMethod 'http://emblemhealth-qa.lvh.me:3030/api/auth' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "data": {
        "id": 23618,
        "slug": "pjFyqbd9d4nzpU3Gr6bkyPVB",
        "first_name": "FirstName",
        "last_name": "LastName",
        "email": "apiuser@domain.com",
        "provider": "email",
        "uid": "apiuser@domain.com",
        "password_changed_at": "2020-03-12T05:25:52.197-04:00",
        "organization_id": 35,
        "team_id": null,
        "role": "individual",
        "user_type": null,
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
        "allow_password_change": false,
        "is_any_broker_type": false,
        "latest_quote_id": null,
        "access_token": "eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxOCwiZXhwIjoxNTg0MDkxNTUyfQ.rwE4pMUTTNtWYda664xEewtHDygLV3Wnljj9p0z9W5w"
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
curl --location --request POST 'https://wellthie-qa.affordablecareadvisor.net/api/auth/sign_in' \
--header 'Content-Type: application/json' \
--data-raw '{
	"email":"api_user@domain.com",
	"password":"SecureSecurePassword123"
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

  url := "https://wellthie-qa.affordablecareadvisor.net/api/auth/sign_in"
  method := "POST"

  payload := strings.NewReader("{\n	\"email\":\"api_user@domain.com\",\n	\"password\":\"SecurePassword123\"\n}")

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
  "url": "https://wellthie-qa.affordablecareadvisor.net/api/auth/sign_in",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json"
  },
  "data": JSON.stringify({"email":"api_user@domain.com","password":"SecurePassword123"}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```powershell
$headers = New-Object "System.Collections.Generic.Dictionary[[String],[String]]"
$headers.Add("Content-Type", "application/json")

$body = "{`n	`"email`":`"api_user@domain.com`",`n	`"password`":`"SecurePassword123`"`n}"

$response = Invoke-RestMethod 'https://wellthie-qa.affordablecareadvisor.net/api/auth/sign_in' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthie-qa.affordablecareadvisor.net/api/auth/sign_in"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n	\"email\":\"api_user@domain.com\",\n	\"password\":\"SecurePassword123\"\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

> Response looks like this:

```json
{
  "data": {
    "id": "id",
    "slug": "slug",
    "first_name": "Name",
    "last_name": "Lastname",
    "email": "name.lastname@domain.com",
    "provider": "email",
    "uid": "name.lastname@domain.com",
    "password_changed_at": "2017-05-04T12:57:21.000-04:00",
    "organization_id": 1,
    "team_id": null,
    "role": "organization_admin",
    "user_type": null,
    "npn": "A1B2",
    "broker_code": "A1B2",
    "phone_number": "",
    "account_expiration_date": null,
    "created_by_user_id": 2,
    "time_zone": "Eastern Time (US & Canada)",
    "deleted_at": null,
    "is_any_broker_type": true
  }
}
```

This endpoint allows you to get a session token.

### HTTP Request

`POST /api/auth/sign_in`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
email        | N/A     | User's email address  | true
password     | N/A     | User's password       | true

## Sign out

```shell
curl --location --request DELETE 'http://emblemhealth-qa.lvh.me:3030/api/auth/sign_out' \
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

  url := "http://emblemhealth-qa.lvh.me:3030/api/auth/sign_out"
  method := "DELETE"

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
  "url": "http://emblemhealth-qa.lvh.me:3030/api/auth/sign_out",
  "method": "DELETE",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://emblemhealth-qa.lvh.me:3030/api/auth/sign_out"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"" dataUsingEncoding:NSUTF8StringEncoding]];
[request setHTTPBody:postData];

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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoyMzYxNCwiZXhwIjoxNTg0MDk5NTgwfQ.wANmfcqNQLgnhJv0tQLjw6CKhTSBVApOalWsOWXFNCs")

$body = ""

$response = Invoke-RestMethod 'http://emblemhealth-qa.lvh.me:3030/api/auth/sign_out' -Method 'DELETE' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
  "success": true
}
```

Use this endpoint to finish the session and discard the access_token acquired on the sign in API call

### HTTP Request

`POST /api/auth/sign_out`

### Parameters

This API doesnot require any parameter.