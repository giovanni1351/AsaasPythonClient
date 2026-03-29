# MyAccountGetAccountFeesPaymentDebitCardDTO

Taxas de cartão de débito

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**operation_value** | **float** | Taxa operacional por cobrança | [optional] 
**default_percentage** | **float** | Taxa percentual por cobrança | [optional] 
**days_to_receive** | **int** | Dias para recebimento da cobrança | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_payment_debit_card_dto import MyAccountGetAccountFeesPaymentDebitCardDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesPaymentDebitCardDTO from a JSON string
my_account_get_account_fees_payment_debit_card_dto_instance = MyAccountGetAccountFeesPaymentDebitCardDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesPaymentDebitCardDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_payment_debit_card_dto_dict = my_account_get_account_fees_payment_debit_card_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesPaymentDebitCardDTO from a dict
my_account_get_account_fees_payment_debit_card_dto_from_dict = MyAccountGetAccountFeesPaymentDebitCardDTO.from_dict(my_account_get_account_fees_payment_debit_card_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


