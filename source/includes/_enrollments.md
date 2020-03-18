# Enrollments

Enrollment APIs are used to store information about contact details for the Inquiry

## Create Enrollment Contact

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/enrollments/contact' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/enrollments/contact"
  method := "POST"

  payload := strings.NewReader("{\n    \"enrollment_contact_form\": {\n        \"name\": \"Contact Person Name\",\n        \"email\": \"contact@email.com\",\n        \"phone\": \"2020202020\",\n        \"comments\": \"Example Comment\"\n    },\n    \"inquiry_slug\": \"SMIQ4519\",\n    \"enrollment\": {}\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/enrollments/contact",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/enrollments/contact"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

$body = "{`n    `"enrollment_contact_form`": {`n        `"name`": `"Contact Person Name`",`n        `"email`": `"contact@email.com`",`n        `"phone`": `"2020202020`",`n        `"comments`": `"Example Comment`"`n    },`n    `"inquiry_slug`": `"SMIQ4519`",`n    `"enrollment`": {}`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/enrollments/contact' -Method 'POST' -Headers $headers -Body $body
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
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

## Create Employee Contact

<aside class="success">
  <a href="#create-census">Use Census Create logic</a>
</aside>

## Update Employee Contact

<aside class="success">
  <a href="#create-census">Use Census Create logic</a>
</aside>
