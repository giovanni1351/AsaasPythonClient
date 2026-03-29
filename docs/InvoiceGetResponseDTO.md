# InvoiceGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo de objeto | [optional] 
**id** | **str** | Identificador único da nota fiscal no Asaas | [optional] 
**status** | [**InvoiceGetResponseInvoiceStatus**](InvoiceGetResponseInvoiceStatus.md) |  | [optional] 
**customer** | **str** | Identificador único do cliente no Asaas | [optional] 
**payment** | **str** | Identificador único da cobrança no Asaas | [optional] 
**installment** | **str** | Identificador único do parcelamento no Asaas | [optional] 
**type** | **str** | Tipo de nota fiscal | [optional] 
**status_description** | **str** | Descrição da situação atual da nota fiscal | [optional] 
**service_description** | **str** | Descrição dos serviços da nota fiscal | [optional] 
**pdf_url** | **str** | Link para arquivo pdf da nota fiscal emitida | [optional] 
**xml_url** | **str** | Link para arquivo xml da nota fiscal emitida | [optional] 
**rps_serie** | **str** | Série da nota fiscal | [optional] 
**rps_number** | **str** | RPS convertido para a nota fiscal | [optional] 
**number** | **str** | Número da nota fiscal | [optional] 
**validation_code** | **str** | Código de verificação | [optional] 
**value** | **float** | Valor total | [optional] 
**deductions** | **float** | Deduções. As deduções não alteram o valor total da nota fiscal, mas alteram a base de cálculo do ISS | [optional] 
**effective_date** | **date** | Data de emissão da nota fiscal | [optional] 
**observations** | **str** | Observações adicionais | [optional] 
**estimated_taxes_description** | **str** | Impostos estimados da nota fiscal | [optional] 
**external_reference** | **str** | Identificador da nota fiscal no seu sistema | [optional] 
**taxes** | [**InvoiceTaxesResponseDTO**](InvoiceTaxesResponseDTO.md) |  | [optional] 
**municipal_service_id** | **str** | Identificador único do serviço municipal | [optional] 
**municipal_service_code** | **str** | Código de serviço municipal | [optional] 
**municipal_service_name** | **str** | Nome do serviço municipal | [optional] 

## Example

```python
from asaas.models.invoice_get_response_dto import InvoiceGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InvoiceGetResponseDTO from a JSON string
invoice_get_response_dto_instance = InvoiceGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(InvoiceGetResponseDTO.to_json())

# convert the object into a dict
invoice_get_response_dto_dict = invoice_get_response_dto_instance.to_dict()
# create an instance of InvoiceGetResponseDTO from a dict
invoice_get_response_dto_from_dict = InvoiceGetResponseDTO.from_dict(invoice_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


