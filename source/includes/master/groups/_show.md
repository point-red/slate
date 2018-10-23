## Show Group

```shell
curl -X GET \
  'https://api.point.red/api/v1/master/groups/<id>?group_type=customer' \
  -H 'Authorization: Bearer <access_token>' \
  -H 'cache-control: no-cache'
```

> Response

```json
{
    "data": {
        "id": 1,
        "type": "App\\Model\\Master\\Customer",
        "name": "General"
    }
}
```

Show a group.

### HTTP Request

`GET http://api.point.red/api/v1/master/groups/<id>`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id *(required)* | int | The ID of the groups to retrieve
group_type *(required)* | string |