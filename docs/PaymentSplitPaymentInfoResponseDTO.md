# PaymentSplitPaymentInfoResponseDTO

Dados da cobrança associada ao split

## Properties

| Name                   | Type     | Description                       | Notes      |
| ---------------------- | -------- | --------------------------------- | ---------- |
| **confirmed_date**     | **date** | Data de pagamento da cobrança     | [optional] |
| **invoice_number**     | **str**  | Número da fatura                  | [optional] |
| **external_reference** | **str**  | Identificador externo da cobrança | [optional] |

## Example

```python
from asaas.models.payment_split_payment_info_response_dto import PaymentSplitPaymentInfoResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSplitPaymentInfoResponseDTO from a JSON string
payment_split_payment_info_response_dto_instance = PaymentSplitPaymentInfoResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSplitPaymentInfoResponseDTO.to_json())

# convert the object into a dict
payment_split_payment_info_response_dto_dict = payment_split_payment_info_response_dto_instance.to_dict()
# create an instance of PaymentSplitPaymentInfoResponseDTO from a dict
payment_split_payment_info_response_dto_from_dict = PaymentSplitPaymentInfoResponseDTO.from_dict(payment_split_payment_info_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
