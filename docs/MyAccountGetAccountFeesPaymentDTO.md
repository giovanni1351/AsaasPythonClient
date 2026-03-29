# MyAccountGetAccountFeesPaymentDTO

Taxas de cobranças

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bank_slip** | [**MyAccountGetAccountFeesPaymentBankSlipDTO**](MyAccountGetAccountFeesPaymentBankSlipDTO.md) |  | [optional] 
**credit_card** | [**MyAccountGetAccountFeesPaymentCreditCardDTO**](MyAccountGetAccountFeesPaymentCreditCardDTO.md) |  | [optional] 
**debit_card** | [**MyAccountGetAccountFeesPaymentDebitCardDTO**](MyAccountGetAccountFeesPaymentDebitCardDTO.md) |  | [optional] 
**pix** | [**MyAccountGetAccountFeesPaymentPixDTO**](MyAccountGetAccountFeesPaymentPixDTO.md) |  | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_payment_dto import MyAccountGetAccountFeesPaymentDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesPaymentDTO from a JSON string
my_account_get_account_fees_payment_dto_instance = MyAccountGetAccountFeesPaymentDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesPaymentDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_payment_dto_dict = my_account_get_account_fees_payment_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesPaymentDTO from a dict
my_account_get_account_fees_payment_dto_from_dict = MyAccountGetAccountFeesPaymentDTO.from_dict(my_account_get_account_fees_payment_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


