# TransferBankSaveRequestDTO

Dados do banco de destino

## Properties

| Name     | Type    | Description                                        | Notes |
| -------- | ------- | -------------------------------------------------- | ----- |
| **code** | **str** | Código de compensação do banco no sistema bancário |

## Example

```python
from asaas.models.transfer_bank_save_request_dto import TransferBankSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferBankSaveRequestDTO from a JSON string
transfer_bank_save_request_dto_instance = TransferBankSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(TransferBankSaveRequestDTO.to_json())

# convert the object into a dict
transfer_bank_save_request_dto_dict = transfer_bank_save_request_dto_instance.to_dict()
# create an instance of TransferBankSaveRequestDTO from a dict
transfer_bank_save_request_dto_from_dict = TransferBankSaveRequestDTO.from_dict(transfer_bank_save_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
