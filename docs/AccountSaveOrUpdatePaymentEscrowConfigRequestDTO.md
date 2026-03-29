# AccountSaveOrUpdatePaymentEscrowConfigRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**days_to_expire** | **int** | Quantidade de dias para expiração do bloqueio dos valores em garantia na Conta Escrow | 
**enabled** | **bool** | Indica se a Conta Escrow está habilitada | [optional] 
**is_fee_payer** | **bool** | Indica se a subconta é responsável pelo pagamento da taxa da Conta Escrow. Caso não informado, a taxa será paga pela conta principal | [optional] 

## Example

```python
from asaas.models.account_save_or_update_payment_escrow_config_request_dto import AccountSaveOrUpdatePaymentEscrowConfigRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountSaveOrUpdatePaymentEscrowConfigRequestDTO from a JSON string
account_save_or_update_payment_escrow_config_request_dto_instance = AccountSaveOrUpdatePaymentEscrowConfigRequestDTO.from_json(json)
# print the JSON string representation of the object
print(AccountSaveOrUpdatePaymentEscrowConfigRequestDTO.to_json())

# convert the object into a dict
account_save_or_update_payment_escrow_config_request_dto_dict = account_save_or_update_payment_escrow_config_request_dto_instance.to_dict()
# create an instance of AccountSaveOrUpdatePaymentEscrowConfigRequestDTO from a dict
account_save_or_update_payment_escrow_config_request_dto_from_dict = AccountSaveOrUpdatePaymentEscrowConfigRequestDTO.from_dict(account_save_or_update_payment_escrow_config_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


