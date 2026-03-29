# PixOriginalTransactionResponseDTO

Informações originais da transação caso tenha ocorrido um estorno

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único da transação | [optional] 
**end_to_end_identifier** | **str** | Identificador único da transação Pix no Banco Central | [optional] 
**value** | **float** | Valor original da transação | [optional] 
**effective_date** | **date** | Data da transação | [optional] 

## Example

```python
from asaas.models.pix_original_transaction_response_dto import PixOriginalTransactionResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixOriginalTransactionResponseDTO from a JSON string
pix_original_transaction_response_dto_instance = PixOriginalTransactionResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixOriginalTransactionResponseDTO.to_json())

# convert the object into a dict
pix_original_transaction_response_dto_dict = pix_original_transaction_response_dto_instance.to_dict()
# create an instance of PixOriginalTransactionResponseDTO from a dict
pix_original_transaction_response_dto_from_dict = PixOriginalTransactionResponseDTO.from_dict(pix_original_transaction_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


