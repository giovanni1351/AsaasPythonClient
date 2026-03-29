# CustomerApiAccessTokenUpdateRequestDTO

## Properties

| Name                | Type         | Description                              | Notes |
| ------------------- | ------------ | ---------------------------------------- | ----- |
| **name**            | **str**      | Nome da chave de API                     |
| **enabled**         | **bool**     | Indica se a chave de API está habilitada |
| **expiration_date** | **datetime** | Data de expiração da chave de API        |

## Example

```python
from asaas.models.customer_api_access_token_update_request_dto import CustomerApiAccessTokenUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerApiAccessTokenUpdateRequestDTO from a JSON string
customer_api_access_token_update_request_dto_instance = CustomerApiAccessTokenUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(CustomerApiAccessTokenUpdateRequestDTO.to_json())

# convert the object into a dict
customer_api_access_token_update_request_dto_dict = customer_api_access_token_update_request_dto_instance.to_dict()
# create an instance of CustomerApiAccessTokenUpdateRequestDTO from a dict
customer_api_access_token_update_request_dto_from_dict = CustomerApiAccessTokenUpdateRequestDTO.from_dict(customer_api_access_token_update_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
