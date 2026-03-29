# PaymentReceiveInCashRequestDTO

## Properties

| Name                | Type      | Description                                                      | Notes      |
| ------------------- | --------- | ---------------------------------------------------------------- | ---------- |
| **payment_date**    | **date**  | Data em que o cliente efetuou o pagamento                        | [optional] |
| **value**           | **float** | Valor pago pelo cliente                                          | [optional] |
| **notify_customer** | **bool**  | Enviar ou não notificação de pagamento confirmado para o cliente | [optional] |

## Example

```python
from asaas.models.payment_receive_in_cash_request_dto import PaymentReceiveInCashRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentReceiveInCashRequestDTO from a JSON string
payment_receive_in_cash_request_dto_instance = PaymentReceiveInCashRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentReceiveInCashRequestDTO.to_json())

# convert the object into a dict
payment_receive_in_cash_request_dto_dict = payment_receive_in_cash_request_dto_instance.to_dict()
# create an instance of PaymentReceiveInCashRequestDTO from a dict
payment_receive_in_cash_request_dto_from_dict = PaymentReceiveInCashRequestDTO.from_dict(payment_receive_in_cash_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
