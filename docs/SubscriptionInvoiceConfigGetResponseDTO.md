# SubscriptionInvoiceConfigGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**municipal_service_id** | **str** | Identificador único do serviço municipal | [optional] 
**municipal_service_code** | **str** | Código de serviço municipal | [optional] 
**municipal_service_name** | **str** | Nome do serviço municipal | [optional] 
**deductions** | **float** | Deduções. As deduções não alteram o valor total da nota fiscal, mas alteram a base de cálculo do ISS. | [optional] 
**invoice_creation_period** | **str** | Quando a nota fiscal será emitida | [optional] 
**days_before_due_date** | **int** | Quantidade de dias antes do vencimento da cobrança | [optional] 
**received_only** | **bool** | Emitir apenas para cobranças pagas | [optional] 
**observations** | **str** | Observações adicionais da nota fiscal | [optional] 
**taxes** | [**InvoiceTaxesDTO**](InvoiceTaxesDTO.md) |  | [optional] 

## Example

```python
from asaas.models.subscription_invoice_config_get_response_dto import SubscriptionInvoiceConfigGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionInvoiceConfigGetResponseDTO from a JSON string
subscription_invoice_config_get_response_dto_instance = SubscriptionInvoiceConfigGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionInvoiceConfigGetResponseDTO.to_json())

# convert the object into a dict
subscription_invoice_config_get_response_dto_dict = subscription_invoice_config_get_response_dto_instance.to_dict()
# create an instance of SubscriptionInvoiceConfigGetResponseDTO from a dict
subscription_invoice_config_get_response_dto_from_dict = SubscriptionInvoiceConfigGetResponseDTO.from_dict(subscription_invoice_config_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


