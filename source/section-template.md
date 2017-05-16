## <operation_name>

```shell
curl -X <METHOD> "" \
     -H "Content-Type: application/json" \
     -H "access-token: kZgVhiDPIIwkBaFPmp9I3Q" \
     -H "uid: sebastian.jimenez@crossover.com" \
     -H "client: hiF9kRj-PjmoWQSU80AL6Q" \
     -d '{ JSON DATA HERE }'
```

> Response looks like this:

```json
{
  JSON RESPONSE HERE
}
```

Describe endpoint here.

<aside class="notice">
  This endpoint is secured and requires authentication headers.
</aside>

### HTTP Request

`<METHOD> path`

### Parameters

Parameter    | Default | Description           | Required?
------------ | ------- | --------------------- | ----------
email        | N/A     | User's email address  | true
password     | N/A     | User's password       | true
