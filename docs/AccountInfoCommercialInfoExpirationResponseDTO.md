# AccountInfoCommercialInfoExpirationResponseDTO

Informações sobre a expiração dos dados comerciais

## Properties

| Name               | Type         | Description                                      | Notes      |
| ------------------ | ------------ | ------------------------------------------------ | ---------- |
| **is_expired**     | **bool**     | Informa se os dados comerciais estão expirados   | [optional] |
| **scheduled_date** | **datetime** | Informa a data de expiração dos dados comerciais | [optional] |

## Example

```python
from asaas.models.account_info_commercial_info_expiration_response_dto import AccountInfoCommercialInfoExpirationResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountInfoCommercialInfoExpirationResponseDTO from a JSON string
account_info_commercial_info_expiration_response_dto_instance = AccountInfoCommercialInfoExpirationResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AccountInfoCommercialInfoExpirationResponseDTO.to_json())

# convert the object into a dict
account_info_commercial_info_expiration_response_dto_dict = account_info_commercial_info_expiration_response_dto_instance.to_dict()
# create an instance of AccountInfoCommercialInfoExpirationResponseDTO from a dict
account_info_commercial_info_expiration_response_dto_from_dict = AccountInfoCommercialInfoExpirationResponseDTO.from_dict(account_info_commercial_info_expiration_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
