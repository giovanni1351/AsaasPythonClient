# MobilePhoneRechargeFindProviderResponseDTO

## Properties

| Name       | Type                                                                                                              | Description                      | Notes      |
| ---------- | ----------------------------------------------------------------------------------------------------------------- | -------------------------------- | ---------- |
| **name**   | **str**                                                                                                           | Nome da operadora do celular     | [optional] |
| **values** | [**List[MobilePhoneRechargeFindProviderResponseValuesDTO]**](MobilePhoneRechargeFindProviderResponseValuesDTO.md) | Valores disponíveis para recarga | [optional] |

## Example

```python
from asaas.models.mobile_phone_recharge_find_provider_response_dto import MobilePhoneRechargeFindProviderResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MobilePhoneRechargeFindProviderResponseDTO from a JSON string
mobile_phone_recharge_find_provider_response_dto_instance = MobilePhoneRechargeFindProviderResponseDTO.from_json(json)
# print the JSON string representation of the object
print(MobilePhoneRechargeFindProviderResponseDTO.to_json())

# convert the object into a dict
mobile_phone_recharge_find_provider_response_dto_dict = mobile_phone_recharge_find_provider_response_dto_instance.to_dict()
# create an instance of MobilePhoneRechargeFindProviderResponseDTO from a dict
mobile_phone_recharge_find_provider_response_dto_from_dict = MobilePhoneRechargeFindProviderResponseDTO.from_dict(mobile_phone_recharge_find_provider_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
