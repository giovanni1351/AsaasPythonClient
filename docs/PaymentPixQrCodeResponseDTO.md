# PaymentPixQrCodeResponseDTO

Dados do pagamento relacionados a Pix

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**encoded_image** | **str** | Imagem do QrCode em base64 | [optional] 
**payload** | **str** | Copia e Cola do QrCode | [optional] 
**expiration_date** | **datetime** | Data de expiração do QrCode | [optional] 
**description** | **str** | Descrição do QrCode | [optional] 

## Example

```python
from asaas.models.payment_pix_qr_code_response_dto import PaymentPixQrCodeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentPixQrCodeResponseDTO from a JSON string
payment_pix_qr_code_response_dto_instance = PaymentPixQrCodeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentPixQrCodeResponseDTO.to_json())

# convert the object into a dict
payment_pix_qr_code_response_dto_dict = payment_pix_qr_code_response_dto_instance.to_dict()
# create an instance of PaymentPixQrCodeResponseDTO from a dict
payment_pix_qr_code_response_dto_from_dict = PaymentPixQrCodeResponseDTO.from_dict(payment_pix_qr_code_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


