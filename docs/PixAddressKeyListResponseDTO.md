# PixAddressKeyListResponseDTO

## Properties

| Name     | Type                                                                    | Description      | Notes      |
| -------- | ----------------------------------------------------------------------- | ---------------- | ---------- |
| **data** | [**List[PixAddressKeyGetResponseDTO]**](PixAddressKeyGetResponseDTO.md) | Lista de objetos | [optional] |

## Example

```python
from asaas.models.pix_address_key_list_response_dto import PixAddressKeyListResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixAddressKeyListResponseDTO from a JSON string
pix_address_key_list_response_dto_instance = PixAddressKeyListResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixAddressKeyListResponseDTO.to_json())

# convert the object into a dict
pix_address_key_list_response_dto_dict = pix_address_key_list_response_dto_instance.to_dict()
# create an instance of PixAddressKeyListResponseDTO from a dict
pix_address_key_list_response_dto_from_dict = PixAddressKeyListResponseDTO.from_dict(pix_address_key_list_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
