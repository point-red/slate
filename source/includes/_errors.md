# Errors

The Point API uses the following error codes:

Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your <access_token> is wrong.
403 | Forbidden -- The endpoint requested is hidden for administrators only.
404 | Not Found -- The specified endpoint could not be found.
405 | Method Not Allowed -- Invalid method.
406 | Not Acceptable -- You requested a format that isn't valid.
422 | Validation Failed -- Your request not is valid.
429 | Too Many Requests -- You're requesting too much! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
