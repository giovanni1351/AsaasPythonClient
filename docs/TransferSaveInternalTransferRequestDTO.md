# TransferSaveInternalTransferRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | Valor a ser transferido | 
**wallet_id** | **str** | WalletId da conta destino | 
**external_reference** | **str** | Identificador da transferência no seu sistema | [optional] 

## Example

```python
from asaas.models.transfer_save_internal_transfer_request_dto import TransferSaveInternalTransferRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferSaveInternalTransferRequestDTO from a JSON string
transfer_save_internal_transfer_request_dto_instance = TransferSaveInternalTransferRequestDTO.from_json(json)
# print the JSON string representation of the object
print(TransferSaveInternalTransferRequestDTO.to_json())

# convert the object into a dict
transfer_save_internal_transfer_request_dto_dict = transfer_save_internal_transfer_request_dto_instance.to_dict()
# create an instance of TransferSaveInternalTransferRequestDTO from a dict
transfer_save_internal_transfer_request_dto_from_dict = TransferSaveInternalTransferRequestDTO.from_dict(transfer_save_internal_transfer_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


