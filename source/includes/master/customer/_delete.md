## Delete Customer

```shell
curl "https://api.point.red/api/v1/master/customers/<id>"
  -X DELETE
  -H "Authorization: <access_code>"
```

> Return response 204 with no data

Delete a Customer

### HTTP Request

`DELETE http://api.point.red/api/v1/master/customers/<id>`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id *(required)* | int | The ID of the group to delete
