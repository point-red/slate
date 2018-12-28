## Show SUpplier

```shell
curl -X GET \
  'https://api.point.red/api/v1/master/suppliers/<id>' \
  -H 'Authorization: Bearer <access_token>' \
  -H 'cache-control: no-cache'
```

> Response

```json
{
    "data": {
        "id": 1,
        "name": "John Doe"
    }
}
```

Show a SUpplier.

### HTTP Request

`GET http://api.point.red/api/v1/master/suppliers/<id>`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id *(required)* | int | The ID of the suppliers to retrieve
