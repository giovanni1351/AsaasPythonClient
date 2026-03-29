# MyAccountDisableAccountResponseDTO

## Properties

| Name             | Type    | Description                  | Notes      |
| ---------------- | ------- | ---------------------------- | ---------- |
| **observations** | **str** | Informações sobre a exclusão | [optional] |

## Example

```python
from asaas.models.my_account_disable_account_response_dto import MyAccountDisableAccountResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountDisableAccountResponseDTO from a JSON string
my_account_disable_account_response_dto_instance = MyAccountDisableAccountResponseDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountDisableAccountResponseDTO.to_json())

# convert the object into a dict
my_account_disable_account_response_dto_dict = my_account_disable_account_response_dto_instance.to_dict()
# create an instance of MyAccountDisableAccountResponseDTO from a dict
my_account_disable_account_response_dto_from_dict = MyAccountDisableAccountResponseDTO.from_dict(my_account_disable_account_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
