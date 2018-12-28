## Get Groups

```shell
curl -X GET \
  'https://api.point.red/api/v1/master/groups?type=customer' \
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
            "name": "General",
            "type": "App\\Model\\Master\\Customer"
        },
        {
            "id": 2,
            "name": "Member",
            "type": "App\\Model\\Master\\Customer"
        }
    ]
}
```

List Groups.

### HTTP Request

`GET http://api.point.red/api/v1/master/groups`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
type *(required)* | string | 
