## Create Customer

```shell
curl -X POST \
  https://api.point.red/api/v1/master/customers \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer <access_token>' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'name=<name>'
```

> Response

```json
{
    "data": {
        "id": 1,
        "name": "John Doe",
        "updated_at": "2018-10-22 06:14:27",
        "created_at": "2018-10-22 06:14:27",
        "updated_by": 1,
        "created_by": 1
    }
}
```

Create a Customer.

### HTTP Request

`POST http://api.point.red/api/v1/master/customers`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
name *(required)* | string |
