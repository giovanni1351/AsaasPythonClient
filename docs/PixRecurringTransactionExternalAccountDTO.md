# PixRecurringTransactionExternalAccountDTO

Informações sobre o recebedor

## Properties

| Name                           | Type    | Description                      | Notes      |
| ------------------------------ | ------- | -------------------------------- | ---------- |
| **name**                       | **str** | Nome do recebedor                | [optional] |
| **financial_institution_name** | **str** | Nome da instituição de pagamento | [optional] |
| **cpf_cnpj**                   | **str** | CPF ou CNPJ do recebedor         | [optional] |
| **pix_key**                    | **str** | Chave Pix do recebedor           | [optional] |

## Example

```python
from asaas.models.pix_recurring_transaction_external_account_dto import PixRecurringTransactionExternalAccountDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixRecurringTransactionExternalAccountDTO from a JSON string
pix_recurring_transaction_external_account_dto_instance = PixRecurringTransactionExternalAccountDTO.from_json(json)
# print the JSON string representation of the object
print(PixRecurringTransactionExternalAccountDTO.to_json())

# convert the object into a dict
pix_recurring_transaction_external_account_dto_dict = pix_recurring_transaction_external_account_dto_instance.to_dict()
# create an instance of PixRecurringTransactionExternalAccountDTO from a dict
pix_recurring_transaction_external_account_dto_from_dict = PixRecurringTransactionExternalAccountDTO.from_dict(pix_recurring_transaction_external_account_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
