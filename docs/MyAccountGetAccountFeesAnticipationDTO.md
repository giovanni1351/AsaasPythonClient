# MyAccountGetAccountFeesAnticipationDTO

Taxas de antecipação

## Properties

| Name            | Type                                                                                                        | Description | Notes      |
| --------------- | ----------------------------------------------------------------------------------------------------------- | ----------- | ---------- |
| **credit_card** | [**MyAccountGetAccountFeesAnticipationCreditCardDTO**](MyAccountGetAccountFeesAnticipationCreditCardDTO.md) |             | [optional] |
| **bank_slip**   | [**MyAccountGetAccountFeesAnticipationBankSlipDTO**](MyAccountGetAccountFeesAnticipationBankSlipDTO.md)     |             | [optional] |

## Example

```python
from asaas.models.my_account_get_account_fees_anticipation_dto import MyAccountGetAccountFeesAnticipationDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesAnticipationDTO from a JSON string
my_account_get_account_fees_anticipation_dto_instance = MyAccountGetAccountFeesAnticipationDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesAnticipationDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_anticipation_dto_dict = my_account_get_account_fees_anticipation_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesAnticipationDTO from a dict
my_account_get_account_fees_anticipation_dto_from_dict = MyAccountGetAccountFeesAnticipationDTO.from_dict(my_account_get_account_fees_anticipation_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
