# PixQrCodeDeleteResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador do QrCode | [optional] 
**deleted** | **bool** | Indica se o QR Code foi removido | [optional] 

## Example

```python
from asaas.models.pix_qr_code_delete_response_dto import PixQrCodeDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixQrCodeDeleteResponseDTO from a JSON string
pix_qr_code_delete_response_dto_instance = PixQrCodeDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixQrCodeDeleteResponseDTO.to_json())

# convert the object into a dict
pix_qr_code_delete_response_dto_dict = pix_qr_code_delete_response_dto_instance.to_dict()
# create an instance of PixQrCodeDeleteResponseDTO from a dict
pix_qr_code_delete_response_dto_from_dict = PixQrCodeDeleteResponseDTO.from_dict(pix_qr_code_delete_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


