# InstallmentUpdateSplitRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**splits** | [**List[InstallmentSplitRequestDTO]**](InstallmentSplitRequestDTO.md) | Dados de split para atualizar | [optional] 

## Example

```python
from asaas.models.installment_update_split_request_dto import InstallmentUpdateSplitRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentUpdateSplitRequestDTO from a JSON string
installment_update_split_request_dto_instance = InstallmentUpdateSplitRequestDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentUpdateSplitRequestDTO.to_json())

# convert the object into a dict
installment_update_split_request_dto_dict = installment_update_split_request_dto_instance.to_dict()
# create an instance of InstallmentUpdateSplitRequestDTO from a dict
installment_update_split_request_dto_from_dict = InstallmentUpdateSplitRequestDTO.from_dict(installment_update_split_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


