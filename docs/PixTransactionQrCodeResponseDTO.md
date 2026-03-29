# PixTransactionQrCodeResponseDTO

Informações sobre o QrCode

## Properties

| Name                        | Type                                                                                | Description                                        | Notes      |
| --------------------------- | ----------------------------------------------------------------------------------- | -------------------------------------------------- | ---------- |
| **payer**                   | [**PixTransactionQrCodePayerResponseDTO**](PixTransactionQrCodePayerResponseDTO.md) |                                                    | [optional] |
| **conciliation_identifier** | **str**                                                                             | Identificador único de conciliação Pix com o Asaas | [optional] |
| **original_value**          | **float**                                                                           | Valor original da transação                        | [optional] |
| **due_date**                | **date**                                                                            | Data de vencimento                                 | [optional] |
| **interest**                | **float**                                                                           | Valor dos juros                                    | [optional] |
| **fine**                    | **float**                                                                           | Valor da multa                                     | [optional] |
| **discount**                | **float**                                                                           | Valor do desconto                                  | [optional] |
| **expiration_date**         | **datetime**                                                                        | Data de expiração                                  | [optional] |
| **description**             | **str**                                                                             | Descrição do QrCode                                | [optional] |

## Example

```python
from asaas.models.pix_transaction_qr_code_response_dto import PixTransactionQrCodeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixTransactionQrCodeResponseDTO from a JSON string
pix_transaction_qr_code_response_dto_instance = PixTransactionQrCodeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixTransactionQrCodeResponseDTO.to_json())

# convert the object into a dict
pix_transaction_qr_code_response_dto_dict = pix_transaction_qr_code_response_dto_instance.to_dict()
# create an instance of PixTransactionQrCodeResponseDTO from a dict
pix_transaction_qr_code_response_dto_from_dict = PixTransactionQrCodeResponseDTO.from_dict(pix_transaction_qr_code_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
