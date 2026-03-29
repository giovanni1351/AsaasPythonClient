# PixTransactionGetResponseDTO

## Properties

| Name                        | Type                                                                                                                        | Description                                                                  | Notes      |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------- |
| **id**                      | **str**                                                                                                                     | Identificador único da transação Pix no Asaas                                | [optional] |
| **end_to_end_identifier**   | **str**                                                                                                                     | Identificador da transação Pix no Banco Central                              | [optional] |
| **finality**                | [**PixTransactionGetResponsePixTransactionCashValueFinality**](PixTransactionGetResponsePixTransactionCashValueFinality.md) |                                                                              | [optional] |
| **value**                   | **float**                                                                                                                   | Valor da transação ou de um Saque                                            | [optional] |
| **change_value**            | **float**                                                                                                                   | Valor do troco                                                               | [optional] |
| **refunded_value**          | **float**                                                                                                                   | Valor estornado                                                              | [optional] |
| **effective_date**          | **datetime**                                                                                                                | Data da transação                                                            | [optional] |
| **scheduled_date**          | **date**                                                                                                                    | Data do agendamento                                                          | [optional] |
| **status**                  | [**PixTransactionGetResponsePixTransactionStatus**](PixTransactionGetResponsePixTransactionStatus.md)                       |                                                                              | [optional] |
| **type**                    | [**PixTransactionGetResponsePixTransactionType**](PixTransactionGetResponsePixTransactionType.md)                           |                                                                              | [optional] |
| **origin_type**             | [**PixTransactionGetResponsePixTransactionOriginType**](PixTransactionGetResponsePixTransactionOriginType.md)               |                                                                              | [optional] |
| **conciliation_identifier** | **str**                                                                                                                     | Identificador do QrCode vinculado a transação                                | [optional] |
| **description**             | **str**                                                                                                                     | Descrição sobre a transação                                                  | [optional] |
| **transaction_receipt_url** | **str**                                                                                                                     | Comprovante de transação, estará disponível após a transação ser confirmada. | [optional] |
| **refusal_reason**          | **str**                                                                                                                     | Motivo pelo qual a transação foi recusada                                    | [optional] |
| **can_be_canceled**         | **bool**                                                                                                                    | Indica se a transação pode ser cancelada                                     | [optional] |
| **original_transaction**    | [**PixOriginalTransactionResponseDTO**](PixOriginalTransactionResponseDTO.md)                                               |                                                                              | [optional] |
| **external_account**        | [**PixTransactionExternalAccountResponseDTO**](PixTransactionExternalAccountResponseDTO.md)                                 |                                                                              | [optional] |
| **qr_code**                 | [**PixTransactionQrCodeResponseDTO**](PixTransactionQrCodeResponseDTO.md)                                                   |                                                                              | [optional] |
| **payment**                 | **str**                                                                                                                     | Identificador único da cobrança                                              | [optional] |
| **can_be_refunded**         | **bool**                                                                                                                    | Indica se a transação pode ser estornada                                     | [optional] |
| **refund_disabled_reason**  | **str**                                                                                                                     | Motivo pelo qual o estorno foi desabilitado                                  | [optional] |
| **charged_fee_value**       | **float**                                                                                                                   | Taxa de débito ou crédito referente a transação                              | [optional] |
| **date_created**            | **datetime**                                                                                                                | Data de criação da transação                                                 | [optional] |
| **address_key**             | **str**                                                                                                                     | Chave Pix quando a transação é um crédito                                    | [optional] |
| **address_key_type**        | [**PixTransactionGetResponsePixAddressKeyType**](PixTransactionGetResponsePixAddressKeyType.md)                             |                                                                              | [optional] |
| **transfer_id**             | **str**                                                                                                                     | Identificador da transferência                                               | [optional] |
| **external_reference**      | **str**                                                                                                                     | Campo livre para busca                                                       | [optional] |

## Example

```python
from asaas.models.pix_transaction_get_response_dto import PixTransactionGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixTransactionGetResponseDTO from a JSON string
pix_transaction_get_response_dto_instance = PixTransactionGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixTransactionGetResponseDTO.to_json())

# convert the object into a dict
pix_transaction_get_response_dto_dict = pix_transaction_get_response_dto_instance.to_dict()
# create an instance of PixTransactionGetResponseDTO from a dict
pix_transaction_get_response_dto_from_dict = PixTransactionGetResponseDTO.from_dict(pix_transaction_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
