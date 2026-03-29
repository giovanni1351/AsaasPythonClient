# MyAccountGetAccountFeesTransferPixDTO

Taxas para transferências Pix

## Properties

| Name                                            | Type         | Description                                                       | Notes      |
| ----------------------------------------------- | ------------ | ----------------------------------------------------------------- | ---------- |
| **fee_value**                                   | **float**    | Taxa por envio de transferências via Pix                          | [optional] |
| **discount_value**                              | **float**    | Taxa promocional (Se houver)                                      | [optional] |
| **expiration_date**                             | **datetime** | Data de expiração da taxa promocional (Se houver)                 | [optional] |
| **considered_in_monthly_transfers_without_fee** | **bool**     | Indica se a quantidade de transações grátis mensais considera Pix | [optional] |

## Example

```python
from asaas.models.my_account_get_account_fees_transfer_pix_dto import MyAccountGetAccountFeesTransferPixDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesTransferPixDTO from a JSON string
my_account_get_account_fees_transfer_pix_dto_instance = MyAccountGetAccountFeesTransferPixDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesTransferPixDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_transfer_pix_dto_dict = my_account_get_account_fees_transfer_pix_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesTransferPixDTO from a dict
my_account_get_account_fees_transfer_pix_dto_from_dict = MyAccountGetAccountFeesTransferPixDTO.from_dict(my_account_get_account_fees_transfer_pix_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
