# Enrollments

## POST Contact

```shell
curl --location --request POST 'http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/inquiries/SMIQ4519/enrollments/contact' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22undefined%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22undefined%22%2C%22expiry%22%3A%22undefined%22%2C%22uid%22%3A%22undefined%22%7D' \
--header 'access-token: ' \
--header 'client: ' \
--header 'expiry: ' \
--header 'uid: ' \
--data-raw '{
    "enrollment_contact_form": {
        "name": "Contact Person Name",
        "email": "contact@email.com",
        "phone": "2020202020",
        "comments": "Example Comment"
    },
    "inquiry_slug": "SMIQ4519",
    "enrollment": {}
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

  url := "http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/inquiries/SMIQ4519/enrollments/contact"
  method := "POST"

  payload := strings.NewReader("{\n    \"enrollment_contact_form\": {\n        \"name\": \"Contact Person Name\",\n        \"email\": \"contact@email.com\",\n        \"phone\": \"2020202020\",\n        \"comments\": \"Example Comment\"\n    },\n    \"inquiry_slug\": \"SMIQ4519\",\n    \"enrollment\": {}\n}")

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
  "url": "http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/inquiries/SMIQ4519/enrollments/contact",
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
  "data": JSON.stringify({"enrollment_contact_form":{"name":"Contact Person Name","email":"contact@email.com","phone":"2020202020","comments":"Example Comment"},"inquiry_slug":"SMIQ4519","enrollment":{}}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/inquiries/SMIQ4519/enrollments/contact"]
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
NSData *postData = [[NSData alloc] initWithData:[@"{\n    \"enrollment_contact_form\": {\n        \"name\": \"Contact Person Name\",\n        \"email\": \"contact@email.com\",\n        \"phone\": \"2020202020\",\n        \"comments\": \"Example Comment\"\n    },\n    \"inquiry_slug\": \"SMIQ4519\",\n    \"enrollment\": {}\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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

$body = "{`n    `"enrollment_contact_form`": {`n        `"name`": `"Contact Person Name`",`n        `"email`": `"contact@email.com`",`n        `"phone`": `"2020202020`",`n        `"comments`": `"Example Comment`"`n    },`n    `"inquiry_slug`": `"SMIQ4519`",`n    `"enrollment`": {}`n}"

$response = Invoke-RestMethod 'http://wellthiedemo-smallbusiness-qa.lvh.me:3030/api/inquiries/SMIQ4519/enrollments/contact' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "id": 5200,
    "company_id": 107639,
    "encrypted_name": "LoTG8E7hHBA4N3u8AeyjQJuGfviKlzqb78ws8AVEhFo=\n",
    "encrypted_phone": "tXoUVsMdfiSqpTxbzORi+w==\n",
    "encrypted_email": "6J0iyCDmVvgoDLy58JcOotT3pRjtMvw2QY3ptL6uP3g=\n",
    "date_to_call": null,
    "preferred_time": null,
    "comments": "Example Comment",
    "created_at": "2020-03-11T08:14:10.744-04:00",
    "updated_at": "2020-03-11T08:16:31.378-04:00"
}
```

Use this endpoint to create a new Enrollment Contact.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`POST /api/inquiries/:inquiry_slug/enrollments/contact`

### Parameters

Parameter                                         | Default   | Description
------------------------------------------------- | --------- | -------------------
<strong>name</strong><strong>required</strong>    | N/A       | Name of the contact
<strong>email</strong><strong>required</strong>   | N/A       | Email of the contact
<strong>phone</strong><strong>required</strong>   | N/A       | Phone number
comments                                          | N/A       | Any comments

> Here's an example response:

```json
{
    "id": 113569,
    "estimate_tax_credit_eligibility_trash": null,
    "show_group_to_individual_selected_trash": null,
    "created_at": "2020-03-11T08:12:56.354-04:00",
    "updated_at": "2020-03-11T08:12:56.354-04:00",
    "inquiry_id": 130139
}
```

## POST Employees Contact

Use this endpoint to update contact details of the Employees.
[Use Census Create logic](#create-census)
<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>.
</aside>

## PUT Employees Contact
Use this endpoint to update contact details of the Employees.


<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>.
  <a href="#create-census">Use Census Create logic</a>
</aside>

Use this endpoint to create a new census.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`PUT /api/inquiries/:inquiry_slug/enrollments/employees_contact`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
census       | N/A     | Census object         | true
