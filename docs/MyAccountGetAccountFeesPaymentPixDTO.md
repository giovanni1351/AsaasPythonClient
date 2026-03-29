# MyAccountGetAccountFeesPaymentPixDTO

Taxas de pix

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fixed_fee_value** | **float** | Taxa fixa (Se houver) | [optional] 
**fixed_fee_value_with_discount** | **float** | Taxa fixa promocional (Se houver) | [optional] 
**percentage_fee** | **float** | Taxa percentual (Se houver) | [optional] 
**minimum_fee_value** | **float** | Taxa fixa mínima em caso de taxa percentual | [optional] 
**maximum_fee_value** | **float** | Taxa fixa máxima em caso de taxa percentual | [optional] 
**discount_expiration** | **datetime** | Data de expiração da taxa promocional (Se houver) | [optional] 
**monthly_credits_without_fee** | **int** | Quantidade de transações grátis no mês | [optional] 
**credits_received_of_current_month** | **int** | Quantas transações já recebeu este mês | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_payment_pix_dto import MyAccountGetAccountFeesPaymentPixDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesPaymentPixDTO from a JSON string
my_account_get_account_fees_payment_pix_dto_instance = MyAccountGetAccountFeesPaymentPixDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesPaymentPixDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_payment_pix_dto_dict = my_account_get_account_fees_payment_pix_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesPaymentPixDTO from a dict
my_account_get_account_fees_payment_pix_dto_from_dict = MyAccountGetAccountFeesPaymentPixDTO.from_dict(my_account_get_account_fees_payment_pix_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


