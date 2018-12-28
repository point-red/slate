## Delete Supplier

```shell
curl "https://api.point.red/api/v1/master/suppliers/<id>"
  -X DELETE
  -H "Authorization: <access_code>"
```

> Return response 204 with no data

Delete a Supplier

### HTTP Request

`DELETE http://api.point.red/api/v1/master/suppliers/<id>`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id *(required)* | int | The ID of the group to delete
