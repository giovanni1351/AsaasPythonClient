# InstallmentDeleteResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted** | **bool** | Indica se o parcelamento está removido | [optional] 
**id** | **str** | Identificador único do parcelamento no Asaas | [optional] 

## Example

```python
from asaas.models.installment_delete_response_dto import InstallmentDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentDeleteResponseDTO from a JSON string
installment_delete_response_dto_instance = InstallmentDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentDeleteResponseDTO.to_json())

# convert the object into a dict
installment_delete_response_dto_dict = installment_delete_response_dto_instance.to_dict()
# create an instance of InstallmentDeleteResponseDTO from a dict
installment_delete_response_dto_from_dict = InstallmentDeleteResponseDTO.from_dict(installment_delete_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


