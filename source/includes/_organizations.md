# Organizations

An Organization is a group like yours that will be consuming the Wellthie BIZ API to build something.

## Get Settings

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/organization/settings' \
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
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE")

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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/organization/settings"]
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

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/organization/settings' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "logo": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/organizations/logos/000/000/023/main/logo-4-color.png?1474486469",
    "splash_image": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/organizations/splash_photos/000/000/023/homepage/1600x800-banner-01-nr3.png?1505424554",
    "show_broker_code": true,
    "effective_dates": [
        {
            "label": "April 1, 2020",
            "data": "2020-04-01",
            "states": []
        },
        {
            "label": "May 1, 2020",
            "data": "2020-05-01",
            "states": []
        },
        {
            "label": "June 1, 2020",
            "data": "2020-06-01",
            "states": []
        }
    ],
    "show_schedule_a_call": true,
    "schedule_a_call_availabilities": [
        {
            "day": "Monday, March  9",
            "data": "2020-03-09",
            "hours": [
                {
                    "label": "9:00AM - 10:00AM"
                },
                {
                    "label": "10:00AM - 11:00AM"
                },
                {
                    "label": "11:00AM - 12:00AM"
                },
                {
                    "label": "12:00AM - 1:00PM"
                },
                {
                    "label": "1:00PM - 2:00PM"
                },
                {
                    "label": "2:00PM - 3:00PM"
                },
                {
                    "label": "3:00PM - 4:00PM"
                },
                {
                    "label": "4:00PM - 5:00PM"
                }
            ]
        },
        {
            "day": "Tuesday, March 10",
            "data": "2020-03-10",
            "hours": [
                {
                    "label": "9:00AM - 10:00AM"
                },
                {
                    "label": "10:00AM - 11:00AM"
                },
                {
                    "label": "11:00AM - 12:00AM"
                },
                {
                    "label": "12:00AM - 1:00PM"
                },
                {
                    "label": "1:00PM - 2:00PM"
                },
                {
                    "label": "2:00PM - 3:00PM"
                },
                {
                    "label": "3:00PM - 4:00PM"
                },
                {
                    "label": "4:00PM - 5:00PM"
                }
            ]
        },
        {
            "day": "Wednesday, March 11",
            "data": "2020-03-11",
            "hours": [
                {
                    "label": "9:00AM - 10:00AM"
                },
                {
                    "label": "10:00AM - 11:00AM"
                },
                {
                    "label": "11:00AM - 12:00AM"
                },
                {
                    "label": "12:00AM - 1:00PM"
                },
                {
                    "label": "1:00PM - 2:00PM"
                },
                {
                    "label": "2:00PM - 3:00PM"
                },
                {
                    "label": "3:00PM - 4:00PM"
                },
                {
                    "label": "4:00PM - 5:00PM"
                }
            ]
        }
    ],
    "show_issuer_logos": false,
    "excel_template_file": true,
    "excel_template_url": "URL",
    "allow_group_and_group_to_individual": true,
    "allow_only_group": false,
    "allow_only_group_to_individual": false,
    "show_enrollment_buttons_on_quote_page": true,
    "business_large_group_url": "URL",
    "business_individual_url": "https://www.healthcare.gov/",
    "census_child_max_age_for_inclusion_in_household": 26,
    "show_renewals": false,
    "use_sso": true,
    "sso_idp_target_url": "https://wellthieinc-dev.onelogin.com",
    "sso_idp_login_link_text": "Login through Wellthie's OneLogin",
    "disable_direct_login": false,
    "organization_name": "Wellthie Demo",
    "show_dental": true,
    "show_vision": true,
    "show_value_add": false,
    "show_dental_and_vision_bundle": false,
    "show_value_add_bundle": false,
    "show_limited_medical": false,
    "filters_configuration": {
        "medical_filters": [
            {
                "label": "Issuer",
                "value": "issuer",
                "type": "issuer",
                "icon": "icon--issuers",
                "show_for_single": true,
                "show_for_family": true
            },
            {
                "label": "Exchange Type",
                "value": "exchange_type",
                "icon": "icon--exchange-type",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "selected_tags": [
                    "off_exchange"
                ],
                "tags": [
                    {
                        "value": "on_exchange",
                        "label": "On Exchange"
                    },
                    {
                        "value": "off_exchange",
                        "label": "Off Exchange"
                    }
                ]
            },
            {
                "label": "Savings Account",
                "value": "hsa_eligible",
                "icon": "icon--hsa",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "hsa_eligible",
                        "label": "HSA Eligible"
                    }
                ]
            },
            {
                "label": "Deductible",
                "value": "deductible",
                "icon": "icon--deductible-single",
                "type": "range",
                "plan_property": "deductible_single_number",
                "show_for_single": true,
                "show_for_family": true,
                "ranges": [
                    {
                        "label": "$0 to $2,000",
                        "value": "under_2000",
                        "start_range": 0,
                        "end_range": 2000
                    },
                    {
                        "label": "$2,001 to $4,000",
                        "value": "2001_to_4001",
                        "start_range": 2001,
                        "end_range": 4000
                    },
                    {
                        "label": "$4,001 to $6,000",
                        "value": "4001_to_6000",
                        "start_range": 4001,
                        "end_range": 6000
                    },
                    {
                        "label": "$6,001 to $8,000",
                        "value": "6001_to_8000",
                        "start_range": 6001,
                        "end_range": 8000
                    },
                    {
                        "label": "> $8,000",
                        "value": "8001_to_100000",
                        "start_range": 8001,
                        "end_range": 100000
                    }
                ]
            },
            {
                "label": "Metal",
                "value": "metal",
                "icon": "icon--metal",
                "type": "tag",
                "show_for_single": true,
                "show_for_family": true,
                "tags": [
                    {
                        "value": "bronze",
                        "label": "Bronze"
                    },
                    {
                        "value": "silver",
                        "label": "Silver"
                    },
                    {
                        "value": "gold",
                        "label": "Gold"
                    },
                    {
                        "value": "platinum",
                        "label": "Platinum"
                    }
                ]
            },
            {
                "label": "Maximum Out Of Pocket",
                "value": "maximum_out_of_pocket",
                "icon": "icon--moop-single",
                "type": "range",
                "plan_property": "moop_single_number",
                "show_for_single": true,
                "show_for_family": true,
                "ranges": [
                    {
                        "label": "$0 to $2,000",
                        "value": "under_2000",
                        "start_range": 0,
                        "end_range": 2000
                    },
                    ...
                ]
            },
            {
                "label": "Network",
                "value": "network",
                "icon": "icon--network",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "epo",
                        "label": "EPO"
                    },
                    ...
                ]
            },
            {
                "label": "PCP Cost Sharing Amount",
                "value": "pcp_amount",
                "icon": "icon--copay",
                "type": "range",
                "show_for_single": true,
                "show_for_family": true,
                "ranges": [
                    {
                        "label": "< $30 before deductible",
                        "value": "amount_low_range_before",
                        "start_range": 0,
                        "end_range": 30,
                        "plan_property": "pcp_amount_number_before_deductible"
                    },
                    ...
                ]
            },
            {
                "label": "PCP Cost Sharing Percentage",
                "value": "pcp_percentage",
                "icon": "icon--discount",
                "type": "range",
                "show_for_single": true,
                "show_for_family": true,
                "ranges": [
                    {
                        "label": "< 30% before deductible",
                        "value": "percentage_low_range_before",
                        "start_range": 0,
                        "end_range": 30,
                        "plan_property": "pcp_percentage_number_before_deductible"
                    },
                    ...
                ]
            }
        ],
        "dental_filters": [
            {
                "label": "Issuer",
                "value": "issuer",
                "type": "issuer",
                "icon": "icon--issuers",
                "show_for_single": true,
                "show_for_family": true
            },
            {
                "label": "Network",
                "value": "network",
                "icon": "icon--network",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "dental_hmo",
                        "label": "HMO"
                    },
                    ...
                ]
            },
            {
                "label": "Includes",
                "value": "includes",
                "icon": "icon--add-on",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "dental_orthodontia_over_19",
                        "label": "Orthodontia Over Age 19"
                    },
                    {
                        "value": "dental_orthodontia_under_19",
                        "label": "Orthodontia Under Age 19"
                    },
                    {
                        "value": "dental_discount_plan",
                        "label": "Discount Plan"
                    }
                ]
            }
        ],
        "vision_filters": [
            {
                "label": "Issuer",
                "value": "issuer",
                "type": "issuer",
                "icon": "icon--issuers",
                "show_for_single": true,
                "show_for_family": true
            },
            {
                "label": "Network",
                "value": "network",
                "icon": "icon--network",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "vision_hmo",
                        "label": "HMO"
                    },
                    ...
                ]
            },
            {
                "label": "Includes",
                "value": "includes",
                "icon": "icon--add-on",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "vision_lens_options",
                        "label": "Lens Options"
                    },
                    {
                        "value": "vision_contacts",
                        "label": "Contacts Options"
                    }
                ]
            }
        ],
        "dental_vision_bundle_filters": [
            {
                "label": "Issuer",
                "value": "issuer",
                "type": "issuer",
                "icon": "icon--issuers",
                "show_for_single": true,
                "show_for_family": true
            },
            {
                "label": "Network",
                "value": "network",
                "icon": "icon--network",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "dental_and_vision_bundle_hmo",
                        "label": "HMO"
                    },
                    {
                        "value": "dental_and_vision_bundle_pos",
                        "label": "POS"
                    },
                    {
                        "value": "dental_and_vision_bundle_ppo",
                        "label": "PPO"
                    }
                ]
            },
            {
                "label": "Dental Benefits Includes",
                "value": "dental_benefits_includes",
                "icon": "icon--add-on",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "orthodontia_over_19",
                        "label": "Orthodontia Over Age 19"
                    },
                    {
                        "value": "orthodontia_under_19",
                        "label": "Orthodontia Under Age 19"
                    }
                ]
            },
            {
                "label": "Vision Benefits Includes",
                "value": "vision_benefits_includes",
                "icon": "icon--add-on",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "vision_lens_options",
                        "label": "Lens Options"
                    },
                    {
                        "value": "vision_contacts",
                        "label": "Contacts Options"
                    }
                ]
            }
        ],
        "value_add_filters": [
            {
                "label": "Issuer",
                "value": "issuer",
                "type": "issuer",
                "icon": "icon--issuers",
                "show_for_single": true,
                "show_for_family": true
            },
            {
                "value": "type",
                "label": "Type",
                "icon": "icon--includes",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "label": "Accident UPDATED",
                        "value": "accident"
                    },
                    {
                        "label": "Accidental Death & Dismemberment",
                        "value": "ad_and_d"
                    }
                ]
            }
        ],
        "value_add_bundle_filters": [
            {
                "label": "Issuer",
                "value": "issuer",
                "type": "issuer",
                "icon": "icon--issuers",
                "show_for_single": true,
                "show_for_family": true
            }
        ],
        "limited_medical_filters": [
            {
                "label": "Issuer",
                "value": "issuer",
                "type": "issuer",
                "icon": "icon--issuers",
                "show_for_single": true,
                "show_for_family": true
            },
            {
                "label": "Includes",
                "value": "includes",
                "icon": "icon--add-on",
                "show_for_single": true,
                "show_for_family": true,
                "type": "tag",
                "tags": [
                    {
                        "value": "limited_medical_accident",
                        "label": "Accident"
                    },
                    {
                        "value": "limited_medical_anesthesia",
                        "label": "Anesthesia"
                    },
                    {
                        "value": "limited_medical_critical_care",
                        "label": "Critical Care"
                    }
                ]
            }
        ]
    },
    "show_composite_rates": true,
    "allow_broker_registration": true,
    "events_api_url": null,
    "mixpanel_project_id": "ea174d0291bcc41acc0bf30285568917",
    "name": "Wellthie Demo"
}
```

Use this endpoint to retrieve the settings like available / enabled effective dates, times to schedule calls, whether or not to show ancillary plans like dental, vision, etc.

<aside class="notice">
  This endpoint does not require a session or authorization token.
</aside>

### HTTP Request

`GET /api/organization/settings`

### Parameters

No parameters required.
