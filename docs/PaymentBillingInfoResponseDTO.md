# PaymentBillingInfoResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pix** | [**PaymentPixQrCodeResponseDTO**](PaymentPixQrCodeResponseDTO.md) |  | [optional] 
**credit_card** | [**CreditCardTokenizeResponseDTO**](CreditCardTokenizeResponseDTO.md) |  | [optional] 
**bank_slip** | [**BankSlipBillingInfoResponseDTO**](BankSlipBillingInfoResponseDTO.md) |  | [optional] 

## Example

```python
from asaas.models.payment_billing_info_response_dto import PaymentBillingInfoResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentBillingInfoResponseDTO from a JSON string
payment_billing_info_response_dto_instance = PaymentBillingInfoResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentBillingInfoResponseDTO.to_json())

# convert the object into a dict
payment_billing_info_response_dto_dict = payment_billing_info_response_dto_instance.to_dict()
# create an instance of PaymentBillingInfoResponseDTO from a dict
payment_billing_info_response_dto_from_dict = PaymentBillingInfoResponseDTO.from_dict(payment_billing_info_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


