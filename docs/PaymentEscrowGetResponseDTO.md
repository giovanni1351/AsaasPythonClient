# PaymentEscrowGetResponseDTO

Informações de garantia da cobrança na Conta Escrow

## Properties

| Name                | Type                                                                                                          | Description                                                          | Notes      |
| ------------------- | ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ---------- |
| **id**              | **str**                                                                                                       | Identificador único da garantia da cobrança na Conta Escrow do Asaas | [optional] |
| **status**          | [**PaymentEscrowGetResponsePaymentEscrowStatus**](PaymentEscrowGetResponsePaymentEscrowStatus.md)             |                                                                      | [optional] |
| **expiration_date** | **date**                                                                                                      | Data de expiração da garantia da cobrança                            | [optional] |
| **finish_date**     | **date**                                                                                                      | Data de encerramento da garantia da cobrança                         | [optional] |
| **finish_reason**   | [**PaymentEscrowGetResponsePaymentEscrowFinishReason**](PaymentEscrowGetResponsePaymentEscrowFinishReason.md) |                                                                      | [optional] |

## Example

```python
from asaas.models.payment_escrow_get_response_dto import PaymentEscrowGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentEscrowGetResponseDTO from a JSON string
payment_escrow_get_response_dto_instance = PaymentEscrowGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentEscrowGetResponseDTO.to_json())

# convert the object into a dict
payment_escrow_get_response_dto_dict = payment_escrow_get_response_dto_instance.to_dict()
# create an instance of PaymentEscrowGetResponseDTO from a dict
payment_escrow_get_response_dto_from_dict = PaymentEscrowGetResponseDTO.from_dict(payment_escrow_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
