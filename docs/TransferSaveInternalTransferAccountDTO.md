# TransferSaveInternalTransferAccountDTO

Informações básicas da conta de destino

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Nome da conta de destino | [optional] 
**cpf_cnpj** | **str** | CPF ou CNPJ da conta de destino | [optional] 
**agency** | **str** | Código da agência da conta de destino | [optional] 
**account** | **str** | Número da conta de destino | [optional] 
**account_digit** | **str** | Dígito da conta de destino | [optional] 

## Example

```python
from asaas.models.transfer_save_internal_transfer_account_dto import TransferSaveInternalTransferAccountDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferSaveInternalTransferAccountDTO from a JSON string
transfer_save_internal_transfer_account_dto_instance = TransferSaveInternalTransferAccountDTO.from_json(json)
# print the JSON string representation of the object
print(TransferSaveInternalTransferAccountDTO.to_json())

# convert the object into a dict
transfer_save_internal_transfer_account_dto_dict = transfer_save_internal_transfer_account_dto_instance.to_dict()
# create an instance of TransferSaveInternalTransferAccountDTO from a dict
transfer_save_internal_transfer_account_dto_from_dict = TransferSaveInternalTransferAccountDTO.from_dict(transfer_save_internal_transfer_account_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


