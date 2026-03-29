# MobilePhoneRechargeGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único da recarga de celular no Asaas | [optional] 
**value** | **float** | Valor da recarga | [optional] 
**phone_number** | **str** | Número do celular que foi solicitado a recarga | [optional] 
**status** | [**MobilePhoneRechargeGetResponseMobilePhoneRechargeStatus**](MobilePhoneRechargeGetResponseMobilePhoneRechargeStatus.md) |  | [optional] 
**can_be_cancelled** | **bool** | Se a recarga pode ser cancelada | [optional] [default to True]
**operator_name** | **str** | Nome da operadora do celular | [optional] 

## Example

```python
from asaas.models.mobile_phone_recharge_get_response_dto import MobilePhoneRechargeGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MobilePhoneRechargeGetResponseDTO from a JSON string
mobile_phone_recharge_get_response_dto_instance = MobilePhoneRechargeGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(MobilePhoneRechargeGetResponseDTO.to_json())

# convert the object into a dict
mobile_phone_recharge_get_response_dto_dict = mobile_phone_recharge_get_response_dto_instance.to_dict()
# create an instance of MobilePhoneRechargeGetResponseDTO from a dict
mobile_phone_recharge_get_response_dto_from_dict = MobilePhoneRechargeGetResponseDTO.from_dict(mobile_phone_recharge_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


