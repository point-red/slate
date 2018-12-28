## Update Supplier

```shell
curl -X POST \
  https://api.point.red/api/v1/master/suppliers \
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

Update a Supplier.

### HTTP Request

`PATCH http://api.point.red/api/v1/master/suppliers/<id>`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id *(required)* | int | The ID of the group to delete
name *(required)* | string |
