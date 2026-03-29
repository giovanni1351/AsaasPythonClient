# PaymentSimulateBankSlipResponseDTO

Taxas de boleto

## Properties

| Name            | Type                                                                                  | Description   | Notes      |
| --------------- | ------------------------------------------------------------------------------------- | ------------- | ---------- |
| **net_value**   | **float**                                                                             | Valor liquido | [optional] |
| **fee_value**   | **float**                                                                             | Valor da taxa | [optional] |
| **installment** | [**PaymentSimulateInstallmentResponseDTO**](PaymentSimulateInstallmentResponseDTO.md) |               | [optional] |

## Example

```python
from asaas.models.payment_simulate_bank_slip_response_dto import PaymentSimulateBankSlipResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSimulateBankSlipResponseDTO from a JSON string
payment_simulate_bank_slip_response_dto_instance = PaymentSimulateBankSlipResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSimulateBankSlipResponseDTO.to_json())

# convert the object into a dict
payment_simulate_bank_slip_response_dto_dict = payment_simulate_bank_slip_response_dto_instance.to_dict()
# create an instance of PaymentSimulateBankSlipResponseDTO from a dict
payment_simulate_bank_slip_response_dto_from_dict = PaymentSimulateBankSlipResponseDTO.from_dict(payment_simulate_bank_slip_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
