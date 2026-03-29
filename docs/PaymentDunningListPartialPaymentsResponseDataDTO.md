# PaymentDunningListPartialPaymentsResponseDataDTO

Lista de objetos

## Properties

| Name             | Type      | Description            | Notes      |
| ---------------- | --------- | ---------------------- | ---------- |
| **value**        | **float** | Valor pago             | [optional] |
| **description**  | **str**   | Descrição do pagamento | [optional] |
| **payment_date** | **str**   | Data do pagamento      | [optional] |

## Example

```python
from asaas.models.payment_dunning_list_partial_payments_response_data_dto import PaymentDunningListPartialPaymentsResponseDataDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDunningListPartialPaymentsResponseDataDTO from a JSON string
payment_dunning_list_partial_payments_response_data_dto_instance = PaymentDunningListPartialPaymentsResponseDataDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDunningListPartialPaymentsResponseDataDTO.to_json())

# convert the object into a dict
payment_dunning_list_partial_payments_response_data_dto_dict = payment_dunning_list_partial_payments_response_data_dto_instance.to_dict()
# create an instance of PaymentDunningListPartialPaymentsResponseDataDTO from a dict
payment_dunning_list_partial_payments_response_data_dto_from_dict = PaymentDunningListPartialPaymentsResponseDataDTO.from_dict(payment_dunning_list_partial_payments_response_data_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
