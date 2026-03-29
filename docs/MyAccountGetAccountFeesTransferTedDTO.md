# MyAccountGetAccountFeesTransferTedDTO

Taxas para transferências TED

## Properties

| Name                                            | Type      | Description                                                       | Notes      |
| ----------------------------------------------- | --------- | ----------------------------------------------------------------- | ---------- |
| **fee_value**                                   | **float** | Taxa por transferência via TED                                    | [optional] |
| **considered_in_monthly_transfers_without_fee** | **bool**  | Indica se a quantidade de transações grátis mensais considera TED | [optional] |

## Example

```python
from asaas.models.my_account_get_account_fees_transfer_ted_dto import MyAccountGetAccountFeesTransferTedDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesTransferTedDTO from a JSON string
my_account_get_account_fees_transfer_ted_dto_instance = MyAccountGetAccountFeesTransferTedDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesTransferTedDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_transfer_ted_dto_dict = my_account_get_account_fees_transfer_ted_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesTransferTedDTO from a dict
my_account_get_account_fees_transfer_ted_dto_from_dict = MyAccountGetAccountFeesTransferTedDTO.from_dict(my_account_get_account_fees_transfer_ted_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
