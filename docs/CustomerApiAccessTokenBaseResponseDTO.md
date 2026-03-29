# CustomerApiAccessTokenBaseResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | ID da chave de API | [optional] 
**name** | **str** | Nome da chave de API | [optional] 
**enabled** | **bool** | Indica se a chave de API está habilitada | [optional] 
**expiration_date** | **datetime** | Data de expiração da chave de API | [optional] 
**date_created** | **datetime** | Data de criação da chave de API | [optional] 
**projected_expiration_date_by_lack_of_use** | **date** | Data prevista de expiração por falta de uso da chave de API | [optional] 

## Example

```python
from asaas.models.customer_api_access_token_base_response_dto import CustomerApiAccessTokenBaseResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerApiAccessTokenBaseResponseDTO from a JSON string
customer_api_access_token_base_response_dto_instance = CustomerApiAccessTokenBaseResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CustomerApiAccessTokenBaseResponseDTO.to_json())

# convert the object into a dict
customer_api_access_token_base_response_dto_dict = customer_api_access_token_base_response_dto_instance.to_dict()
# create an instance of CustomerApiAccessTokenBaseResponseDTO from a dict
customer_api_access_token_base_response_dto_from_dict = CustomerApiAccessTokenBaseResponseDTO.from_dict(customer_api_access_token_base_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


