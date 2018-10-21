# Groups

## Get Groups

```shell
curl -X GET \
  'https://api.point.red/api/v1/master/groups?group_type=customer' \
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

Retrieves all groups of master.

You need to specify which groups you want to retrieve, there is available master :
customer / supplier / item / service / employee

### HTTP Request

`GET http://api.point.red/api/v1/master/groups`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
group_type *(required)* | string | 

## Find Group

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

This endpoint retrieves a specific kitten.

### HTTP Request

`GET http://api.point.red/api/v1/master/groups/<id>`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id *(required)* | int | The ID of the groups to retrieve
group_type *(required)* | string |

## Delete a Group

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
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
