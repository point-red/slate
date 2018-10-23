## Delete Group

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: <access_code>"
```

> Return response 204 with no data

Delete a Group

### HTTP Request

`DELETE http://api.point.red/api/v1/master/groups/<id>`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id *(required)* | int | The ID of the group to delete
group_type *(required)* | string