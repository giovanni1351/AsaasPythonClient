# CustomerApiAccessTokenListResponseDTO

## Properties

| Name              | Type                                                                                        | Description                        | Notes      |
| ----------------- | ------------------------------------------------------------------------------------------- | ---------------------------------- | ---------- |
| **access_tokens** | [**List[CustomerApiAccessTokenBaseResponseDTO]**](CustomerApiAccessTokenBaseResponseDTO.md) | Lista de chaves de API da subconta | [optional] |

## Example

```python
from asaas.models.customer_api_access_token_list_response_dto import CustomerApiAccessTokenListResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerApiAccessTokenListResponseDTO from a JSON string
customer_api_access_token_list_response_dto_instance = CustomerApiAccessTokenListResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CustomerApiAccessTokenListResponseDTO.to_json())

# convert the object into a dict
customer_api_access_token_list_response_dto_dict = customer_api_access_token_list_response_dto_instance.to_dict()
# create an instance of CustomerApiAccessTokenListResponseDTO from a dict
customer_api_access_token_list_response_dto_from_dict = CustomerApiAccessTokenListResponseDTO.from_dict(customer_api_access_token_list_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
