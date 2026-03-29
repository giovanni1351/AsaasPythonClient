# PaymentChargebackResponseDTO

## Properties

| Name                                   | Type                                                                                                        | Description                                                         | Notes      |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ---------- |
| **id**                                 | **str**                                                                                                     | Identificador único do chargeback.                                  | [optional] |
| **payment**                            | **str**                                                                                                     | Identificador único da cobrança no Asaas                            | [optional] |
| **installment**                        | **str**                                                                                                     | Identificador único do parcelamento no Asaas                        | [optional] |
| **customer_account**                   | **str**                                                                                                     | Identificador único do cliente ao qual o chargeback está vinculado. | [optional] |
| **status**                             | [**PaymentChargebackResponseChargebackStatus**](PaymentChargebackResponseChargebackStatus.md)               |                                                                     | [optional] |
| **reason**                             | [**PaymentChargebackResponseChargebackReason**](PaymentChargebackResponseChargebackReason.md)               |                                                                     | [optional] |
| **dispute_start_date**                 | **date**                                                                                                    | Data de abertura do chargeback.                                     | [optional] |
| **value**                              | **float**                                                                                                   | Valor do chargeback.                                                | [optional] |
| **payment_date**                       | **date**                                                                                                    | Data de liquidação da cobrança no Asaas                             | [optional] |
| **credit_card**                        | [**ChargebackCreditCardResponseDTO**](ChargebackCreditCardResponseDTO.md)                                   |                                                                     | [optional] |
| **dispute_status**                     | [**PaymentChargebackResponseChargebackDisputeStatus**](PaymentChargebackResponseChargebackDisputeStatus.md) |                                                                     | [optional] |
| **deadline_to_send_dispute_documents** | **date**                                                                                                    | Data limite para envio de documentos de disputa.                    | [optional] |

## Example

```python
from asaas.models.payment_chargeback_response_dto import PaymentChargebackResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentChargebackResponseDTO from a JSON string
payment_chargeback_response_dto_instance = PaymentChargebackResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentChargebackResponseDTO.to_json())

# convert the object into a dict
payment_chargeback_response_dto_dict = payment_chargeback_response_dto_instance.to_dict()
# create an instance of PaymentChargebackResponseDTO from a dict
payment_chargeback_response_dto_from_dict = PaymentChargebackResponseDTO.from_dict(payment_chargeback_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
