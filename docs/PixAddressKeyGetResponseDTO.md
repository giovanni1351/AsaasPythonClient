# PixAddressKeyGetResponseDTO

## Properties

| Name                         | Type                                                                                              | Description                               | Notes      |
| ---------------------------- | ------------------------------------------------------------------------------------------------- | ----------------------------------------- | ---------- |
| **id**                       | **str**                                                                                           | Identificador único da chave Pix no Asaas | [optional] |
| **key**                      | **str**                                                                                           | Valor da chave                            | [optional] |
| **type**                     | [**PixAddressKeyGetResponsePixAddressKeyType**](PixAddressKeyGetResponsePixAddressKeyType.md)     |                                           | [optional] |
| **status**                   | [**PixAddressKeyGetResponsePixAddressKeyStatus**](PixAddressKeyGetResponsePixAddressKeyStatus.md) |                                           | [optional] |
| **date_created**             | **datetime**                                                                                      | Data de criação da chave                  | [optional] |
| **can_be_deleted**           | **bool**                                                                                          | Determina se a chave pode ser deletada    | [optional] |
| **cannot_be_deleted_reason** | **str**                                                                                           | Motivo de não poder ser removida          | [optional] |
| **qr_code**                  | [**PixAddressKeyQrCodeGetResponseDTO**](PixAddressKeyQrCodeGetResponseDTO.md)                     |                                           | [optional] |

## Example

```python
from asaas.models.pix_address_key_get_response_dto import PixAddressKeyGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixAddressKeyGetResponseDTO from a JSON string
pix_address_key_get_response_dto_instance = PixAddressKeyGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixAddressKeyGetResponseDTO.to_json())

# convert the object into a dict
pix_address_key_get_response_dto_dict = pix_address_key_get_response_dto_instance.to_dict()
# create an instance of PixAddressKeyGetResponseDTO from a dict
pix_address_key_get_response_dto_from_dict = PixAddressKeyGetResponseDTO.from_dict(pix_address_key_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
