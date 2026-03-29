# MyAccountGetAccountNumberResponseDTO

## Properties

| Name              | Type    | Description      | Notes      |
| ----------------- | ------- | ---------------- | ---------- |
| **agency**        | **str** | Agência da conta | [optional] |
| **account**       | **str** | Número da conta  | [optional] |
| **account_digit** | **str** | Dígito da conta  | [optional] |

## Example

```python
from asaas.models.my_account_get_account_number_response_dto import MyAccountGetAccountNumberResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountNumberResponseDTO from a JSON string
my_account_get_account_number_response_dto_instance = MyAccountGetAccountNumberResponseDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountNumberResponseDTO.to_json())

# convert the object into a dict
my_account_get_account_number_response_dto_dict = my_account_get_account_number_response_dto_instance.to_dict()
# create an instance of MyAccountGetAccountNumberResponseDTO from a dict
my_account_get_account_number_response_dto_from_dict = MyAccountGetAccountNumberResponseDTO.from_dict(my_account_get_account_number_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
