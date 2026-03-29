# FinanceBalanceResponseDTO

## Properties

| Name        | Type      | Description    | Notes      |
| ----------- | --------- | -------------- | ---------- |
| **balance** | **float** | Saldo da conta | [optional] |

## Example

```python
from asaas.models.finance_balance_response_dto import FinanceBalanceResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FinanceBalanceResponseDTO from a JSON string
finance_balance_response_dto_instance = FinanceBalanceResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FinanceBalanceResponseDTO.to_json())

# convert the object into a dict
finance_balance_response_dto_dict = finance_balance_response_dto_instance.to_dict()
# create an instance of FinanceBalanceResponseDTO from a dict
finance_balance_response_dto_from_dict = FinanceBalanceResponseDTO.from_dict(finance_balance_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
