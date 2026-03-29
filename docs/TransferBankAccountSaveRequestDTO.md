# TransferBankAccountSaveRequestDTO

Informe os dados da conta caso seja uma transferência para conta bancária

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bank** | [**TransferBankSaveRequestDTO**](TransferBankSaveRequestDTO.md) |  | [optional] 
**account_name** | **str** | Nome da conta bancária | [optional] 
**owner_name** | **str** | Nome do proprietário da conta bancária | 
**owner_birth_date** | **date** | Data de nascimento do proprietário da conta. Somente quando a conta bancária não pertencer ao mesmo CPF ou CNPJ da conta Asaas. | [optional] 
**cpf_cnpj** | **str** | CPF ou CNPJ do proprietário da conta bancária | 
**agency** | **str** | Número da agência sem dígito | 
**account** | **str** | Número da conta bancária sem dígito | 
**account_digit** | **str** | Dígito da conta bancária | 
**bank_account_type** | [**TransferBankAccountSaveRequestBankAccountType**](TransferBankAccountSaveRequestBankAccountType.md) |  | [optional] 
**ispb** | **str** | Identificador no Sistema de Pagamentos Brasileiro | [optional] 

## Example

```python
from asaas.models.transfer_bank_account_save_request_dto import TransferBankAccountSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferBankAccountSaveRequestDTO from a JSON string
transfer_bank_account_save_request_dto_instance = TransferBankAccountSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(TransferBankAccountSaveRequestDTO.to_json())

# convert the object into a dict
transfer_bank_account_save_request_dto_dict = transfer_bank_account_save_request_dto_instance.to_dict()
# create an instance of TransferBankAccountSaveRequestDTO from a dict
transfer_bank_account_save_request_dto_from_dict = TransferBankAccountSaveRequestDTO.from_dict(transfer_bank_account_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


