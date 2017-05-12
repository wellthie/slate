## <operation_name>

```shell
curl -X POST "/api/< path_to_endpoint >" \
     -H "Content-Type: application/json" \
     -d '{ JSON DATA HERE }'
```

> Response looks like this:

```json
{
  JSON RESPONSE HERE
}
```

Describe endpoint here.

### HTTP Request

`POST /api/< path_to_endpoint >`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
email        | N/A     | User's email address  | true
password     | N/A     | User's password       | true
