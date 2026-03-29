# PixQrCodeSaveResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Imagem do qrCode em base64 | [optional] 
**encoded_image** | **str** | Identificador do QrCode | [optional] 
**payload** | **str** | Copia e Cola do QrCode | [optional] 
**allows_multiple_payments** | **bool** | Indica se permite múltiplos pagamentos | [optional] 
**expiration_date** | **datetime** | Data/Hora de expiração do QrCode, após desta data todos os pagamentos serão recusados | [optional] 
**external_reference** | **str** | Campo livre para busca | [optional] 
**description** | **str** | Descrição do QrCode | [optional] 

## Example

```python
from asaas.models.pix_qr_code_save_response_dto import PixQrCodeSaveResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixQrCodeSaveResponseDTO from a JSON string
pix_qr_code_save_response_dto_instance = PixQrCodeSaveResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixQrCodeSaveResponseDTO.to_json())

# convert the object into a dict
pix_qr_code_save_response_dto_dict = pix_qr_code_save_response_dto_instance.to_dict()
# create an instance of PixQrCodeSaveResponseDTO from a dict
pix_qr_code_save_response_dto_from_dict = PixQrCodeSaveResponseDTO.from_dict(pix_qr_code_save_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


