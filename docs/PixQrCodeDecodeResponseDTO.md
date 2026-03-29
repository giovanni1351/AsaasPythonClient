# PixQrCodeDecodeResponseDTO

## Properties

| Name                                 | Type                                                                                                                    | Description                                         | Notes      |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- | ---------- |
| **payload**                          | **str**                                                                                                                 | Copia e Cola do QrCode                              | [optional] |
| **type**                             | [**PixQrCodeDecodeResponsePixQrCodeType**](PixQrCodeDecodeResponsePixQrCodeType.md)                                     |                                                     | [optional] |
| **transaction_origin_type**          | [**PixQrCodeDecodeResponsePixTransactionOriginType**](PixQrCodeDecodeResponsePixTransactionOriginType.md)               |                                                     | [optional] |
| **pix_key**                          | **str**                                                                                                                 | Chave Pix utilizada                                 | [optional] |
| **conciliation_identifier**          | **str**                                                                                                                 | Identificador único de conciliação Pix com o Asaas  | [optional] |
| **due_date**                         | **date**                                                                                                                | Data de vencimento                                  | [optional] |
| **expiration_date**                  | **datetime**                                                                                                            | Data de expiração                                   | [optional] |
| **finality**                         | [**PixQrCodeDecodeResponsePixTransactionCashValueFinality**](PixQrCodeDecodeResponsePixTransactionCashValueFinality.md) |                                                     | [optional] |
| **value**                            | **float**                                                                                                               | Valor do QRCode                                     | [optional] |
| **change_value**                     | **float**                                                                                                               | Valor do troco                                      | [optional] |
| **interest**                         | **float**                                                                                                               | Valor dos juros                                     | [optional] |
| **fine**                             | **float**                                                                                                               | Valor das multas                                    | [optional] |
| **discount**                         | **float**                                                                                                               | Valor do desconto                                   | [optional] |
| **total_value**                      | **float**                                                                                                               | Valor total com a multa, juros e desconto aplicados | [optional] |
| **can_be_paid_with_different_value** | **bool**                                                                                                                | Informa se o QRCode pode ser pago com outro valor   | [optional] |
| **can_be_modify_change_value**       | **bool**                                                                                                                | Informa se o troco pode ser pago com outro valor    | [optional] |
| **receiver**                         | [**PixQrCodeDecodeReceiverDTO**](PixQrCodeDecodeReceiverDTO.md)                                                         |                                                     | [optional] |
| **payer**                            | [**PixTransactionQrCodePayerResponseDTO**](PixTransactionQrCodePayerResponseDTO.md)                                     |                                                     | [optional] |
| **description**                      | **str**                                                                                                                 | Descrição informada durante a criação do QRCode     | [optional] |
| **can_be_paid**                      | **bool**                                                                                                                | Informa se o QRCode pode ser pago                   | [optional] |
| **cannot_be_paid_reason**            | **str**                                                                                                                 | Informa o porquê do QRCode não pode ser pago        | [optional] |

## Example

```python
from asaas.models.pix_qr_code_decode_response_dto import PixQrCodeDecodeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixQrCodeDecodeResponseDTO from a JSON string
pix_qr_code_decode_response_dto_instance = PixQrCodeDecodeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixQrCodeDecodeResponseDTO.to_json())

# convert the object into a dict
pix_qr_code_decode_response_dto_dict = pix_qr_code_decode_response_dto_instance.to_dict()
# create an instance of PixQrCodeDecodeResponseDTO from a dict
pix_qr_code_decode_response_dto_from_dict = PixQrCodeDecodeResponseDTO.from_dict(pix_qr_code_decode_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
