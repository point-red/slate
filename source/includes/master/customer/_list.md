## Get Customer

```shell
curl -X GET \
  'https://api.point.red/api/v1/master/customers' \
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
            "code": "AAPL",
            "tax_identification_number": "38.704.149.0-603.802",
            "name": "Apple Inc",
            "notes": "Apple Inc. is an American multinational technology company headquartered in Cupertino, California, that designs, develops, and sells consumer electronics, computer software, and online services. It is considered one of the Big Four of technology along with Amazon, Google, and Facebook",
            "disabled": 0,
            "credit_ceiling": 2000000,
            "created_by": null,
            "updated_by": null,
            "pricing_group_id": 1,
            "created_at": "2019-03-18 03:28:06",
            "updated_at": "2019-03-18 03:28:06"
        },
        {
            "id": 2,
            "code": "MCD",
            "tax_identification_number": "94.757.767.9-896.672",
            "name": "McDonald's Corporation",
            "notes": "McDonald's is the world's largest restaurant chain by revenue, serving over 69 million customers daily in over 100 countries across 37,855 outlets as of 2018.",
            "disabled": 0,
            "credit_ceiling": 0,
            "created_by": null,
            "updated_by": null,
            "pricing_group_id": 2,
            "created_at": "2019-03-18 03:28:06",
            "updated_at": "2019-03-18 03:28:06"
        },
    ]
}
```

List Customer.

### HTTP Request

`GET http://api.point.red/api/v1/master/customers`

### Relations

Relation Name  | References                                   
-------------- | ---------------------------------------------
groups         | [Groups](https://groups.com)
contactPersons | [Contact Persons](https://contactPersons.com)
addresses      | [Addresses](https://addresses.com)
phones         | [Phones](https://phones.com)
emails         | [Emails](https://emails.com)
banks          | [Banks](https://banks.com)  
journals       | [Journals](https://journals.com) 
pricingGroup   | [Pricing Group](https://pricingGroup.com)
payments       | [Payments](https://payments.com)
