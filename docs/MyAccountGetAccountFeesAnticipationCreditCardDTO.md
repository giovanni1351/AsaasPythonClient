# MyAccountGetAccountFeesAnticipationCreditCardDTO

Tarifa de antecipações em cartão de crédito

## Properties

| Name                              | Type      | Description                           | Notes      |
| --------------------------------- | --------- | ------------------------------------- | ---------- |
| **detached_monthly_fee_value**    | **float** | Taxa ao mês para cobranças à vista    | [optional] |
| **installment_monthly_fee_value** | **int**   | Taxa ao mês para cobranças parceladas | [optional] |

## Example

```python
from asaas.models.my_account_get_account_fees_anticipation_credit_card_dto import MyAccountGetAccountFeesAnticipationCreditCardDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesAnticipationCreditCardDTO from a JSON string
my_account_get_account_fees_anticipation_credit_card_dto_instance = MyAccountGetAccountFeesAnticipationCreditCardDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesAnticipationCreditCardDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_anticipation_credit_card_dto_dict = my_account_get_account_fees_anticipation_credit_card_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesAnticipationCreditCardDTO from a dict
my_account_get_account_fees_anticipation_credit_card_dto_from_dict = MyAccountGetAccountFeesAnticipationCreditCardDTO.from_dict(my_account_get_account_fees_anticipation_credit_card_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
