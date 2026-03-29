# PixTransactionQrCodeSaveRequestDTO

Payload do QRCode para pagamento

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payload** | **str** | Payload do QRCode | 
**change_value** | **float** | Valor do troco (para QRCode Troco) | [optional] 

## Example

```python
from asaas.models.pix_transaction_qr_code_save_request_dto import PixTransactionQrCodeSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixTransactionQrCodeSaveRequestDTO from a JSON string
pix_transaction_qr_code_save_request_dto_instance = PixTransactionQrCodeSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PixTransactionQrCodeSaveRequestDTO.to_json())

# convert the object into a dict
pix_transaction_qr_code_save_request_dto_dict = pix_transaction_qr_code_save_request_dto_instance.to_dict()
# create an instance of PixTransactionQrCodeSaveRequestDTO from a dict
pix_transaction_qr_code_save_request_dto_from_dict = PixTransactionQrCodeSaveRequestDTO.from_dict(pix_transaction_qr_code_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


