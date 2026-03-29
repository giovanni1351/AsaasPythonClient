# PaymentBankSlipRefundResponseDTO

## Properties

| Name            | Type    | Description                            | Notes      |
| --------------- | ------- | -------------------------------------- | ---------- |
| **request_url** | **str** | Link para informar os dados de estorno | [optional] |

## Example

```python
from asaas.models.payment_bank_slip_refund_response_dto import PaymentBankSlipRefundResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentBankSlipRefundResponseDTO from a JSON string
payment_bank_slip_refund_response_dto_instance = PaymentBankSlipRefundResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentBankSlipRefundResponseDTO.to_json())

# convert the object into a dict
payment_bank_slip_refund_response_dto_dict = payment_bank_slip_refund_response_dto_instance.to_dict()
# create an instance of PaymentBankSlipRefundResponseDTO from a dict
payment_bank_slip_refund_response_dto_from_dict = PaymentBankSlipRefundResponseDTO.from_dict(payment_bank_slip_refund_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
