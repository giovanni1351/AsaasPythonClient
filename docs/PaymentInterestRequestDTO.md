# PaymentInterestRequestDTO

Informações de juros para pagamento após o vencimento

## Properties

| Name      | Type      | Description                                                                             | Notes      |
| --------- | --------- | --------------------------------------------------------------------------------------- | ---------- |
| **value** | **float** | Percentual de juros _ao mês_ sobre o valor da cobrança para pagamento após o vencimento | [optional] |

## Example

```python
from asaas.models.payment_interest_request_dto import PaymentInterestRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentInterestRequestDTO from a JSON string
payment_interest_request_dto_instance = PaymentInterestRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentInterestRequestDTO.to_json())

# convert the object into a dict
payment_interest_request_dto_dict = payment_interest_request_dto_instance.to_dict()
# create an instance of PaymentInterestRequestDTO from a dict
payment_interest_request_dto_from_dict = PaymentInterestRequestDTO.from_dict(payment_interest_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
