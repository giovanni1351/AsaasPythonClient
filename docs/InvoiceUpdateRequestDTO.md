# InvoiceUpdateRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service_description** | **str** | Descrição dos serviços da nota fiscal | [optional] 
**observations** | **str** | Observações adicionais | [optional] 
**external_reference** | **str** | Identificador da nota fiscal no seu sistema | [optional] 
**value** | **float** | Valor total | [optional] 
**deductions** | **float** | Deduções. As deduções não alteram o valor total da nota fiscal, mas alteram a base de cálculo do ISS | [optional] 
**effective_date** | **date** | Data de emissão da nota fiscal | [optional] 
**update_payment** | **bool** | Atualizar o valor da cobrança com os impostos da nota já descontados. | [optional] 
**taxes** | [**InvoiceTaxesRequestDTO**](InvoiceTaxesRequestDTO.md) |  | [optional] 

## Example

```python
from asaas.models.invoice_update_request_dto import InvoiceUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InvoiceUpdateRequestDTO from a JSON string
invoice_update_request_dto_instance = InvoiceUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(InvoiceUpdateRequestDTO.to_json())

# convert the object into a dict
invoice_update_request_dto_dict = invoice_update_request_dto_instance.to_dict()
# create an instance of InvoiceUpdateRequestDTO from a dict
invoice_update_request_dto_from_dict = InvoiceUpdateRequestDTO.from_dict(invoice_update_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


