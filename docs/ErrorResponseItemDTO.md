# ErrorResponseItemDTO

Lista de objetos

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** | Código do erro | [optional] 
**description** | **str** | Descrição do erro | [optional] 

## Example

```python
from asaas.models.error_response_item_dto import ErrorResponseItemDTO

# TODO update the JSON string below
json = "{}"
# create an instance of ErrorResponseItemDTO from a JSON string
error_response_item_dto_instance = ErrorResponseItemDTO.from_json(json)
# print the JSON string representation of the object
print(ErrorResponseItemDTO.to_json())

# convert the object into a dict
error_response_item_dto_dict = error_response_item_dto_instance.to_dict()
# create an instance of ErrorResponseItemDTO from a dict
error_response_item_dto_from_dict = ErrorResponseItemDTO.from_dict(error_response_item_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


