# CustomerDeleteResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted** | **bool** | Indica se o cliente foi removido | [optional] 
**id** | **str** | Identificador único do cliente | [optional] 

## Example

```python
from asaas.models.customer_delete_response_dto import CustomerDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerDeleteResponseDTO from a JSON string
customer_delete_response_dto_instance = CustomerDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CustomerDeleteResponseDTO.to_json())

# convert the object into a dict
customer_delete_response_dto_dict = customer_delete_response_dto_instance.to_dict()
# create an instance of CustomerDeleteResponseDTO from a dict
customer_delete_response_dto_from_dict = CustomerDeleteResponseDTO.from_dict(customer_delete_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


