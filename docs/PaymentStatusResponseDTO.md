# PaymentStatusResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**PaymentStatusResponsePaymentStatus**](PaymentStatusResponsePaymentStatus.md) |  | [optional] 

## Example

```python
from asaas.models.payment_status_response_dto import PaymentStatusResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentStatusResponseDTO from a JSON string
payment_status_response_dto_instance = PaymentStatusResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentStatusResponseDTO.to_json())

# convert the object into a dict
payment_status_response_dto_dict = payment_status_response_dto_instance.to_dict()
# create an instance of PaymentStatusResponseDTO from a dict
payment_status_response_dto_from_dict = PaymentStatusResponseDTO.from_dict(payment_status_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


