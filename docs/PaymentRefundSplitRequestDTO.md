# PaymentRefundSplitRequestDTO

Estorno de splits

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único do split no Asaas | 
**value** | **float** | Valor a ser estornado do split | 

## Example

```python
from asaas.models.payment_refund_split_request_dto import PaymentRefundSplitRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentRefundSplitRequestDTO from a JSON string
payment_refund_split_request_dto_instance = PaymentRefundSplitRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentRefundSplitRequestDTO.to_json())

# convert the object into a dict
payment_refund_split_request_dto_dict = payment_refund_split_request_dto_instance.to_dict()
# create an instance of PaymentRefundSplitRequestDTO from a dict
payment_refund_split_request_dto_from_dict = PaymentRefundSplitRequestDTO.from_dict(payment_refund_split_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


