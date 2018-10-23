# API Response

Point API calls return HTTP status codes. Some API calls also return JSON response bodies that include information about the resource including one or more contextual HATEOAS links. Use these links to request more information about and construct an API flow that is relative to a specific request.

## HTTP status codes

Each REST API request returns a success or error HTTP status code.

### Success

In the responses, Point returns these HTTP status codes for successful requests:

| Status code      | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
| `200 OK`         | The request succeeded.                                       |
| `201 Created`    | A `POST` method successfully created a resource. If the resource was already created by a previous execution of the same method, for example, the server returns the HTTP `200 OK` status code. |
| `202 Accepted`   | The server accepted the request and will execute it later.   |
| `204 No Content` | The server successfully executed the method but returns no response body. |

### Error

In the responses for failed requests, Point returns HTTP 4XX or 5XX status codes.

For all errors except Identity errors, Point returns an error response body that includes additional error details in this format.

| HTTP status code                   | Typical error code and error message                         | Cause                                                        |
| ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `400 Bad Request`                  | `INVALID_REQUEST`. Request is not well-formed, syntactically incorrect, or violates schema. | The server could not understand the request. Indicates one of these conditions: The API cannot convert the payload data to the underlying data type. The data is not in the expected data format.A required field is not available. A simple data validation error occurred. |
| `401 Unauthorized`                 | `AUTHENTICATION_FAILURE`. Authentication failed due to invalid authentication credentials. | The request requires authentication and the caller did not provide valid credentials. |
| `403 Forbidden`                    | `NOT_AUTHORIZED`. Authorization failed due to insufficient permissions. | The client is not authorized to access this resource although it might have valid credentials. For example, the client does not have the correct OAuth 2 scope. Additionally, a business-level authorization error might have occurred. For example, the account holder does not have sufficient funds. |
| `404 Not Found`                    | `RESOURCE_NOT_FOUND`. The specified resource does not exist. | The server did not find anything that matches the request URI. Either the URI is incorrect or the resource is not available. For example, no data exists in the database at that key. |
| `405 Method Not Allowed`           | `METHOD_NOT_SUPPORTED`. The server does not implement the requested HTTP method. | The service does not support the requested HTTP method. For example, `PATCH`. |
| `406 Not Acceptable`               | `MEDIA_TYPE_NOT_ACCEPTABLE`. The server does not implement the media type that would be acceptable to the client. | The server cannot use the client-request media type to return the response payload. For example, this error occurs if the client sends an `Accept: application/xml`request header but the API can generate only an `application/json` response. |
| `415` `Unsupported` `Media` `Type` | `UNSUPPORTED_MEDIA_TYPE`. The server does not support the request payload’s media type. | The API cannot process the media type of the request payload. For example, this error occurs if the client sends a `Content-Type: application/xml`request header but the API can only accept `application/json` request payloads. |
| `422 Unprocessable Entity`         | `UNPROCCESSABLE_ENTITY`. The API cannot complete the requested action, or the request action is semantically incorrect or fails business validation. | The API cannot complete the requested action and might require interaction with APIs or processes outside of the current request. No systemic problems limit the API from completing the request. For example, this error occurs for any business validation errors, including errors that are not usually of the `400` type. |
| `429 Unprocessable Entity`         | `RATE_LIMIT_REACHED`. Too many requests. Blocked due to rate limiting. | The rate limit for the user, application, or token exceeds a predefined value. |
| `500 Internal Server Error`        | `INTERNAL_SERVER_ERROR`. An internal server error has occurred. | A system or application error occurred. Although the client appears to provide a correct request, something unexpected occurred on the server. |
| `503 Service Unavailable`          | `SERVICE_UNAVAILABLE`. Service Unavailable.                  | The server cannot handle the request for a service due to temporary maintenance. |