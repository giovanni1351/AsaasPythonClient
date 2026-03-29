# FiscalInfoUpdateUseNationalPortalResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** | Estado da requisição para alteração da habilitação do uso do portal nacional para emissão de notas fiscais. | [optional] 

## Example

```python
from asaas.models.fiscal_info_update_use_national_portal_response_dto import FiscalInfoUpdateUseNationalPortalResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoUpdateUseNationalPortalResponseDTO from a JSON string
fiscal_info_update_use_national_portal_response_dto_instance = FiscalInfoUpdateUseNationalPortalResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoUpdateUseNationalPortalResponseDTO.to_json())

# convert the object into a dict
fiscal_info_update_use_national_portal_response_dto_dict = fiscal_info_update_use_national_portal_response_dto_instance.to_dict()
# create an instance of FiscalInfoUpdateUseNationalPortalResponseDTO from a dict
fiscal_info_update_use_national_portal_response_dto_from_dict = FiscalInfoUpdateUseNationalPortalResponseDTO.from_dict(fiscal_info_update_use_national_portal_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


