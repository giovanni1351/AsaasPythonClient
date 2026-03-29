# FiscalInfoListMunicipalServicesResponseDataDTO

Lista de objetos

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único do serviço | [optional] 
**description** | **str** | Descrição do serviço | [optional] 
**iss_tax** | **float** | Taxa percentual do ISS | [optional] 

## Example

```python
from asaas.models.fiscal_info_list_municipal_services_response_data_dto import FiscalInfoListMunicipalServicesResponseDataDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoListMunicipalServicesResponseDataDTO from a JSON string
fiscal_info_list_municipal_services_response_data_dto_instance = FiscalInfoListMunicipalServicesResponseDataDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoListMunicipalServicesResponseDataDTO.to_json())

# convert the object into a dict
fiscal_info_list_municipal_services_response_data_dto_dict = fiscal_info_list_municipal_services_response_data_dto_instance.to_dict()
# create an instance of FiscalInfoListMunicipalServicesResponseDataDTO from a dict
fiscal_info_list_municipal_services_response_data_dto_from_dict = FiscalInfoListMunicipalServicesResponseDataDTO.from_dict(fiscal_info_list_municipal_services_response_data_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


