# PaymentInterestResponseDTO

Informações de juros para pagamento após o vencimento

## Properties

| Name      | Type      | Description                    | Notes      |
| --------- | --------- | ------------------------------ | ---------- |
| **value** | **float** | Valor dos juros em porcentagem | [optional] |

## Example

```python
from asaas.models.payment_interest_response_dto import PaymentInterestResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentInterestResponseDTO from a JSON string
payment_interest_response_dto_instance = PaymentInterestResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentInterestResponseDTO.to_json())

# convert the object into a dict
payment_interest_response_dto_dict = payment_interest_response_dto_instance.to_dict()
# create an instance of PaymentInterestResponseDTO from a dict
payment_interest_response_dto_from_dict = PaymentInterestResponseDTO.from_dict(payment_interest_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
