# InstallmentUpdateSplitResponseDTO

## Properties

| Name       | Type                                                                          | Description     | Notes      |
| ---------- | ----------------------------------------------------------------------------- | --------------- | ---------- |
| **splits** | [**List[InstallmentSplitGetResponseDTO]**](InstallmentSplitGetResponseDTO.md) | Array de splits | [optional] |

## Example

```python
from asaas.models.installment_update_split_response_dto import InstallmentUpdateSplitResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentUpdateSplitResponseDTO from a JSON string
installment_update_split_response_dto_instance = InstallmentUpdateSplitResponseDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentUpdateSplitResponseDTO.to_json())

# convert the object into a dict
installment_update_split_response_dto_dict = installment_update_split_response_dto_instance.to_dict()
# create an instance of InstallmentUpdateSplitResponseDTO from a dict
installment_update_split_response_dto_from_dict = InstallmentUpdateSplitResponseDTO.from_dict(installment_update_split_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
