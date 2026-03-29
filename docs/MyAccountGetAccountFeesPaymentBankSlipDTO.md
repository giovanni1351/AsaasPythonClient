# MyAccountGetAccountFeesPaymentBankSlipDTO

Taxas de boleto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**default_value** | **float** | Taxa por cobrança | [optional] 
**discount_value** | **float** | Taxa promocional (Se houver) | [optional] 
**expiration_date** | **datetime** | Data de expiração da taxa promocional (Se houver) | [optional] 
**days_to_receive** | **int** | Dias para recebimento da cobrança | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_payment_bank_slip_dto import MyAccountGetAccountFeesPaymentBankSlipDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesPaymentBankSlipDTO from a JSON string
my_account_get_account_fees_payment_bank_slip_dto_instance = MyAccountGetAccountFeesPaymentBankSlipDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesPaymentBankSlipDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_payment_bank_slip_dto_dict = my_account_get_account_fees_payment_bank_slip_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesPaymentBankSlipDTO from a dict
my_account_get_account_fees_payment_bank_slip_dto_from_dict = MyAccountGetAccountFeesPaymentBankSlipDTO.from_dict(my_account_get_account_fees_payment_bank_slip_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


