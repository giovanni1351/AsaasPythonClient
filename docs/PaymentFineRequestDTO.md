# PaymentFineRequestDTO

Informações de multa para pagamento após o vencimento

## Properties

| Name      | Type                                                            | Description                                                                    | Notes      |
| --------- | --------------------------------------------------------------- | ------------------------------------------------------------------------------ | ---------- |
| **value** | **float**                                                       | Percentual de multa sobre o valor da cobrança para pagamento após o vencimento | [optional] |
| **type**  | [**PaymentFineRequestFineType**](PaymentFineRequestFineType.md) |                                                                                | [optional] |

## Example

```python
from asaas.models.payment_fine_request_dto import PaymentFineRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentFineRequestDTO from a JSON string
payment_fine_request_dto_instance = PaymentFineRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentFineRequestDTO.to_json())

# convert the object into a dict
payment_fine_request_dto_dict = payment_fine_request_dto_instance.to_dict()
# create an instance of PaymentFineRequestDTO from a dict
payment_fine_request_dto_from_dict = PaymentFineRequestDTO.from_dict(payment_fine_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
