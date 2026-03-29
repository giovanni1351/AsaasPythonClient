# FiscalInfoMunicipalOptionsGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authentication_type** | [**FiscalInfoMunicipalOptionsGetResponseEnotasTipoAutenticacao**](FiscalInfoMunicipalOptionsGetResponseEnotasTipoAutenticacao.md) |  | [optional] 
**supports_cancellation** | **bool** | Suporta ou não o cancelamento de notas fiscais automaticamente na sua prefeitura | [optional] [default to True]
**uses_special_tax_regimes** | **bool** | Necessário informar ou não o regime especial de tributação. Caso utilize, informe-o no campo &#x60;specialTaxRegime&#x60; do **Criar ou atualizar informações fiscais** de acordo com as opções retornadas na lista &#x60;specialTaxRegimesList&#x60; | [optional] [default to True]
**uses_service_list_item** | **bool** | Necessário informar ou não o item da lista de serviço | [optional] [default to True]
**special_tax_regimes_list** | [**List[FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO]**](FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO.md) | Opções de regime especial de tributação | [optional] 
**national_portal_tax_calculation_regime_list** | [**List[FiscalInfoMunicipalOptionsNationalPortalTaxCalculationRegimeDTO]**](FiscalInfoMunicipalOptionsNationalPortalTaxCalculationRegimeDTO.md) | Opções de regime de apuração tributária pelo Simples Nacional | [optional] 
**national_portal_tax_calculation_regime_help** | **str** | Explicação sobre o regime de apuração tributária pelo Simples Nacional | [optional] 
**municipal_inscription_help** | **str** | Explicação sobre formato da inscrição municipal | [optional] 
**special_tax_regime_help** | **str** | Explicação sobre o regime especial de tributação | [optional] 
**service_list_item_help** | **str** | Explicação sobre formato do item da lista de serviço | [optional] 
**digital_certificated_help** | **str** | Explicação sobre certificado digital | [optional] 
**access_token_help** | **str** | Explicação sobre token | [optional] 
**municipal_service_code_help** | **str** | Explicação sobre formato do código de serviço municipal | [optional] 

## Example

```python
from asaas.models.fiscal_info_municipal_options_get_response_dto import FiscalInfoMunicipalOptionsGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoMunicipalOptionsGetResponseDTO from a JSON string
fiscal_info_municipal_options_get_response_dto_instance = FiscalInfoMunicipalOptionsGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoMunicipalOptionsGetResponseDTO.to_json())

# convert the object into a dict
fiscal_info_municipal_options_get_response_dto_dict = fiscal_info_municipal_options_get_response_dto_instance.to_dict()
# create an instance of FiscalInfoMunicipalOptionsGetResponseDTO from a dict
fiscal_info_municipal_options_get_response_dto_from_dict = FiscalInfoMunicipalOptionsGetResponseDTO.from_dict(fiscal_info_municipal_options_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


