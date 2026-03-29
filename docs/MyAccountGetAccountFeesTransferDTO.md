# MyAccountGetAccountFeesTransferDTO

Taxas de transferências

## Properties

| Name                              | Type                                                                                  | Description                             | Notes      |
| --------------------------------- | ------------------------------------------------------------------------------------- | --------------------------------------- | ---------- |
| **monthly_transfers_without_fee** | **int**                                                                               | Quantidade de transações grátis mensais | [optional] |
| **ted**                           | [**MyAccountGetAccountFeesTransferTedDTO**](MyAccountGetAccountFeesTransferTedDTO.md) |                                         | [optional] |
| **pix**                           | [**MyAccountGetAccountFeesTransferPixDTO**](MyAccountGetAccountFeesTransferPixDTO.md) |                                         | [optional] |

## Example

```python
from asaas.models.my_account_get_account_fees_transfer_dto import MyAccountGetAccountFeesTransferDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesTransferDTO from a JSON string
my_account_get_account_fees_transfer_dto_instance = MyAccountGetAccountFeesTransferDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesTransferDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_transfer_dto_dict = my_account_get_account_fees_transfer_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesTransferDTO from a dict
my_account_get_account_fees_transfer_dto_from_dict = MyAccountGetAccountFeesTransferDTO.from_dict(my_account_get_account_fees_transfer_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
