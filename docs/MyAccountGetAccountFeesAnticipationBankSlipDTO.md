# MyAccountGetAccountFeesAnticipationBankSlipDTO

Tarifa de antecipações em boletos

## Properties

| Name                       | Type      | Description                          | Notes      |
| -------------------------- | --------- | ------------------------------------ | ---------- |
| **monthly_fee_percentage** | **float** | Taxa ao mês para cobranças em boleto | [optional] |

## Example

```python
from asaas.models.my_account_get_account_fees_anticipation_bank_slip_dto import MyAccountGetAccountFeesAnticipationBankSlipDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesAnticipationBankSlipDTO from a JSON string
my_account_get_account_fees_anticipation_bank_slip_dto_instance = MyAccountGetAccountFeesAnticipationBankSlipDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesAnticipationBankSlipDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_anticipation_bank_slip_dto_dict = my_account_get_account_fees_anticipation_bank_slip_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesAnticipationBankSlipDTO from a dict
my_account_get_account_fees_anticipation_bank_slip_dto_from_dict = MyAccountGetAccountFeesAnticipationBankSlipDTO.from_dict(my_account_get_account_fees_anticipation_bank_slip_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
