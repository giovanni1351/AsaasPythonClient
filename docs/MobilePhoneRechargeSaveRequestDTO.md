# MobilePhoneRechargeSaveRequestDTO

## Properties

| Name             | Type      | Description       | Notes |
| ---------------- | --------- | ----------------- | ----- |
| **value**        | **float** | Valor da recarga  |
| **phone_number** | **str**   | Número do celular |

## Example

```python
from asaas.models.mobile_phone_recharge_save_request_dto import MobilePhoneRechargeSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MobilePhoneRechargeSaveRequestDTO from a JSON string
mobile_phone_recharge_save_request_dto_instance = MobilePhoneRechargeSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(MobilePhoneRechargeSaveRequestDTO.to_json())

# convert the object into a dict
mobile_phone_recharge_save_request_dto_dict = mobile_phone_recharge_save_request_dto_instance.to_dict()
# create an instance of MobilePhoneRechargeSaveRequestDTO from a dict
mobile_phone_recharge_save_request_dto_from_dict = MobilePhoneRechargeSaveRequestDTO.from_dict(mobile_phone_recharge_save_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
