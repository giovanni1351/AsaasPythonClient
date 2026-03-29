# FinancialTransactionListResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo de objeto | [optional] 
**has_more** | **bool** | Indica se há mais uma página a ser buscada | [optional] 
**total_count** | **int** | Quantidade total de itens para os filtros informados | [optional] 
**limit** | **int** | Quantidade de objetos por página | [optional] 
**offset** | **int** | Posição do objeto a partir do qual a página deve ser carregada | [optional] 
**data** | [**List[FinancialTransactionGetResponseDTO]**](FinancialTransactionGetResponseDTO.md) | Lista de objetos | [optional] 

## Example

```python
from asaas.models.financial_transaction_list_response_dto import FinancialTransactionListResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FinancialTransactionListResponseDTO from a JSON string
financial_transaction_list_response_dto_instance = FinancialTransactionListResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FinancialTransactionListResponseDTO.to_json())

# convert the object into a dict
financial_transaction_list_response_dto_dict = financial_transaction_list_response_dto_instance.to_dict()
# create an instance of FinancialTransactionListResponseDTO from a dict
financial_transaction_list_response_dto_from_dict = FinancialTransactionListResponseDTO.from_dict(financial_transaction_list_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


