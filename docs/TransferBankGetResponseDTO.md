# TransferBankGetResponseDTO

Dados do banco de destino

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ispb** | **str** | Identificador no Sistema de Pagamentos Brasileiro | [optional] 
**code** | **str** | Código de compensação do banco no sistema bancário | [optional] 
**name** | **str** | Nome do banco | [optional] 

## Example

```python
from asaas.models.transfer_bank_get_response_dto import TransferBankGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferBankGetResponseDTO from a JSON string
transfer_bank_get_response_dto_instance = TransferBankGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(TransferBankGetResponseDTO.to_json())

# convert the object into a dict
transfer_bank_get_response_dto_dict = transfer_bank_get_response_dto_instance.to_dict()
# create an instance of TransferBankGetResponseDTO from a dict
transfer_bank_get_response_dto_from_dict = TransferBankGetResponseDTO.from_dict(transfer_bank_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


