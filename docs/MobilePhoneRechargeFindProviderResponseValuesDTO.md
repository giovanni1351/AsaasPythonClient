# MobilePhoneRechargeFindProviderResponseValuesDTO

Valores disponíveis para recarga

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Nome do pacote | [optional] 
**description** | **str** | Descrição do pacote | [optional] 
**bonus** | **str** | Bônus do pacote | [optional] 
**min_value** | **float** | Valor mínimo de recarga | [optional] 
**max_value** | **float** | Valor máximo de recarga | [optional] 

## Example

```python
from asaas.models.mobile_phone_recharge_find_provider_response_values_dto import MobilePhoneRechargeFindProviderResponseValuesDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MobilePhoneRechargeFindProviderResponseValuesDTO from a JSON string
mobile_phone_recharge_find_provider_response_values_dto_instance = MobilePhoneRechargeFindProviderResponseValuesDTO.from_json(json)
# print the JSON string representation of the object
print(MobilePhoneRechargeFindProviderResponseValuesDTO.to_json())

# convert the object into a dict
mobile_phone_recharge_find_provider_response_values_dto_dict = mobile_phone_recharge_find_provider_response_values_dto_instance.to_dict()
# create an instance of MobilePhoneRechargeFindProviderResponseValuesDTO from a dict
mobile_phone_recharge_find_provider_response_values_dto_from_dict = MobilePhoneRechargeFindProviderResponseValuesDTO.from_dict(mobile_phone_recharge_find_provider_response_values_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


