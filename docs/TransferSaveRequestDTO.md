# TransferSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | Valor a ser transferido | 
**bank_account** | [**TransferBankAccountSaveRequestDTO**](TransferBankAccountSaveRequestDTO.md) |  | [optional] 
**operation_type** | [**TransferSaveRequestTransferType**](TransferSaveRequestTransferType.md) |  | [optional] 
**pix_address_key** | **str** | Informe a chave Pix caso seja uma transferência para chave Pix | [optional] 
**pix_address_key_type** | [**TransferSaveRequestPixAddressKeyType**](TransferSaveRequestPixAddressKeyType.md) |  | [optional] 
**description** | **str** | Transferências via Pix permitem descrição | [optional] 
**schedule_date** | **date** | Para transferências agendadas, caso não informado o pagamento é instantâneo | [optional] 
**external_reference** | **str** | Identificador da transferência no seu sistema | [optional] 
**recurring** | [**TransferRecurringSaveRequestDTO**](TransferRecurringSaveRequestDTO.md) |  | [optional] 

## Example

```python
from asaas.models.transfer_save_request_dto import TransferSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferSaveRequestDTO from a JSON string
transfer_save_request_dto_instance = TransferSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(TransferSaveRequestDTO.to_json())

# convert the object into a dict
transfer_save_request_dto_dict = transfer_save_request_dto_instance.to_dict()
# create an instance of TransferSaveRequestDTO from a dict
transfer_save_request_dto_from_dict = TransferSaveRequestDTO.from_dict(transfer_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


