# PaymentSimulatePixResponseDTO

Taxas de PIX

## Properties

| Name               | Type                                                                                  | Description         | Notes      |
| ------------------ | ------------------------------------------------------------------------------------- | ------------------- | ---------- |
| **net_value**      | **float**                                                                             | Valor liquido       | [optional] |
| **fee_percentage** | **float**                                                                             | Taxa em porcentagem | [optional] |
| **fee_value**      | **float**                                                                             | Valor da taxa       | [optional] |
| **installment**    | [**PaymentSimulateInstallmentResponseDTO**](PaymentSimulateInstallmentResponseDTO.md) |                     | [optional] |

## Example

```python
from asaas.models.payment_simulate_pix_response_dto import PaymentSimulatePixResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSimulatePixResponseDTO from a JSON string
payment_simulate_pix_response_dto_instance = PaymentSimulatePixResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSimulatePixResponseDTO.to_json())

# convert the object into a dict
payment_simulate_pix_response_dto_dict = payment_simulate_pix_response_dto_instance.to_dict()
# create an instance of PaymentSimulatePixResponseDTO from a dict
payment_simulate_pix_response_dto_from_dict = PaymentSimulatePixResponseDTO.from_dict(payment_simulate_pix_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
