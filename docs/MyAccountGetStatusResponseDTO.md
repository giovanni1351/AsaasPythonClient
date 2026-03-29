# MyAccountGetStatusResponseDTO

## Properties

| Name                  | Type                                                                        | Description                           | Notes      |
| --------------------- | --------------------------------------------------------------------------- | ------------------------------------- | ---------- |
| **id**                | **str**                                                                     | Identificador único da conta no Asaas | [optional] |
| **commercial_info**   | [**MyAccountGetStatusResponseStatus**](MyAccountGetStatusResponseStatus.md) |                                       | [optional] |
| **bank_account_info** | [**MyAccountGetStatusResponseStatus**](MyAccountGetStatusResponseStatus.md) |                                       | [optional] |
| **documentation**     | [**MyAccountGetStatusResponseStatus**](MyAccountGetStatusResponseStatus.md) |                                       | [optional] |
| **general**           | [**MyAccountGetStatusResponseStatus**](MyAccountGetStatusResponseStatus.md) |                                       | [optional] |

## Example

```python
from asaas.models.my_account_get_status_response_dto import MyAccountGetStatusResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetStatusResponseDTO from a JSON string
my_account_get_status_response_dto_instance = MyAccountGetStatusResponseDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetStatusResponseDTO.to_json())

# convert the object into a dict
my_account_get_status_response_dto_dict = my_account_get_status_response_dto_instance.to_dict()
# create an instance of MyAccountGetStatusResponseDTO from a dict
my_account_get_status_response_dto_from_dict = MyAccountGetStatusResponseDTO.from_dict(my_account_get_status_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
