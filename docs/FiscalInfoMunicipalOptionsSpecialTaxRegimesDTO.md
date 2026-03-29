# FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO

Opções de regime especial de tributação

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **str** | Nome do regime especial de tributação | [optional] 
**value** | **str** | Identificador do regime especial de tributação | [optional] 

## Example

```python
from asaas.models.fiscal_info_municipal_options_special_tax_regimes_dto import FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO from a JSON string
fiscal_info_municipal_options_special_tax_regimes_dto_instance = FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO.to_json())

# convert the object into a dict
fiscal_info_municipal_options_special_tax_regimes_dto_dict = fiscal_info_municipal_options_special_tax_regimes_dto_instance.to_dict()
# create an instance of FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO from a dict
fiscal_info_municipal_options_special_tax_regimes_dto_from_dict = FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO.from_dict(fiscal_info_municipal_options_special_tax_regimes_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


