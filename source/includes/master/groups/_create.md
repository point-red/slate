## Create Group

```shell
curl -X POST \
  https://api.point.red/api/v1/master/groups \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer <access_token>' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'type=<type>&name=<name>'
```

> Response

```json
{
    "data": {
        "id": 1,
        "name": "John Doe",
        "type": "App\\Model\\Master\\Customer",
        "updated_at": "2018-10-22 06:14:27",
        "created_at": "2018-10-22 06:14:27",
        "updated_by": 1,
        "created_by": 1
    }
}
```

Create a Group.

### HTTP Request

`POST http://api.point.red/api/v1/master/groups`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
type *(required)* | string |
name *(required)* | string |
