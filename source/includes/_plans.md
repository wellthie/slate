# Plans

## List GroupPlans

```shell
curl -X GET "/api/inquiries/JUWD4521/plans/group_plans" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
```

> Response looks like this:

```json
[
  {
    "promotional_label": null,
    "issuer_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/148/main/healthnetlogo.png?1474664189",
    "id": 4175,
    "name": "Full Network HMO Gold $50 + Infertility",
    "medical_deductible_single": "$0 ",
    "maximum_out_of_pocket_limit_single": "$7,150 ",
    "highlight_1": {
      "icon": "icon--metal",
      "value": "Gold"
    },
    "highlight_2": {
      "icon": "icon--network",
      "value": "HMO"
    },
    "highlight_3": {
      "icon": "icon--add-on",
      "value": "PCP $50 "
    },
    "available_exchanges": {
      "icon": "icon--exchange-type",
      "value": "Available Off Exchange"
    },
    "sbc_download_url": "https://www.healthnet.com/portal/shopping/sbc/viewSbcDoc.ndo?filePath=%2Findex%2Fverity%2Fpsa%2Frepos%2F2016%2Fsbc%2Fsbc_manual_doc%2FCZL_A1T_Y9C_B4N_QU_15N_20170101_CA_SBG_HMO_ENG_11172016.pdf",
    "network_url": "https://www.healthnet.com/portal/providerSearch.action#",
    "formulary_url": "https://www.healthnet.com/portal/member/unprotected/find_formulary_druglist.action",
    "hios_plan_identifier": "67138CA0240227",
    "pcp": "$50 ",
    "specialist": "$70 ",
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
        "row_key": "network_type",
        "display_key": "Plan Attribute Display Name: network_type",
        "tooltip_key": "Plan Attribute Tooltip: network_type",
        "content": "HMO",
        "heading_row": false,
        "details_view": null
      },
      {
        "row_key": "medical_deductible_single",
        "display_key": "Plan Attribute Display Name: medical_deductible_single",
        "tooltip_key": "Plan Attribute Tooltip: medical_deductible_single",
        "content": "$0 ",
        "heading_row": false,
        "details_view": null
      },
      {
        "row_key": "maximum_out_of_pocket_limit_single",
        "display_key": "Plan Attribute Display Name: maximum_out_of_pocket_limit_single",
        "tooltip_key": "Plan Attribute Tooltip: maximum_out_of_pocket_limit_single",
        "content": "$7,150 ",
        "heading_row": false,
        "details_view": null
      },
      {
        "row_key": "preventive_care",
        "display_key": "Plan Attribute Display Name: preventive_care",
        "tooltip_key": "Plan Attribute Tooltip: preventive_care",
        "content": "$0 ",
        "heading_row": false,
        "details_view": true
      },
      {
        "row_key": "pcp",
        "display_key": "Plan Attribute Display Name: pcp",
        "tooltip_key": "Plan Attribute Tooltip: pcp",
        "content": "$50 ",
        "heading_row": false,
        "details_view": true
      },
      {
        "row_key": "specialist",
        "display_key": "Plan Attribute Display Name: specialist",
        "tooltip_key": "Plan Attribute Tooltip: specialist",
        "content": "$70 ",
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
      },
      {
        "row_key": "generic",
        "display_key": "Plan Attribute Display Name: generic",
        "tooltip_key": "Plan Attribute Tooltip: generic",
        "content": "$20 ",
        "heading_row": false,
        "details_view": true
      },
      {
        "row_key": "formulary_brand",
        "display_key": "Plan Attribute Display Name: formulary_brand",
        "tooltip_key": "Plan Attribute Tooltip: formulary_brand",
        "content": "$50 ",
        "heading_row": false,
        "details_view": true
      },
      {
        "row_key": "non_formulary_brand",
        "display_key": "Plan Attribute Display Name: non_formulary_brand",
        "tooltip_key": "Plan Attribute Tooltip: non_formulary_brand",
        "content": "$70 ",
        "heading_row": false,
        "details_view": true
      }
    ],
    "tags": [
      "gold",
      "deductible_single_0_to_1000",
      "deductible_family_0_to_2000",
      "5001_to_7500",
      "12001_to_18000",
      "hmo",
      "gold",
      "0_to_2000_deductible_single",
      "0_to_4000",
      "6001_to_8000_moop_single",
      "14001_to_20000",
      "hmo",
      "gold",
      "0_to_2000_deductible_single",
      "0_to_4000",
      "6001_to_8000_moop_single",
      "14001_to_20000",
      "hmo",
      "health-net-of-california-inc",
      "off_exchange_plans"
    ],
    "group_or_individual_plan_type": "Group",
    "metal_level_name": "Gold",
    "product_plan_identifier": null,
    "on_exchange": false,
    "off_exchange": true,
    "issuer": {
      "id": 148,
      "name": "Health Net of California, Inc",
      "main_logo_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/issuers/logos/000/000/148/main/healthnetlogo.png?1474664189",
      "enrollment_resources": [
        {
          "name": "Health Net of California, Inc. Broker Portal",
          "product_type": "Medical",
          "resource_type": "link",
          "display_link_url": "https://www.healthnet.com/portal/broker/home.ndo\t",
          "sort_order": 10
        },
        {
          "name": "Health Net of California, Inc. Small Business Application",
          "product_type": "Medical",
          "resource_type": "file",
          "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/enrollment_resources/attachments/000/000/270/original/small%20group%20application-hj20.pdf?1482446410",
          "sort_order": 20
        },
        {
          "name": "Health Net of California, Inc. Employee Application",
          "product_type": "Medical",
          "resource_type": "file",
          "display_link_url": "https://d3uxyywlniz2wb.cloudfront.net/advisor/development/enrollment_resources/attachments/000/000/271/original/ca_sbg_jan_enrollment_app_2017-lk68.pdf?1482446457",
          "sort_order": 30
        }
      ]
    }
  }
]
```

Use this endpoint to get all the group plans available. A list of plans should be returned. In the example there's only one plan, since the json is pretty long, but usually there are several plans.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/inquiries/JUWD4521/plans/group_plans`

### Parameters

No parameters required.


## List GroupPlansPricing

```shell
curl -X GET "/api/inquiries/JUWD4521/plans/group_plans_pricing" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
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
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/inquiries/JUWD4521/plans/group_plans_pricing`

### Parameters

No parameters required.


## List IndividualPlans

```shell
curl -X GET "/api/inquiries/JUWD4521/plans/individual_plans" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
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
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/inquiries/JUWD4521/plans/individual_plans`

### Parameters

No parameters required.


## List IndividualPlansPricing

```shell
curl -X GET "http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/inquiries/JUWD4521/plans/individual_plans_pricing" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
```

> Response looks like this:

```json
[
  {
    "id": 18652,
    "product_plan_identifier": null,
    "premiums": {
      "member_prices": {
        "households": {
          "262858": 233.41,
          "262859": 213.6,
          "262860": 259.9,
          "262861": 784.71,
          "262862": 433.65
        },
        "members": {
          "325137": 233.41,
          "325138": 213.6,
          "325139": 259.9,
          "325140": 263.24,
          "325141": 256.57,
          "325142": 132.45,
          "325143": 132.45,
          "325144": 301.2,
          "325145": 132.45
        }
      },
      "total_monthly_premium": 1925.27,
      "total_annual_premium": 23103.24
    }
  }
]
```

Use this endpoint to list the pricing for the available individual plans.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET /api/inquiries/JUWD4521/plans/individual_plans_pricing`

### Parameters

No parameters required.


## List Filters

```shell
curl -X GET "http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/inquiries/JUWD4521/plans/filters" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q"
```

> Response looks like this:

```json
[
  {
    "icon": "icon--issuers",
    "value": "issuers",
    "tags": [
      {
        "value": "blue-cross-blue-shield-of-michigan",
        "label_key": "Tag: Name: blue-cross-blue-shield-of-michigan"
      },
      {
        "value": "priority-health",
        "label_key": "Tag: Name: priority-health"
      }
    ],
    "label_key": "Tag Category: Name: issuers"
  },
  {
    "icon": "icon--exchange-type",
    "value": "exchange_type",
    "tags": [
      {
        "value": "off_exchange_plans",
        "label_key": "Tag: Name: off_exchange_plans"
      },
      {
        "value": "on_exchange_plans",
        "label_key": "Tag: Name: on_exchange_plans"
      }
    ],
    "label_key": "Tag Category: Name: exchange_type"
  },
  {
    "icon": "icon--deductible-single",
    "value": "deductible_single",
    "tags": [
      {
        "value": "0_to_2000_deductible_single",
        "label_key": "Tag: Name: 0_to_2000_deductible_single"
      },
      {
        "value": "2001_to_4000_deductible_single",
        "label_key": "Tag: Name: 2001_to_4000_deductible_single"
      },
      {
        "value": "4001_to_6000_deductible_single",
        "label_key": "Tag: Name: 4001_to_6000_deductible_single"
      },
      {
        "value": "6001_to_8000_deductible_single",
        "label_key": "Tag: Name: 6001_to_8000_deductible_single"
      }
    ],
    "label_key": "Tag Category: Name: deductible_single"
  },
  {
    "icon": "icon--metal",
    "value": "metal",
    "tags": [
      {
        "value": "bronze",
        "label_key": "Tag: Name: bronze"
      },
      {
        "value": "silver",
        "label_key": "Tag: Name: silver"
      },
      {
        "value": "gold",
        "label_key": "Tag: Name: gold"
      },
      {
        "value": "platinum",
        "label_key": "Tag: Name: platinum"
      }
    ],
    "label_key": "Tag Category: Name: metal"
  },
  {
    "icon": "icon--moop-single",
    "value": "moop_single",
    "tags": [
      {
        "value": "2001_to_4000_moop_single",
        "label_key": "Tag: Name: 2001_to_4000_moop_single"
      },
      {
        "value": "4001_to_6000_moop_single",
        "label_key": "Tag: Name: 4001_to_6000_moop_single"
      },
      {
        "value": "6001_to_8000_moop_single",
        "label_key": "Tag: Name: 6001_to_8000_moop_single"
      }
    ],
    "label_key": "Tag Category: Name: moop_single"
  },
  {
    "icon": "icon--network",
    "value": "network",
    "tags": [
      {
        "value": "ppo",
        "label_key": "Tag: Name: ppo"
      },
      {
        "value": "hmo",
        "label_key": "Tag: Name: hmo"
      },
      {
        "value": "pos",
        "label_key": "Tag: Name: pos"
      }
    ],
    "label_key": "Tag Category: Name: network"
  }
]
```

Use this endpoint to list the filters for the available plans.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`GET http://wellthiedemo-smallbusiness-test.lvh.me:3030/api/inquiries/JUWD4521/plans/filters`

### Parameters

No parameters required.


## POST SelectPlan (TODO)
`POST           /api/inquiries/:inquiry_slug/plans/select`

NOTE: Should be on its own endpoint and not under inquiry.

## DELETE UnselectPlan (TODO)
`DELETE         /api/inquiries/:inquiry_slug/plans/unselect`

NOTE: Should be on its own endpoint and not under inquiry.

## Compare (TODO)

NOTE: Should be on its own endpoint and not under inquiry.

`POST           /api/inquiries/:inquiry_slug/plans/compare/generate_excel`

`GET            /api/inquiries/:inquiry_slug/plans/compare/download_excel`

`POST           /api/inquiries/:inquiry_slug/plans/compare/generate_filtered_plan_excel`

`GET            /api/inquiries/:inquiry_slug/plans/compare/download_filtered_plan_excel`
