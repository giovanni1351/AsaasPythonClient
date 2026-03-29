# PaymentRefundGetResponseDTO

Informações de estorno

## Properties

| Name                        | Type                                                                                              | Description                                                  | Notes      |
| --------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ | ---------- |
| **date_created**            | **datetime**                                                                                      | Data da criação do estorno                                   | [optional] |
| **status**                  | [**PaymentRefundGetResponsePaymentRefundStatus**](PaymentRefundGetResponsePaymentRefundStatus.md) |                                                              | [optional] |
| **value**                   | **float**                                                                                         | Valor do estorno                                             | [optional] |
| **end_to_end_identifier**   | **str**                                                                                           | (Apenas pix) Identificador da transação Pix no Banco Central | [optional] |
| **description**             | **str**                                                                                           | Descrição do estorno                                         | [optional] |
| **effective_date**          | **datetime**                                                                                      | (Apenas pix) Data de efetivação do estorno                   | [optional] |
| **transaction_receipt_url** | **str**                                                                                           | Link do recibo da transação                                  | [optional] |
| **refunded_splits**         | [**List[PaymentRefundedSplitResponseDTO]**](PaymentRefundedSplitResponseDTO.md)                   | Lista de splits estornados, se houver                        | [optional] |

## Example

```python
from asaas.models.payment_refund_get_response_dto import PaymentRefundGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentRefundGetResponseDTO from a JSON string
payment_refund_get_response_dto_instance = PaymentRefundGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentRefundGetResponseDTO.to_json())

# convert the object into a dict
payment_refund_get_response_dto_dict = payment_refund_get_response_dto_instance.to_dict()
# create an instance of PaymentRefundGetResponseDTO from a dict
payment_refund_get_response_dto_from_dict = PaymentRefundGetResponseDTO.from_dict(payment_refund_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
