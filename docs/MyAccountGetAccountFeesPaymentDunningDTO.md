# MyAccountGetAccountFeesPaymentDunningDTO

Taxas de negativação Serasa

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fee_value** | **float** | Taxa por cobrança | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_payment_dunning_dto import MyAccountGetAccountFeesPaymentDunningDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesPaymentDunningDTO from a JSON string
my_account_get_account_fees_payment_dunning_dto_instance = MyAccountGetAccountFeesPaymentDunningDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesPaymentDunningDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_payment_dunning_dto_dict = my_account_get_account_fees_payment_dunning_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesPaymentDunningDTO from a dict
my_account_get_account_fees_payment_dunning_dto_from_dict = MyAccountGetAccountFeesPaymentDunningDTO.from_dict(my_account_get_account_fees_payment_dunning_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


