# MyAccountGetAccountFeesInvoiceDTO

Taxas de notas fiscais

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fee_value** | **float** | Taxa por nota de serviço emitida | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_invoice_dto import MyAccountGetAccountFeesInvoiceDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesInvoiceDTO from a JSON string
my_account_get_account_fees_invoice_dto_instance = MyAccountGetAccountFeesInvoiceDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesInvoiceDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_invoice_dto_dict = my_account_get_account_fees_invoice_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesInvoiceDTO from a dict
my_account_get_account_fees_invoice_dto_from_dict = MyAccountGetAccountFeesInvoiceDTO.from_dict(my_account_get_account_fees_invoice_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


