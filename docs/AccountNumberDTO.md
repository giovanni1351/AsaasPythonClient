# AccountNumberDTO

Subaccount number in Asaas

## Properties

| Name              | Type    | Description    | Notes      |
| ----------------- | ------- | -------------- | ---------- |
| **agency**        | **str** | Account agency | [optional] |
| **account**       | **str** | Account number | [optional] |
| **account_digit** | **str** | Account digit  | [optional] |

## Example

```python
from asaas.models.account_number_dto import AccountNumberDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountNumberDTO from a JSON string
account_number_dto_instance = AccountNumberDTO.from_json(json)
# print the JSON string representation of the object
print(AccountNumberDTO.to_json())

# convert the object into a dict
account_number_dto_dict = account_number_dto_instance.to_dict()
# create an instance of AccountNumberDTO from a dict
account_number_dto_from_dict = AccountNumberDTO.from_dict(account_number_dto_dict)
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
