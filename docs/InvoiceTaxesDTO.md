# InvoiceTaxesDTO

Impostos da nota fiscal

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**retain_iss** | **bool** | Tomador da nota fiscal deve reter ISS ou não | 
**cofins** | **float** | Alíquota COFINS | 
**csll** | **float** | Alíquota CSLL | 
**inss** | **float** | Alíquota INSS | 
**ir** | **float** | Alíquota IR | 
**pis** | **float** | Alíquota PIS | 
**iss** | **float** | Alíquota ISS | 

## Example

```python
from asaas.models.invoice_taxes_dto import InvoiceTaxesDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InvoiceTaxesDTO from a JSON string
invoice_taxes_dto_instance = InvoiceTaxesDTO.from_json(json)
# print the JSON string representation of the object
print(InvoiceTaxesDTO.to_json())

# convert the object into a dict
invoice_taxes_dto_dict = invoice_taxes_dto_instance.to_dict()
# create an instance of InvoiceTaxesDTO from a dict
invoice_taxes_dto_from_dict = InvoiceTaxesDTO.from_dict(invoice_taxes_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


