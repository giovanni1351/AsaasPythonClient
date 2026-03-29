# FiscalInfoOperationIndicatorCodeResponseDTO

Lista de objetos

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** | Código do indicador da operação | [optional] 
**description** | **str** | Descrição | [optional] 

## Example

```python
from asaas.models.fiscal_info_operation_indicator_code_response_dto import FiscalInfoOperationIndicatorCodeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoOperationIndicatorCodeResponseDTO from a JSON string
fiscal_info_operation_indicator_code_response_dto_instance = FiscalInfoOperationIndicatorCodeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoOperationIndicatorCodeResponseDTO.to_json())

# convert the object into a dict
fiscal_info_operation_indicator_code_response_dto_dict = fiscal_info_operation_indicator_code_response_dto_instance.to_dict()
# create an instance of FiscalInfoOperationIndicatorCodeResponseDTO from a dict
fiscal_info_operation_indicator_code_response_dto_from_dict = FiscalInfoOperationIndicatorCodeResponseDTO.from_dict(fiscal_info_operation_indicator_code_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


