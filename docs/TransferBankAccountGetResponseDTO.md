# TransferBankAccountGetResponseDTO

Dados da conta bancária

## Properties

| Name                | Type                                                            | Description                                   | Notes      |
| ------------------- | --------------------------------------------------------------- | --------------------------------------------- | ---------- |
| **bank**            | [**TransferBankGetResponseDTO**](TransferBankGetResponseDTO.md) |                                               | [optional] |
| **account_name**    | **str**                                                         | Nome da conta bancária                        | [optional] |
| **owner_name**      | **str**                                                         | Nome do proprietário da conta bancária        | [optional] |
| **cpf_cnpj**        | **str**                                                         | CPF ou CNPJ do proprietário da conta bancária | [optional] |
| **agency**          | **str**                                                         | Número da agência sem dígito                  | [optional] |
| **agency_digit**    | **str**                                                         | Dígito da agência                             | [optional] |
| **account**         | **str**                                                         | Número da conta bancária sem dígito           | [optional] |
| **account_digit**   | **str**                                                         | Dígito da conta bancária                      | [optional] |
| **pix_address_key** | **str**                                                         | Endereço da chave Pix                         | [optional] |

## Example

```python
from asaas.models.transfer_bank_account_get_response_dto import TransferBankAccountGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferBankAccountGetResponseDTO from a JSON string
transfer_bank_account_get_response_dto_instance = TransferBankAccountGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(TransferBankAccountGetResponseDTO.to_json())

# convert the object into a dict
transfer_bank_account_get_response_dto_dict = transfer_bank_account_get_response_dto_instance.to_dict()
# create an instance of TransferBankAccountGetResponseDTO from a dict
transfer_bank_account_get_response_dto_from_dict = TransferBankAccountGetResponseDTO.from_dict(transfer_bank_account_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
