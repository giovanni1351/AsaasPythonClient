# InstallmentRefundRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | Valor total a ser estornado | [optional] 
**split_refunds** | [**List[PaymentRefundSplitRequestDTO]**](PaymentRefundSplitRequestDTO.md) | Estorno de splits | [optional] 

## Example

```python
from asaas.models.installment_refund_request_dto import InstallmentRefundRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentRefundRequestDTO from a JSON string
installment_refund_request_dto_instance = InstallmentRefundRequestDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentRefundRequestDTO.to_json())

# convert the object into a dict
installment_refund_request_dto_dict = installment_refund_request_dto_instance.to_dict()
# create an instance of InstallmentRefundRequestDTO from a dict
installment_refund_request_dto_from_dict = InstallmentRefundRequestDTO.from_dict(installment_refund_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


