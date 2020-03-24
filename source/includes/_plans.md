# Plans

A Plan is the specifics of various plans (e.g. medical insurance). These include rules, regulations, benefits covered, benefits not covered, cost for the policy holder, how much the policy holder pays vs how much the insurance covers, etc.

This section of the API Doc helps with various aspects of fetching and selecting/unselecting different types of plans for the given [census](#census).

## Get Available Group Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans"
  method := "GET"

  payload := strings.NewReader("")

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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans' -Method 'GET' -Headers $headers -Body $body
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

Use this endpoint to get all the group plans available. In the example there's only one plan, but usually there are several plans.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plans/group_plans`

### Parameters

No parameters required.

## Get Pricing for Group Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans_pricing' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans_pricing"
  method := "GET"

  payload := strings.NewReader("")

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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans_pricing",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans_pricing"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/group_plans_pricing' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
    {
        "id": 78699,
        "carrier_plan_identifier": null,
        "premiums": {
            "member_prices": {
                "households": {
                    "423038": 627.63,
                    "423039": 1255.26,
                    "423040": 1788.75,
                    "423041": 1066.97
                },
                "members": {
                    "523302": 627.63,
                    "523303": 1255.26,
                    "523304": 0.0,
                    "523305": 1788.75,
                    "523306": 0.0,
                    "523307": 0.0,
                    "523308": 1066.97,
                    "523309": 0.0
                }
            },
            "total_monthly_premium": 4738.61,
            "total_annual_premium": 56863.32
        }
    },
]
```

Use this endpoint to list the prices for the group plans. In the example there's only one price, but usually there are several prices.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plans/group_plans_pricing`

### Parameters

No parameters required.

## Get Individual Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM' \
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
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

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
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

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
        "id": 58130,
        "name": "Fidelis Care Bronze",
        "service_area_id": 3684,
        "highlight_1": {
            "icon": "icon--metal",
            "value": "Bronze"
        },
        "highlight_2": {
            "icon": "icon--add-on",
            "value": "PCP 50% coinsurance"
        },
        "highlight_3": {
            "icon": "icon--add-on",
            "value": "Specialist 50% coinsurance"
        },
        "highlight_4": null,
        "highlight_5": null,
        "highlight_6": null,
        "available_exchanges": {
            "icon": "icon--exchange-type",
            "value": "Available On/Off Exchange"
        },
        "sbc_download_url": null,
        "network_url": "https://www.fideliscare.org/FindADoctor/#/search",
        "formulary_url": "https://www.fideliscare.org/en-us/products/nystateofhealth.aspx",
        "hios_plan_identifier": "25303NY0010001",
        "plan_year": 2019,
        "tags": [
            "bronze",
            "hmo",
            "on_exchange",
            "off_exchange",
            "adult_vision_coverage_included"
        ],
        "group_or_individual_plan_type": "Individual",
        "metal_level_name": "Bronze",
        "on_exchange": true,
        "off_exchange": true,
        "plan_description": null,
        "plan_detail_header": null,
        "plan_detail_items": null,
        "plan_detail_footer": null,
        "composite_rating": false,
        "hsa_eligible": false,
        "issuer": {
            "id": 803,
            "name": "Fidelis Care",
            "parameterized_name": "fidelis-care",
            "composite_ee_factor": null,
            "composite_es_factor": null,
            "composite_ec_factor": null,
            "composite_ef_factor": null,
            "enrollment_content_area_name": null,
            "main_logo_url": "/static/images/default-insurance-logo.png",
            "issuer_enrollment_resources": []
        },
        "medical_plan_benefit": {
            "medical_plan_id": 58130,
            "medical_deductible_single": "$4,000",
            "medical_deductible_family": "$8,000",
            "maximum_out_of_pocket_limit_single": "$7,600",
            "maximum_out_of_pocket_limit_family": "$15,200",
            "pcp": "50% coinsurance",
            "specialist": "50% coinsurance",
            "preventive_care": "$0",
            "inpatient_facility": "50% coinsurance",
            "outpatient_facility": "50% coinsurance",
            "outpatient_physician_surgeon": "50% coinsurance",
            "imaging": "50% coinsurance",
            "durable_medical_equipment": "50% coinsurance",
            "diagnostic": null,
            "emergency_room": "50% coinsurance",
            "urgent_care": "50% coinsurance",
            "ambulance": "50% coinsurance",
            "rx_deductible": null,
            "generic": "$10",
            "formulary_brand": "$35",
            "non_formulary_brand": "$70",
            "mail_order": "2.5x above",
            "adult_vision_exam": null,
            "adult_preventive_dental": null,
            "adult_major_dental": null,
            "adult_eyewear": "50% coinsurance",
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
            "deductible_single_number": 4000,
            "deductible_family_number": 8000,
            "moop_single_number": 7600,
            "moop_family_number": 15200,
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
            "maximum_out_of_pocket_limit_single_out_network": null,
            "maximum_out_of_pocket_limit_family_out_network": null,
            "medical_deductible_single_out_network": null,
            "medical_deductible_family_out_network": null,
            "pcp_out_network": null,
            "specialist_out_network": null,
            "preventive_care_out_network": null,
            "generic_out_network": null,
            "formulary_brand_out_network": null,
            "non_formulary_brand_out_network": null,
            "non_preferred_generic_out_network": null,
            "non_preferred_brand_out_network": null,
            "rx_deductible_out_network": null,
            "rx_initial_coverage_limit_out_network": null,
            "adult_emergency_dental_out_network": null,
            "adult_eyewear_out_network": null,
            "adult_major_dental_out_network": null,
            "adult_preventive_dental_out_network": null,
            "adult_vision_exam_out_network": null,
            "ambulance_out_network": null,
            "ambulatory_surgery_center_out_network": null,
            "chiropractor_out_network": null,
            "clinical_diagnostic_lab_out_network": null,
            "clinical_diagnostic_mri_out_network": null,
            "clinical_diagnostic_radiation_out_network": null,
            "clinical_diagnostic_xray_out_network": null,
            "diabetic_supplies_out_network": null,
            "diagnostic_out_network": null,
            "durable_medical_equipment_out_network": null,
            "emergency_room_out_network": null,
            "imaging_out_network": null,
            "inpatient_acute_out_network": null,
            "inpatient_facility_out_network": null,
            "inpatient_mental_health_out_network": null,
            "inpatient_physician_surgeon_out_network": null,
            "mail_order_out_network": null,
            "nutritionist_telemedicine_out_network": null,
            "outpatient_facility_out_network": null,
            "outpatient_mental_behavior_health_out_network": null,
            "outpatient_physician_surgeon_out_network": null,
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
            "skilled_nursing_facility_out_network": null,
            "specialty_out_network": null,
            "urgent_care_out_network": null,
            "pcp_percentage_number_after_deductible": null,
            "pcp_amount_number_after_deductible": null,
            "pcp_percentage_number_before_deductible": 50,
            "pcp_amount_number_before_deductible": null
        },
        "carrier_plan_identifier": null,
        "model_name": "medical_plans"
    },
]
```

Use this endpoint to list the individual plans available. In the example there's only one plan, but usually there are several plans.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plans/individual_plans`

### Parameters

No parameters required.

## Get Pricing for Individual Plans

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/ZVTD8453/plans/individual_plans_pricing' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM' \
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
  req.Header.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

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
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

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

Use this endpoint to list the pricing for the available individual plans. In the example there's only one pricing data, but usually there are several plan's pricing data returned.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plans/individual_plans_pricing`

### Parameters

No parameters required.

## Select a Plan for Inquiry 

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/select' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/select"
  method := "POST"

  payload := strings.NewReader("{\n    \"order\": 1,\n    \"plan_id\": 78720,\n    \"plan_type\": \"medical\",\n    \"selected_for_quote\": true\n}")

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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/select",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/select"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

$body = "{`n    `"order`": 1,`n    `"plan_id`": 78720,`n    `"plan_type`": `"medical`",`n    `"selected_for_quote`": true`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/select' -Method 'POST' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
{
    "id": 136333,
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`POST           /api/inquiries/:inquiry_slug/plans/select`

### Parameters

No parameters required.

## Unselect a Plan from Inquiry

```shell
curl --location --request DELETE 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/unselect?plan_id=78720&plan_type=medical' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/unselect?plan_id=78720&plan_type=medical"
  method := "DELETE"

  payload := strings.NewReader("")

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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/unselect?plan_id=78720&plan_type=medical",
  "method": "DELETE",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```objective_c
#import <Foundation/Foundation.h>

dispatch_semaphore_t sema = dispatch_semaphore_create(0);

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/unselect?plan_id=78720&plan_type=medical"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiRnZ2d2wxR0RQYzBranVBUEpWVjhpZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ2MjA0MjF9.fviApfd2KXRYfMJHHpjW5EKJ9dBNEHROrEnwtOnG6TM")

$body = ""

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LAPF8357/plans/unselect?plan_id=78720&plan_type=medical' -Method 'DELETE' -Headers $headers -Body $body
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
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

### HTTP Request

`DELETE         /api/inquiries/:inquiry_slug/plans/unselect`

### Parameters

No parameters required.

## Get Selected plans of an Inquiry

Use this endpoint to retrieve inquiry's plan selections. Up to four plans can be selected.

<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

```shell
curl --location --request GET 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/INBF8325/plan_selections' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/INBF8325/plan_selections"
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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/INBF8325/plan_selections",
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/INBF8325/plan_selections"]
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

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/INBF8325/plan_selections' -Method 'GET' -Headers $headers -Body $body
$response | ConvertTo-Json
```

> Response looks like this:

```json
[
    {
        "id": 136318,
        "individual_plan_id": null,
        "medical_plan_id": 78717,
        "ancillary_plan_id": null,
        "ancillary_plan_type": null,
        "selected_for_quote": true,
        "selected_for_enrollment": false,
        "order": 0
    },
    {
        "id": 136319,
        "individual_plan_id": null,
        "medical_plan_id": 78720,
        "ancillary_plan_id": null,
        "ancillary_plan_type": null,
        "selected_for_quote": true,
        "selected_for_enrollment": false,
        "order": 1
    }
]
```

### HTTP Request

`GET /api/inquiries/:inquiry_slug/plan_selections`

### Parameters

No parameters required.

## Get Company's Current Plan

<aside class="success">
  Current plan details are sent as part of <a href="#get-company-details">Get Company Details</a>
</aside>

## Create Company's Current Plan

Use this endpoint to create a new `current_plan` to a company. This is used for renewal quotes (`is_renewal` is set to true).
<aside class="notice">
  This endpoint is <strong><i>secured</i></strong> and requires <strong><i>Authorization header</i></strong>. 
</aside>

```shell
curl --location --request POST 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/current_plan' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE' \
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

  url := "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/current_plan"
  method := "POST"

  payload := strings.NewReader("{\n  \"current_plan\": {\n    \"product_type\": \"medical\",\n    \"name\": \"Current Plan Name\",\n    \"current_plan_issuer\": \"Current Plan Issuer\",\n    \"metal_level_name\": \"Bronze\",\n    \"employer_monthly_cost\": 1000,\n    \"carrier_plan_identifier\": \"123\",\n    \"medical_deductible_single\": \"Deductible Single\",\n    \"medical_deductible_family\": \"Deductible Single\",\n    \"maximum_out_of_pocket_limit_single\": \"Deductible Single\",\n    \"specialist\": \"Specialist\",\n    \"pcp\": \"Primary Care Physician\",\n    \"maximum_out_of_pocket_limit_family\": \"Max-Out-of-Pocket Family\",\n    \"network_type\": \"Network\",\n    \"preventive_care\": \"Preventive Care\",\n    \"inpatient_facility\": \"Hospital (Inpatient)\",\n    \"emergency_room\": \"Emergency Room\",\n    \"ambulance\": \"Ambulance\",\n    \"urgent_care\": \"Urgent Care\",\n    \"generic\": \"Generic Prescription\",\n    \"formulary_brand\": \"Formulary Prescription\",\n    \"non_formulary_brand\": \"Non Formulary Brand Prescription\",\n    \"mail_order\": \"Mail Order (90 day supply)\"\n  }\n}")

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
  "url": "https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/current_plan",
  "method": "POST",
  "timeout": 0,
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
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

NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/current_plan"]
  cachePolicy:NSURLRequestUseProtocolCachePolicy
  timeoutInterval:10.0];
NSDictionary *headers = @{
  @"Content-Type": @"application/json",
  @"Authorization": @"Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE"
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
$headers.Add("Authorization", "Bearer eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo1ODQ3MSwiY2xpZW50IjoiVU5sRjVaQUxqdW1pZ3lTSVl6SXFyZyIsImlwX2FkZHJlc3MiOiIxMjcuMC4wLjEiLCJzZXNzaW9uX2lkIjoiZGNmOTk4MmQxMjQxNDdiMmVhYzA3YmNlNjg0NzY2YzAiLCJleHAiOjE1ODQ1MTQ5MDV9.tR22SJYO5nHrOnxhXJj7HRAOK-guJT7zOg4kOK-eEPE")

$body = "{`n  `"current_plan`": {`n    `"product_type`": `"medical`",`n    `"name`": `"Current Plan Name`",`n    `"current_plan_issuer`": `"Current Plan Issuer`",`n    `"metal_level_name`": `"Bronze`",`n    `"employer_monthly_cost`": 1000,`n    `"carrier_plan_identifier`": `"123`",`n    `"medical_deductible_single`": `"Deductible Single`",`n    `"medical_deductible_family`": `"Deductible Single`",`n    `"maximum_out_of_pocket_limit_single`": `"Deductible Single`",`n    `"specialist`": `"Specialist`",`n    `"pcp`": `"Primary Care Physician`",`n    `"maximum_out_of_pocket_limit_family`": `"Max-Out-of-Pocket Family`",`n    `"network_type`": `"Network`",`n    `"preventive_care`": `"Preventive Care`",`n    `"inpatient_facility`": `"Hospital (Inpatient)`",`n    `"emergency_room`": `"Emergency Room`",`n    `"ambulance`": `"Ambulance`",`n    `"urgent_care`": `"Urgent Care`",`n    `"generic`": `"Generic Prescription`",`n    `"formulary_brand`": `"Formulary Prescription`",`n    `"non_formulary_brand`": `"Non Formulary Brand Prescription`",`n    `"mail_order`": `"Mail Order (90 day supply)`"`n  }`n}"

$response = Invoke-RestMethod 'https://wellthiedemo-smallbusiness-qa.affordablecareadvisor.net/api/inquiries/LDYA3582/current_plan' -Method 'POST' -Headers $headers -Body $body
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

### HTTP Request

`POST /api/inquiries/:inquiry_slug/current_plan`

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
