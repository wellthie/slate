# Organizations

## Settings

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/organization/settings' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/organization/settings"
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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/organization/settings",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/organization/settings"]
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

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/organization/settings' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
  "logo": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/organizations/logos/000/000/023/main/logo-4-color.png?1474486469",
  "splash_image": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/organizations/splash_photos/000/000/023/homepage/1600x800-Banner-01.png?1461855472",
  "show_broker_code": true,
  "effective_dates": [
    {
      "label": "June 1, 2017",
      "data": "2017-06-01"
    }
  ],
  "show_schedule_a_call": true,
  "schedule_a_call_availabilities": [
    {
      "day": "Monday, May 15",
      "data": "2017-05-15",
      "hours": [
        {
          "label": "9:00AM - 10:00AM"
        }
      ]
    },
    {
      "day": "Tuesday, May 16",
      "data": "2017-05-16",
      "hours": [
        {
          "label": "9:00AM - 10:00AM"
        }
      ]
    },
    {
      "day": "Wednesday, May 17",
      "data": "2017-05-17",
      "hours": [
        {
          "label": "9:00AM - 10:00AM"
        },
        {
          "label": "10:00AM - 11:00AM"
        }
      ]
    }
  ],
  "show_issuer_logos": false,
  "broker_code_regex": "^[a-zA-Z0-9]{4,10}$",
  "broker_code_message": "4-10 Alphanumeric Codes",
  "excel_template_file": true,
  "excel_template_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/organizations/excel_templates/000/000/023/original/downloadable_census-rc37-oc36.xlsx?1478203799",
  "show_group_to_individual": true,
  "hide_enrollment_buttons_on_quote_page": false,
  "business_large_group_url": "https://www.amerihealthnj.com/html/employers/large_businesses.html?",
  "business_individual_url": "https://www.healthcare.gov/",
  "census_child_max_age_for_inclusion_in_household": 26,
  "show_renewals": true,
  "use_sso": true,
  "sso_idp_target_url": "https://wellthieinc-dev.onelogin.com",
  "sso_idp_login_link_text": "Login through Wellthie's OneLogin",
  "disable_direct_login": false,
  "organization_name": "Wellthie Demo",
  "show_dental": true,
  "show_vision": true,
  "show_value_add": true
}
```

Use this endpoint to retrieve the particular 

<aside class="notice">
  This endpoint does not require any session or authorization token.
</aside>

### HTTP Request

`GET /api/organization/settings`

### Parameters

No parameters required.
