# FinancialTransactionGetResponseDTO

Lista de objetos

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo de objeto | [optional] 
**id** | **str** | Identificador único da transação no Asaas | [optional] 
**value** | **float** | Valor da transação | [optional] 
**balance** | **float** | Valor em conta no momento da transação | [optional] 
**type** | [**FinancialTransactionGetResponseFinancialTransactionType**](FinancialTransactionGetResponseFinancialTransactionType.md) |  | [optional] 
**var_date** | **date** | Data da transação | [optional] 
**description** | **str** | Descrição da transação | [optional] 
**payment_id** | **str** | Identificador da cobrança (Se houver) | [optional] 
**split_id** | **str** | Identificador do split (Se houver) | [optional] 
**transfer_id** | **str** | Identificador da transferência (Se houver) | [optional] 
**anticipation_id** | **str** | Identificador da antecipação (Se houver) | [optional] 
**bill_id** | **str** | Identificador do pagamento de contas (Se houver) | [optional] 
**invoice_id** | **str** | Identificador da nota fiscal (Se houver) | [optional] 
**payment_dunning_id** | **str** | Identificador da negativação (Se houver) | [optional] 
**credit_bureau_report_id** | **str** | Identificador da consulta Serasa (Se houver) | [optional] 

## Example

```python
from asaas.models.financial_transaction_get_response_dto import FinancialTransactionGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FinancialTransactionGetResponseDTO from a JSON string
financial_transaction_get_response_dto_instance = FinancialTransactionGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FinancialTransactionGetResponseDTO.to_json())

# convert the object into a dict
financial_transaction_get_response_dto_dict = financial_transaction_get_response_dto_instance.to_dict()
# create an instance of FinancialTransactionGetResponseDTO from a dict
financial_transaction_get_response_dto_from_dict = FinancialTransactionGetResponseDTO.from_dict(financial_transaction_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


