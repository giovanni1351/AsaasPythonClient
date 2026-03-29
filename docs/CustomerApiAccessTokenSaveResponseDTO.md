# CustomerApiAccessTokenSaveResponseDTO

## Properties

| Name                                         | Type         | Description                                                 | Notes      |
| -------------------------------------------- | ------------ | ----------------------------------------------------------- | ---------- |
| **id**                                       | **str**      | ID da chave de API                                          | [optional] |
| **name**                                     | **str**      | Nome da chave de API                                        | [optional] |
| **enabled**                                  | **bool**     | Indica se a chave de API está habilitada                    | [optional] |
| **expiration_date**                          | **datetime** | Data de expiração da chave de API                           | [optional] |
| **date_created**                             | **datetime** | Data de criação da chave de API                             | [optional] |
| **projected_expiration_date_by_lack_of_use** | **date**     | Data prevista de expiração por falta de uso da chave de API | [optional] |
| **api_key**                                  | **str**      | Chave de API                                                | [optional] |

## Example

```python
from asaas.models.customer_api_access_token_save_response_dto import CustomerApiAccessTokenSaveResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerApiAccessTokenSaveResponseDTO from a JSON string
customer_api_access_token_save_response_dto_instance = CustomerApiAccessTokenSaveResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CustomerApiAccessTokenSaveResponseDTO.to_json())

# convert the object into a dict
customer_api_access_token_save_response_dto_dict = customer_api_access_token_save_response_dto_instance.to_dict()
# create an instance of CustomerApiAccessTokenSaveResponseDTO from a dict
customer_api_access_token_save_response_dto_from_dict = CustomerApiAccessTokenSaveResponseDTO.from_dict(customer_api_access_token_save_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
