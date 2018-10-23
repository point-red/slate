## Get Access Token

```shell
curl -X POST \
  https://api.point.red/api/v1/auth/login \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'username=johndoe&password=mysecurepassword'
```

> Response

```json
{
    "data": {
        "id": 1,
        "name": "johndoe",
        "first_name": "John",
        "last_name": "Doe",
        "address": null,
        "phone": null,
        "email": "johndoe@gmail.com",
        "phone_confirmation_code": null,
        "phone_confirmed": 0,
        "email_confirmation_code": "eyJpdiI6IkVsaGhmdU5IbXpCNlRDU0",
        "email_confirmed": 0,
        "created_at": "2018-10-08 15:30:41",
        "updated_at": "2018-10-08 15:30:41",
        "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOPOSUzI1NiIsImp0aSI6ImY5M2U5YTY4ZmM4MjE4OTRhZGIwOTlhYWNhMGNkYzgyYzQ3MWVlMGZhYjJkYWEyOGIyMGJmZWM4YjU3ZGQWETg4OWIyNzA1MDU2ZTAyNzdjIn0.eyJhdWQiOiIxIiwianRpIjoiZjkzZTlhNjhmYzgyMTg5NGFkYjA5OWFhY2EwYDSjODJjNDcxZWUwZmFiMmRhYTI4YjIwYmZlYzhiNTdkY2Q5ODg5YjI3MDUwNTZlMDI3N2MiLCJpYXQiOjE1NDAyNTk3VDgsIm5iZiI6MTU0MDI1OTc0OCwiZXhwIjoxNTcxNzk1NzQ4LCJzdWIiOiIxIiwic2NvcGVzIjpbXX0.WKZ7_5qbP9MDCJY6eqTXYgBAZ8WYgOk6XeqaW289QYBQBP-SmtK3xIS44J-KgmLdw4bv0RcBJbK1KmSqhfKSSW6jDprkpDcaP4cSSFM02XBCgVFQJko2xq3MPyaS3xWzw3-tgLeX4w_SVSDIIdP7C82sJRVDlZ84qkzRQY3FSK78eYsNwkvdyAANi_XuHVH5USzAe_DPq-33Rwnl5NuL2WyiJ0sb6-5hco7V6vqMvQo9DXvDn49gtOUvfwqGtN_PrWNFMEDtxiWE0_RVgKqFj8PTcINTpiDvM9-Q9tb8j0B9__Xr5vGB8RdIVZaOyuMxIxIEqeCJRxPlMuZyYTrVwXQW0GktDhsjoEtXkqbA5BG3LycoyZXR0yyVSbZeGZ7QvZK50MFO9JG2X-58j0PUhD4DoyZnUSQx0X2zNlkZds3OAyxPK9OT-PJRO6BVhZ9rZWr2iiWWEWfDq8LivRIud0MG197T2jgvEU3Bd1tx5zDDw7ONSJl98ZhZPpWgKx7GX-7tDRr2rtRVVHig94zWCL5-YZagmoddIf9HxZh3_aq4IVSFh8GaW_ZaPVGLCu9ZTv04Y7Rj-mHCFN0VGz0E6e4AyPbXarG2XjQijiOrmtCic9ShUIDIBjVptC-oG4XoHysx-N1uNGk3W5sLBS7aFetVjSwYTHboMNdz1n1-B1s",
        "token_type": "Bearer",
        "token_id": "f93e9a68fc821894adb099aaca0cdc82c5r1ee0fab2daa28b20bfec8b57dcd9889b0215056e0277c",
        "token_expires_in": 1571795748
    }
}
```

Get Access Token.

### HTTP Request

`POST http://api.point.red/api/v1/auth/login`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
username *(required)* | string | Your username
password *(required)* | string | Your password