# PaymentRefundRequestDTO

## Properties

| Name              | Type                                                                      | Description                 | Notes      |
| ----------------- | ------------------------------------------------------------------------- | --------------------------- | ---------- |
| **value**         | **float**                                                                 | Valor total a ser estornado | [optional] |
| **description**   | **str**                                                                   | Motivo do estorno           | [optional] |
| **split_refunds** | [**List[PaymentRefundSplitRequestDTO]**](PaymentRefundSplitRequestDTO.md) | Estorno de splits           | [optional] |

## Example

```python
from asaas.models.payment_refund_request_dto import PaymentRefundRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentRefundRequestDTO from a JSON string
payment_refund_request_dto_instance = PaymentRefundRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentRefundRequestDTO.to_json())

# convert the object into a dict
payment_refund_request_dto_dict = payment_refund_request_dto_instance.to_dict()
# create an instance of PaymentRefundRequestDTO from a dict
payment_refund_request_dto_from_dict = PaymentRefundRequestDTO.from_dict(payment_refund_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
