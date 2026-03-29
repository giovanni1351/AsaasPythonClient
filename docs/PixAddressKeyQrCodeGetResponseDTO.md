# PixAddressKeyQrCodeGetResponseDTO

QrCode da chave Pix

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**encoded_image** | **str** | Imagem do QrCode em base64 | [optional] 
**payload** | **str** | Copia e Cola do QrCode | [optional] 

## Example

```python
from asaas.models.pix_address_key_qr_code_get_response_dto import PixAddressKeyQrCodeGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixAddressKeyQrCodeGetResponseDTO from a JSON string
pix_address_key_qr_code_get_response_dto_instance = PixAddressKeyQrCodeGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixAddressKeyQrCodeGetResponseDTO.to_json())

# convert the object into a dict
pix_address_key_qr_code_get_response_dto_dict = pix_address_key_qr_code_get_response_dto_instance.to_dict()
# create an instance of PixAddressKeyQrCodeGetResponseDTO from a dict
pix_address_key_qr_code_get_response_dto_from_dict = PixAddressKeyQrCodeGetResponseDTO.from_dict(pix_address_key_qr_code_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


