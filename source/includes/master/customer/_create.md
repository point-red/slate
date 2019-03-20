## Create Customer

```shell
curl -X POST \
  https://api.point.red/api/v1/master/customers \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer <access_token>' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'name=<name>'
```

> Response

```json
{
    "data": {
        "id": 1,
        "name": "John Doe",
        "updated_at": "2018-10-22 06:14:27",
        "created_at": "2018-10-22 06:14:27",
        "updated_by": 1,
        "created_by": 1,
        "pricing_group_id": 1, 
    }
}
```

Create a Customer.

### HTTP Request

`POST http://api.point.red/api/v1/master/customers`

### URL Parameters

Parameter                              | Type        | Description
-------------------------------------- | ----------- | -----------
name *(required)*                      | string      |
code *(optional)*                      | string      |
tax_identification_number *(optional)* | string      |
notes *(optional)*                     | string      |
credit_ceiling *(optional)*            | decimal     |
pricing_group_id *(optional)*          | integer     |
disabled *(optional)*                  | boolean     |
group *(optional)*                     | object      | required attribute `id` or `name`
addresses *(optional)*                 | array       | array of [Address](https://address.com)
phones *(optional)*                    | array       | array of [Phones](https://phones.com)
emails *(optional)*                    | array       | array of [Emails](https://emails.com)
contacts *(optional)*                  | array       | array of [Contacts](https://contacts.com)
banks *(optional)*                     | array       | array of [Banks](https://banks.com)

##### Additional Notes
- `group={id: 1}`<br>
Inserts customer to group with `group.id=1`.
- `group={name:'Gold Member'}`<br>
If group with name `Gold Member` doesn't exist, create it.<br>
Inserts customer to group with `group.name=Gold Member`.