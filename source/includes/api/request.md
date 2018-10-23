# API Request

To construct a REST API request, combine these components:

## API Service URL

* `SANDBOX` = https://api.sandbox.point.red
* `LIVE` = https://api.point.red

## HTTP Methods

RESTful APIs enable you to develop any kind of web application having all possible CRUD (create, retrieve, update, delete) operations. REST guidelines suggest using a specific HTTP method on a specific type of call made to the server

| Method   | Description                                      |
| -------- | ------------------------------------------------ |
| `DELETE` | Deletes a resource.                              |
| `GET`    | Shows details for a resource or lists resources. |
| `PATCH`  | Partially updates a resource.                    |
| `POST`   | Creates or manages a resource.                   |
| `PUT`    | Updates a resource.                              |

## HTTP Request Headers

HTTP request headers is a component of a network packet sent by a browser or client to the server to request for a specific page or data on the Web server. The commonly used HTTP request headers are:

| Header            | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| **Accept**        | Required for operations with a response body. Specifies the response format. The syntax is: `Accept: application/json`. |
| **Content-Type**  | Required for operations with a request body. Specifies the request format. The syntax is: `Content-Type: application/json`. |
| **Authorization** | Required to get an access token or make API calls. To make REST API calls, include the bearer token in the `Authorization` header with the `Bearer` authentication scheme: `Authorization: Bearer <access_token>` |
| **Tenant** | Required for all request to your project, `Tenant` is a project code when you creating a new project |

## Query parameters

Optional. Controls which data appears in the response. Use to filter, limit the size of, and sort the data in an API response.

For most REST `GET` calls, you can specify one or more optional query parameters on the request URI to Filter, Limit, and Sort the data in an API response. For filter parameters, see the individual `GET` calls.

## Pagination

```
curl -X GET \
  'https://api.point.red/api/v1/master/groups?group_type=customer&limit=20&page=1' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer <access_token>' \
  -H 'Content-Type: application/json' \
```

> Response

```
"data": {
    ...
},
"links": {
    "first": "https://api.point.red/api/v1/master/groups?page=1",
    "last": "https://api.point.red/api/v1/master/groups?page=3",
    "prev": null,
    "next": "https://api.point.red/api/v1/master/groups?page=2"
},
"meta": {
    "current_page": 1,
    "from": 1,
    "last_page": 3,
    "path": "https://api.point.red/api/v1/master/groups",
    "per_page": "20",
    "to": 2,
    "total": 53
}
```

The JSON from the paginator will include meta information such as total, current_page,  last_page, and more. The actual result objects will be available via the data key in the JSON array. 

Paginated responses always contain meta and links keys with information about the paginator's state:

| Response Variable | Type   | Description                            |
| ----------------- | ------ | -------------------------------------- |
| first             | string | The first page of pagination           |
| last              | string | The last page of pagination            |
| prev              | string | The previous page of pagination        |
| next              | string | The next page of pagination            |
| current_page      | int    | Current page                           |
| from              | int    | Data row start from                          |
| last_page         | int    | Number of available page of pagination |
| path              | string | URI of pagination                      |
| per_page          | int    | Number of row per page                 |
| to                | int    | Data row until                          |
| total             | int    | Total data                             |


<aside class="notice">
Not all pagination parameters are available for all APIs
</aside>
