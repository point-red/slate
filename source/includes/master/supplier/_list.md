## Get Supplier

```shell
curl -X GET \
  'https://api.point.red/api/v1/master/suppliers' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer <access_token>' \
  -H 'Content-Type: application/json' \
  -H 'cache-control: no-cache'
```

> Response

```json
{
    "data": [
        {
            "id": 1,
            "name": "John Doe",
        },
        {
            "id": 2,
            "name": "Charlie",
        }
    ]
}
```

List Supplier.

### HTTP Request

`GET http://api.point.red/api/v1/master/suppliers`
