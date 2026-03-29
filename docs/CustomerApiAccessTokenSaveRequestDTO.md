# CustomerApiAccessTokenSaveRequestDTO

## Properties

| Name                | Type         | Description                       | Notes      |
| ------------------- | ------------ | --------------------------------- | ---------- |
| **name**            | **str**      | Nome da chave de API              | [optional] |
| **expiration_date** | **datetime** | Data de expiração da chave de API | [optional] |

## Example

```python
from asaas.models.customer_api_access_token_save_request_dto import CustomerApiAccessTokenSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerApiAccessTokenSaveRequestDTO from a JSON string
customer_api_access_token_save_request_dto_instance = CustomerApiAccessTokenSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(CustomerApiAccessTokenSaveRequestDTO.to_json())

# convert the object into a dict
customer_api_access_token_save_request_dto_dict = customer_api_access_token_save_request_dto_instance.to_dict()
# create an instance of CustomerApiAccessTokenSaveRequestDTO from a dict
customer_api_access_token_save_request_dto_from_dict = CustomerApiAccessTokenSaveRequestDTO.from_dict(customer_api_access_token_save_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
