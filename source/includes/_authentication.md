# Authentication

## Sign In

```shell
curl -X POST "/api/auth/sign_in" \
     -H "Content-Type: application/json" \
     -d '{"email": "name.lastname@domain.com", "password": "pswrd"}'
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
curl -X DELETE "/api/auth/sign_out" \
     -H "Content-Type: application/json" \
     -d '{"uid": "name.lastname@domain.com", "client": "WedFsHGWTiAfdhl4LbFVjg", "access-token": "UyuaNMouSdihadn"}'
```

> Response looks like this:

```json
{
  "success": true
}
```

Use this endpoint to finish the session and discard the access-token acquired on the sign in API call

### HTTP Request

`POST /api/auth/sign_out`

### Parameters

Parameter    | Default | Description            | Required?
------------ | ------- | ---------------------- | ----------
uid          | N/A     | User's email address   | true
client       | N/A     | Client token [HEADERS] | true
access-token | N/A     | Token from sign in     | true
