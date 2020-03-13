# Plans

## Get Available Group Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: rVTzBq3e3ZbyWoOXjpLuXQ' \
--header 'client: ukIdapo9RQvkaMkt-HeMUg' \
--header 'expiry: 1583919204' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "rVTzBq3e3ZbyWoOXjpLuXQ")
  req.Header.Add("client", "ukIdapo9RQvkaMkt-HeMUg")
  req.Header.Add("expiry", "1583919204")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "rVTzBq3e3ZbyWoOXjpLuXQ",
    "client": "ukIdapo9RQvkaMkt-HeMUg",
    "expiry": "1583919204",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"rVTzBq3e3ZbyWoOXjpLuXQ",
  @"client": @"ukIdapo9RQvkaMkt-HeMUg",
  @"expiry": @"1583919204",
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "rVTzBq3e3ZbyWoOXjpLuXQ")
$headers.Add("client", "ukIdapo9RQvkaMkt-HeMUg")
$headers.Add("expiry", "1583919204")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
    {
        "promotional_label": null,
        "issuer_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/173/main/oscar_logo_blue_2020-wg39.png?1573759981",
        "id": 78699,
        "name": "Oscar Circle Plus Bronze $8150 (Dep 29, No DP)",
        "service_area_id": 4334,
        "highlight_1": {
            "icon": "icon--metal",
            "value": "Bronze"
        },
        "highlight_2": {
            "icon": "icon--network",
            "value": "EPO"
        },
        "highlight_3": {
            "icon": "icon--add-on",
            "value": "PCP $0"
        },
        "highlight_4": null,
        "highlight_5": null,
        "highlight_6": null,
        "available_exchanges": {
            "icon": "icon--exchange-type",
            "value": "Available Off Exchange"
        },
        "sbc_download_url": null,
        "network_url": "https://www.hioscar.com/search/",
        "formulary_url": "https://www.hioscar.com/search/",
        "hios_plan_identifier": "74289NY2790019",
        "plan_year": 2020,
        "tags": [
            "bronze",
            "epo",
            "off_exchange"
        ],
        "group_or_individual_plan_type": "Group",
        "metal_level_name": "Bronze",
        "on_exchange": false,
        "off_exchange": true,
        "plan_description": null,
        "plan_detail_header": null,
        "plan_detail_items": null,
        "plan_detail_footer": null,
        "composite_rating": false,
        "hsa_eligible": false,
        "issuer": {
            "id": 173,
            "name": "Oscar",
            "parameterized_name": "oscar",
            "composite_ee_factor": null,
            "composite_es_factor": null,
            "composite_ec_factor": null,
            "composite_ef_factor": null,
            "enrollment_content_area_name": "Enrollment Instructions: Oscar Plans",
            "main_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/173/main/oscar_logo_blue_2020-wg39.png?1573759981",
            "issuer_enrollment_resources": [
                {
                    "name": "Oscar Business Broker Login",
                    "product_type": "Medical",
                    "resource_type": "link",
                    "display_link_url": "https://business.hioscar.com/login",
                    "sort_order": 10
                },
                {
                    "name": "Oscar Auto-Renewal Business Enrollment Form",
                    "product_type": "Medical",
                    "resource_type": "file",
                    "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/805/original/o4b_-_ny_2017_2018_business_enrollment_form__auto-renewal__v04-ao6.pdf?1509036239",
                    "sort_order": 30
                },
                {
                    "name": "Oscar Business Enrollment Form",
                    "product_type": "Medical",
                    "resource_type": "file",
                    "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/806/original/o4b_businessenrollmentform_ny_2017-db81.pdf?1509036301",
                    "sort_order": 20
                },
                {
                    "name": "Oscar Employee Enrollment Form",
                    "product_type": "Medical",
                    "resource_type": "file",
                    "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/803/original/oscar-xa19.pdf?1509036019",
                    "sort_order": 40
                },
                {
                    "name": "Oscar Auto-Renewal Employee Enrollment Form",
                    "product_type": "Medical",
                    "resource_type": "file",
                    "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/804/original/oscar%20employee%20auto-renewal%20form-hy63.pdf?1509036116",
                    "sort_order": 50
                },
                {
                    "name": "Oscar for Business Underwriting Guidelines",
                    "product_type": "Medical",
                    "resource_type": "file",
                    "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuer_enrollment_resources/attachments/000/000/934/original/sgunderwriting03-2017_v9-hd83.pdf?1512419195",
                    "sort_order": 60
                }
            ]
        },
        "medical_plan_benefit": {
            "medical_plan_id": 78699,
            "medical_deductible_single": "$8,150",
            "medical_deductible_family": "$16,300",
            "maximum_out_of_pocket_limit_single": "$8,150",
            "maximum_out_of_pocket_limit_family": "$16,300",
            "pcp": "$0",
            "specialist": "$0",
            "preventive_care": "$0",
            "inpatient_facility": "$0",
            "outpatient_facility": "$0",
            "outpatient_physician_surgeon": "$0",
            "imaging": "$0",
            "durable_medical_equipment": "$0",
            "diagnostic": "$0",
            "emergency_room": "$0",
            "urgent_care": "$0",
            "ambulance": "$0",
            "rx_deductible": null,
            "generic": "$0",
            "formulary_brand": "$0",
            "non_formulary_brand": "$0",
            "mail_order": "2.5x",
            "adult_vision_exam": null,
            "adult_preventive_dental": null,
            "adult_major_dental": null,
            "adult_eyewear": null,
            "adult_emergency_dental": null,
            "eyewear": null,
            "pediatric_vision_exam": null,
            "pediatric_preventive_dental": null,
            "pediatric_orthodontics": null,
            "pediatric_major_dental": null,
            "pediatric_eyewear": null,
            "pediatric_emergency_dental": null,
            "pcp_telemedicine": null,
            "nutritionist_telemedicine": null,
            "deductible_single_number": 8150,
            "deductible_family_number": 16300,
            "moop_single_number": 8150,
            "moop_family_number": 16300,
            "benefit_rows_with_header": {
                "Main Benefits": {
                    "Deductible - Single": "medical_deductible_single",
                    "Deductible - Family": "medical_deductible_family",
                    "Out of Pocket Max - Single": "maximum_out_of_pocket_limit_single",
                    "Out of Pocket Max - Family": "maximum_out_of_pocket_limit_family"
                },
                "Outpatient & Inpatient Services": {
                    "Primary Care Visit": "pcp",
                    "Specialist Visit": "specialist",
                    "Preventive Care": "preventive_care",
                    "Inpatient Facility": "inpatient_facility",
                    "Outpatient Facility": "outpatient_facility",
                    "Outpatient Surgery": "outpatient_physician_surgeon"
                },
                "Medical Equipment & Tests": {
                    "Imaging": "imaging",
                    "Durable Medical Equipment": "durable_medical_equipment",
                    "Diagnostic": "diagnostic"
                },
                "Emergency Services": {
                    "Emergency Room Visit": "emergency_room",
                    "Urgent Care": "urgent_care",
                    "Ambulance": "ambulance"
                },
                "Prescription Drug Coverage": {
                    "RX Code": "rx_code",
                    "Prescription Drug Deductible": "rx_deductible",
                    "Generic Brand Prescriptions": "generic",
                    "Formulary Brand Prescriptions": "formulary_brand",
                    "Non-Formulary Brand Prescriptions": "non_formulary_brand",
                    "Mail Order": "mail_order"
                },
                "Add-on Dental and Vision": {
                    "Adult Vision Exam": "adult_vision_exam",
                    "Adult Preventive Dental": "adult_preventive_dental",
                    "Adult Major Dental": "adult_major_dental",
                    "Adult Eyewear": "adult_eyewear",
                    "Adult Emergency Dental": "adult_emergency_dental",
                    "Eyewear": "eyewear",
                    "Pediatric Vision Exam": "pediatric_vision_exam",
                    "Pediatric Preventive Dental": "pediatric_preventive_dental",
                    "Pediatric Orthodontics": "pediatric_orthodontics",
                    "Pediatric Major Dental": "pediatric_major_dental",
                    "Pediatric Eyewear": "pediatric_eyewear",
                    "Pediatric Emergency Dental": "pediatric_emergency_dental",
                    "PCP Telemedicine": "pcp_telemedicine",
                    "Nutritionist Telemedicine": "nutritionist_telemedicine"
                }
            },
            "view_detail_benefits": [
                "pcp",
                "imaging",
                "formulary_brand",
                "specialist",
                "generic",
                "non_formulary_brand"
            ],
            "out_of_network_benfit_row_header": {
                "Main Benefits": {
                    "Deductible - Single": "medical_deductible_single_out_network",
                    "Deductible - Family": "medical_deductible_family_out_network",
                    "Out of Pocket Max - Single": "maximum_out_of_pocket_limit_single_out_network",
                    "Out of Pocket Max - Family": "maximum_out_of_pocket_limit_family_out_network"
                },
                "Outpatient & Inpatient Services": {
                    "Primary Care Visit": "pcp_out_network",
                    "Specialist Visit": "specialist_out_network",
                    "Preventive Care": "preventive_care_out_network",
                    "Inpatient Facility": "inpatient_facility_out_network",
                    "Outpatient Facility": "outpatient_facility_out_network",
                    "Outpatient Surgery": "outpatient_physician_surgeon_out_network"
                },
                "Medical Equipment & Tests": {
                    "Imaging": "imaging_out_network",
                    "Durable Medical Equipment": "durable_medical_equipment_out_network",
                    "Diagnostic": "diagnostic_out_network"
                },
                "Emergency Services": {
                    "Emergency Room Visit": "emergency_room_out_network",
                    "Urgent Care": "urgent_care_out_network",
                    "Ambulance": "ambulance_out_network"
                },
                "Prescription Drug Coverage": {
                    "RX Code": "rx_code",
                    "Prescription Drug Deductible": "rx_deductible_out_network",
                    "Generic Brand Prescriptions": "generic_out_network",
                    "Formulary Brand Prescriptions": "formulary_brand_out_network",
                    "Non-Formulary Brand Prescriptions": "non_formulary_brand_out_network",
                    "Mail Order": "mail_order_out_network"
                },
                "Add-on Dental and Vision": {
                    "Adult Vision Exam": "adult_vision_exam_out_network",
                    "Adult Preventive Dental": "adult_preventive_dental_out_network",
                    "Adult Major Dental": "adult_major_dental_out_network",
                    "Adult Eyewear": "adult_eyewear_out_network",
                    "Adult Emergency Dental": "adult_emergency_dental_out_network",
                    "Eyewear": "",
                    "Pediatric Vision Exam": "pediatric_vision_exam_out_network",
                    "Pediatric Preventive Dental": "pediatric_preventive_dental_out_network",
                    "Pediatric Orthodontics": "pediatric_orthodontics_out_network",
                    "Pediatric Major Dental": "pediatric_major_dental_out_network",
                    "Pediatric Eyewear": "pediatric_eyewear_out_network",
                    "Pediatric Emergency Dental": "pediatric_emergency_dental_out_network",
                    "PCP Telemedicine": "pcp_telemedicine_out_network",
                    "Nutritionist Telemedicine": "nutritionist_telemedicine_out_network"
                }
            },
            "maximum_out_of_pocket_limit_single_out_network": "Not Covered",
            "maximum_out_of_pocket_limit_family_out_network": "Not Covered",
            "medical_deductible_single_out_network": "Not Covered",
            "medical_deductible_family_out_network": "Not Covered",
            "pcp_out_network": "Not Covered",
            "specialist_out_network": "Not Covered",
            "preventive_care_out_network": "Not Covered",
            "generic_out_network": "Not Covered",
            "formulary_brand_out_network": "Not Covered",
            "non_formulary_brand_out_network": "Not Covered",
            "non_preferred_generic_out_network": null,
            "non_preferred_brand_out_network": null,
            "rx_deductible_out_network": null,
            "rx_initial_coverage_limit_out_network": null,
            "adult_emergency_dental_out_network": null,
            "adult_eyewear_out_network": null,
            "adult_major_dental_out_network": null,
            "adult_preventive_dental_out_network": null,
            "adult_vision_exam_out_network": null,
            "ambulance_out_network": "Not Covered",
            "ambulatory_surgery_center_out_network": null,
            "chiropractor_out_network": null,
            "clinical_diagnostic_lab_out_network": null,
            "clinical_diagnostic_mri_out_network": "Not Covered",
            "clinical_diagnostic_radiation_out_network": null,
            "clinical_diagnostic_xray_out_network": "Not Covered",
            "diabetic_supplies_out_network": null,
            "diagnostic_out_network": "Not Covered",
            "durable_medical_equipment_out_network": "Not Covered",
            "emergency_room_out_network": "Not Covered",
            "imaging_out_network": "Not Covered",
            "inpatient_acute_out_network": null,
            "inpatient_facility_out_network": "Not Covered",
            "inpatient_mental_health_out_network": null,
            "inpatient_physician_surgeon_out_network": "Not Covered",
            "mail_order_out_network": null,
            "nutritionist_telemedicine_out_network": null,
            "outpatient_facility_out_network": "Not Covered",
            "outpatient_mental_behavior_health_out_network": null,
            "outpatient_physician_surgeon_out_network": "Not Covered",
            "pcp_telemedicine_out_network": null,
            "pediatric_emergency_dental_out_network": null,
            "pediatric_eyewear_out_network": null,
            "pediatric_major_dental_out_network": null,
            "pediatric_orthodontics_out_network": null,
            "pediatric_preventive_dental_out_network": null,
            "pediatric_vision_exam_out_network": null,
            "physical_occupational_speech_out_network": null,
            "preferred_brand_out_network": null,
            "preferred_generic_out_network": null,
            "preventive_dental_out_network": null,
            "prosthetics_out_network": null,
            "routine_eye_exam_out_network": null,
            "skilled_nursing_facility_out_network": "Not Covered",
            "specialty_out_network": "Not Covered",
            "urgent_care_out_network": "Not Covered",
            "pcp_percentage_number_after_deductible": null,
            "pcp_amount_number_after_deductible": null,
            "pcp_percentage_number_before_deductible": null,
            "pcp_amount_number_before_deductible": 0
        },
        "carrier_plan_identifier": null,
        "model_name": "medical_plans"
    }
]
```

Use this endpoint to get all the group plans available. A list of plans should be returned. In the example there's only one plan, since the json is pretty long, but usually there are several plans.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plans/group_plans`

### Parameters

No parameters required.


## Get Pricing for Available Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans_pricing' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: rVTzBq3e3ZbyWoOXjpLuXQ' \
--header 'client: ukIdapo9RQvkaMkt-HeMUg' \
--header 'expiry: 1583919204' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans_pricing"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "rVTzBq3e3ZbyWoOXjpLuXQ")
  req.Header.Add("client", "ukIdapo9RQvkaMkt-HeMUg")
  req.Header.Add("expiry", "1583919204")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans_pricing",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "rVTzBq3e3ZbyWoOXjpLuXQ",
    "client": "ukIdapo9RQvkaMkt-HeMUg",
    "expiry": "1583919204",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans_pricing"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"rVTzBq3e3ZbyWoOXjpLuXQ",
  @"client": @"ukIdapo9RQvkaMkt-HeMUg",
  @"expiry": @"1583919204",
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22rVTzBq3e3ZbyWoOXjpLuXQ%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22ukIdapo9RQvkaMkt-HeMUg%22%2C%22expiry%22%3A%221583919204%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "rVTzBq3e3ZbyWoOXjpLuXQ")
$headers.Add("client", "ukIdapo9RQvkaMkt-HeMUg")
$headers.Add("expiry", "1583919204")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/group_plans_pricing' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
  {
    "id": 4175,
    "product_plan_identifier": null,
    "premiums": {
      "member_prices": {
        "households": {
          "262915": 500.98,
          "262916": 536.19,
          "262917": 2854.96,
          "262918": 2450.29,
          "262919": 1274.71
        },
        "members": {
          "325266": 500.98,
          "325267": 536.19,
          "325268": 584.34,
          "325269": 690.37,
          "325270": 256.97,
          "325271": 256.97,
          "325272": 256.97,
          "325273": 0,
          "325274": 0,
          "325275": 0,
          "325276": 0,
          "325277": 404.67,
          "325278": 404.67,
          "325279": 584.34,
          "325280": 690.37,
          "325281": 256.97,
          "325282": 256.97,
          "325283": 0,
          "325284": 0,
          "325285": 0,
          "325286": 0,
          "325287": 0,
          "325288": 256.97,
          "325289": 404.67,
          "325290": 584.34,
          "325291": 690.37
        }
      },
      "total_monthly_premium": 7617.13,
      "total_annual_premium": 91405.56
    }
  }
]
```

Use this endpoint to list the prices for the group plans. A list of prices should be returned. In the example there's only one price, since the json is pretty long, but usually there are several prices.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plans/group_plans_pricing`

### Parameters

No parameters required.


## Get Individual Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: 9ckA3PW4QEnYuttzaKyE6A' \
--header 'client: j9K0fvoNN6PFS35k53FaRg' \
--header 'expiry: 1583920753' \
--header 'uid: apidoc+broker@wellthie.com' \
--header 'Authorization: Bearer ns3G08ntHNhQlrjb0zZzgw' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "9ckA3PW4QEnYuttzaKyE6A")
  req.Header.Add("client", "j9K0fvoNN6PFS35k53FaRg")
  req.Header.Add("expiry", "1583920753")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")
  req.Header.Add("Authorization", "Bearer ns3G08ntHNhQlrjb0zZzgw")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "9ckA3PW4QEnYuttzaKyE6A",
    "client": "j9K0fvoNN6PFS35k53FaRg",
    "expiry": "1583920753",
    "uid": "apidoc+broker@wellthie.com",
    "Authorization": "Bearer ns3G08ntHNhQlrjb0zZzgw"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"9ckA3PW4QEnYuttzaKyE6A",
  @"client": @"j9K0fvoNN6PFS35k53FaRg",
  @"expiry": @"1583920753",
  @"uid": @"apidoc+broker@wellthie.com",
  @"Authorization": @"Bearer ns3G08ntHNhQlrjb0zZzgw"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "9ckA3PW4QEnYuttzaKyE6A")
$headers.Add("client", "j9K0fvoNN6PFS35k53FaRg")
$headers.Add("expiry", "1583920753")
$headers.Add("uid", "apidoc+broker@wellthie.com")
$headers.Add("Authorization", "Bearer ns3G08ntHNhQlrjb0zZzgw")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
  {
    "promotional_label": null,
    "issuer_logo_url": "/static/images/default-insurance-logo.png",
    "id": 18639,
    "name": "Sparrow PHP Platinum 500-100Percent Exclusive",
    "medical_deductible_single": "$500",
    "maximum_out_of_pocket_limit_single": "$1800",
    "highlight_1": null,
    "highlight_2": null,
    "highlight_3": null,
    "available_exchanges": {
      "icon": "icon--exchange-type",
      "value": "Available On/Off Exchange"
    },
    "sbc_download_url": "http://www.phpmichigan.com/upload/docs/ChoosePHPMI/SBCs/2017Plans/60829MI0190007_Ind2017S_Platinum500100Exc_OnBase_PNN00700RX08E368.pdf",
    "network_url": null,
    "formulary_url": null,
    "hios_plan_identifier": "99926MI101",
    "pcp": "$20",
    "specialist": "$35",
    "benefits": [
      {
        "row_key": "main_benefits_heading",
        "display_key": "Plan Attribute Display Name: main_benefits_heading",
        "tooltip_key": "Plan Attribute Tooltip: main_benefits_heading",
        "content": "Plan Attribute Display Name: main_benefits_heading",
        "heading_row": true,
        "details_view": false
      },
      {
        "row_key": "medical_deductible_single",
        "display_key": "Plan Attribute Display Name: medical_deductible_single",
        "tooltip_key": "Plan Attribute Tooltip: medical_deductible_single",
        "content": "$500",
        "heading_row": false,
        "details_view": null
      },
      {
        "row_key": "maximum_out_of_pocket_limit_single",
        "display_key": "Plan Attribute Display Name: maximum_out_of_pocket_limit_single",
        "tooltip_key": "Plan Attribute Tooltip: maximum_out_of_pocket_limit_single",
        "content": "$1800",
        "heading_row": false,
        "details_view": null
      },
      {
        "row_key": "preventive_care",
        "display_key": "Plan Attribute Display Name: preventive_care",
        "tooltip_key": "Plan Attribute Tooltip: preventive_care",
        "content": "$0",
        "heading_row": false,
        "details_view": true
      },
      {
        "row_key": "pcp",
        "display_key": "Plan Attribute Display Name: pcp",
        "tooltip_key": "Plan Attribute Tooltip: pcp",
        "content": "$20",
        "heading_row": false,
        "details_view": true
      },
      {
        "row_key": "specialist",
        "display_key": "Plan Attribute Display Name: specialist",
        "tooltip_key": "Plan Attribute Tooltip: specialist",
        "content": "$35",
        "heading_row": false,
        "details_view": true
      },
      {
        "row_key": "prescription_drugs",
        "display_key": "Plan Attribute Display Name: prescription_drugs",
        "tooltip_key": "Plan Attribute Tooltip: prescription_drugs",
        "content": "Plan Attribute Display Name: prescription_drugs",
        "heading_row": true,
        "details_view": false
      }
    ],
    "tags": [
      "mi-state",
      "off_exchange_plans",
      "on_exchange_plans"
    ],
    "group_or_individual_plan_type": "Individual",
    "metal_level_name": "Platinum",
    "product_plan_identifier": null,
    "on_exchange": true,
    "off_exchange": true,
    "issuer": {
      "id": 103,
      "name": "MI State",
      "main_logo_url": "/static/images/default-insurance-logo.png",
      "enrollment_resources": []
    }
  }
]
```

Use this endpoint to list the individual plans available.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/inquiries/:inquiry_slug/plans/individual_plans`

### Parameters

No parameters required.

## Get Pricing for Individual Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans_pricing' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: 9ckA3PW4QEnYuttzaKyE6A' \
--header 'client: j9K0fvoNN6PFS35k53FaRg' \
--header 'expiry: 1583920753' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans_pricing"
  method := "GET"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "9ckA3PW4QEnYuttzaKyE6A")
  req.Header.Add("client", "j9K0fvoNN6PFS35k53FaRg")
  req.Header.Add("expiry", "1583920753")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans_pricing",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "9ckA3PW4QEnYuttzaKyE6A",
    "client": "j9K0fvoNN6PFS35k53FaRg",
    "expiry": "1583920753",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans_pricing"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"9ckA3PW4QEnYuttzaKyE6A",
  @"client": @"j9K0fvoNN6PFS35k53FaRg",
  @"expiry": @"1583920753",
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "9ckA3PW4QEnYuttzaKyE6A")
$headers.Add("client", "j9K0fvoNN6PFS35k53FaRg")
$headers.Add("expiry", "1583920753")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans_pricing' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
    {
        "id": 58130,
        "carrier_plan_identifier": null,
        "premiums": {
            "member_prices": {
                "households": {
                    "409759": 420.55,
                    "409760": 420.55
                },
                "members": {
                    "506247": 420.55,
                    "506248": 420.55
                }
            },
            "total_monthly_premium": 841.1,
            "total_annual_premium": 10093.2
        }
    }
]
```

Use this endpoint to list the pricing for the available individual plans.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plans/individual_plans_pricing`

### Parameters

No parameters required.

## POST SelectPlan

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/select' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: 9ckA3PW4QEnYuttzaKyE6A' \
--header 'client: j9K0fvoNN6PFS35k53FaRg' \
--header 'expiry: 1583920753' \
--header 'uid: apidoc+broker@wellthie.com' \
--data-raw '{
    "order": 1,
    "plan_id": 78720,
    "plan_type": "medical",
    "selected_for_quote": true
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/select"
  method := "POST"

  payload := strings.NewReader("{\n    \"order\": 1,\n    \"plan_id\": 78720,\n    \"plan_type\": \"medical\",\n    \"selected_for_quote\": true\n}")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "9ckA3PW4QEnYuttzaKyE6A")
  req.Header.Add("client", "j9K0fvoNN6PFS35k53FaRg")
  req.Header.Add("expiry", "1583920753")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/select",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "9ckA3PW4QEnYuttzaKyE6A",
    "client": "j9K0fvoNN6PFS35k53FaRg",
    "expiry": "1583920753",
    "uid": "apidoc+broker@wellthie.com"
  },
  "data": JSON.stringify({"order":1,"plan_id":78720,"plan_type":"medical","selected_for_quote":true}),
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/select"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"9ckA3PW4QEnYuttzaKyE6A",
  @"client": @"j9K0fvoNN6PFS35k53FaRg",
  @"expiry": @"1583920753",
  @"uid": @"apidoc+broker@wellthie.com"
};

[request setAllHTTPHeaderFields:headers];
NSData *postData = [[NSData alloc] initWithData:[@"{\n    \"order\": 1,\n    \"plan_id\": 78720,\n    \"plan_type\": \"medical\",\n    \"selected_for_quote\": true\n}" dataUsingEncoding:NSUTF8StringEncoding]];
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%229ckA3PW4QEnYuttzaKyE6A%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22j9K0fvoNN6PFS35k53FaRg%22%2C%22expiry%22%3A%221583920753%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "9ckA3PW4QEnYuttzaKyE6A")
$headers.Add("client", "j9K0fvoNN6PFS35k53FaRg")
$headers.Add("expiry", "1583920753")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = "{`n    `"order`": 1,`n    `"plan_id`": 78720,`n    `"plan_type`": `"medical`",`n    `"selected_for_quote`": true`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/select' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
  "id": 136305,
  "individual_plan_id": null,
  "medical_plan_id": 78720,
  "ancillary_plan_id": null,
  "ancillary_plan_type": null,
  "selected_for_quote": true,
  "selected_for_enrollment": false,
  "order": 1
}

```

Use this endpoint to select a plan for quote.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`POST           /api/inquiries/:inquiry_slug/plans/select`

### Parameters

No parameters required.

## DELETE UnselectPlan

```shell
curl --location --request DELETE 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/unselect?plan_id=78720&plan_type=medical' \
--header 'Content-Type: application/json' \
--header 'Cookie: auth_headers=%7B%22access-token%22%3A%22cuqWc2emYOTLq3EueiTvDg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583921338%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D' \
--header 'access-token: cuqWc2emYOTLq3EueiTvDg' \
--header 'client: pkevB8VD4yONukgbtPUFFw' \
--header 'expiry: 1583921338' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/unselect?plan_id=78720&plan_type=medical"
  method := "DELETE"

  payload := strings.NewReader("")

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, payload)

  if err != nil {
    fmt.Println(err)
  }
  req.Header.Add("Content-Type", "application/json")
  req.Header.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22cuqWc2emYOTLq3EueiTvDg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583921338%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
  req.Header.Add("access-token", "cuqWc2emYOTLq3EueiTvDg")
  req.Header.Add("client", "pkevB8VD4yONukgbtPUFFw")
  req.Header.Add("expiry", "1583921338")
  req.Header.Add("uid", "apidoc+broker@wellthie.com")

  res, err := client.Do(req)
  defer res.Body.Close()
  body, err := ioutil.ReadAll(res.Body)

  fmt.Println(string(body))
}
```

```javascript
var settings = {
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/unselect?plan_id=78720&plan_type=medical",
  "method": "DELETE",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Cookie": "auth_headers=%7B%22access-token%22%3A%22cuqWc2emYOTLq3EueiTvDg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583921338%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
    "access-token": "cuqWc2emYOTLq3EueiTvDg",
    "client": "pkevB8VD4yONukgbtPUFFw",
    "expiry": "1583921338",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/unselect?plan_id=78720&plan_type=medical"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Cookie": @"auth_headers=%7B%22access-token%22%3A%22cuqWc2emYOTLq3EueiTvDg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583921338%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D",
  @"access-token": @"cuqWc2emYOTLq3EueiTvDg",
  @"client": @"pkevB8VD4yONukgbtPUFFw",
  @"expiry": @"1583921338",
  @"uid": @"apidoc+broker@wellthie.com"
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
$headers.Add("Cookie", "auth_headers=%7B%22access-token%22%3A%22cuqWc2emYOTLq3EueiTvDg%22%2C%22token-type%22%3A%22Bearer%22%2C%22client%22%3A%22pkevB8VD4yONukgbtPUFFw%22%2C%22expiry%22%3A%221583921338%22%2C%22uid%22%3A%22apidoc%2Bbroker%40wellthie.com%22%7D")
$headers.Add("access-token", "cuqWc2emYOTLq3EueiTvDg")
$headers.Add("client", "pkevB8VD4yONukgbtPUFFw")
$headers.Add("expiry", "1583921338")
$headers.Add("uid", "apidoc+broker@wellthie.com")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/JXID6718/plans/unselect?plan_id=78720&plan_type=medical' -Method 'DELETE' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> This request doesn't contain any response. Http response code would be 204.

```json

```

> In case of failure scenario like plan not selected...

```json
[
    "Plan requested to remove is not Selected"
]
```

Use this endpoint to select a plan for quote.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>authentication headers</i></strong>. These include 
  <br/><code style="margin-left: 30px">1. <i>Cookie: auth_headers</i></code>,
  <br/><code style="margin-left: 30px">2. <i>uid</i></code>,
  <br/><code style="margin-left: 30px">3. <i>client</i></code>,
  <br/><code style="margin-left: 30px">4. <i>access-token</i></code> and 
  <br/><code style="margin-left: 30px">5. <i>expiry</i></code>.
</aside>

### HTTP Request

`DELETE         /api/inquiries/:inquiry_slug/plans/unselect`

### Parameters

No parameters required.
