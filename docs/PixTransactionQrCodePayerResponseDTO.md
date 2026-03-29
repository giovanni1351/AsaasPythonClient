# PixTransactionQrCodePayerResponseDTO

Informações sobre o pagador

## Properties

| Name         | Type    | Description            | Notes      |
| ------------ | ------- | ---------------------- | ---------- |
| **name**     | **str** | Nome do pagador        | [optional] |
| **cpf_cnpj** | **str** | CPF ou CNPJ do pagador | [optional] |

## Example

```python
from asaas.models.pix_transaction_qr_code_payer_response_dto import PixTransactionQrCodePayerResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixTransactionQrCodePayerResponseDTO from a JSON string
pix_transaction_qr_code_payer_response_dto_instance = PixTransactionQrCodePayerResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixTransactionQrCodePayerResponseDTO.to_json())

# convert the object into a dict
pix_transaction_qr_code_payer_response_dto_dict = pix_transaction_qr_code_payer_response_dto_instance.to_dict()
# create an instance of PixTransactionQrCodePayerResponseDTO from a dict
pix_transaction_qr_code_payer_response_dto_from_dict = PixTransactionQrCodePayerResponseDTO.from_dict(pix_transaction_qr_code_payer_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
