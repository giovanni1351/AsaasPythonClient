# FinanceGetPaymentStatisticsResponseDTO

## Properties

| Name          | Type      | Description             | Notes      |
| ------------- | --------- | ----------------------- | ---------- |
| **quantity**  | **int**   | Quantidade de cobranças | [optional] |
| **value**     | **float** | Valor total             | [optional] |
| **net_value** | **float** | Valor líquido total     | [optional] |

## Example

```python
from asaas.models.finance_get_payment_statistics_response_dto import FinanceGetPaymentStatisticsResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FinanceGetPaymentStatisticsResponseDTO from a JSON string
finance_get_payment_statistics_response_dto_instance = FinanceGetPaymentStatisticsResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FinanceGetPaymentStatisticsResponseDTO.to_json())

# convert the object into a dict
finance_get_payment_statistics_response_dto_dict = finance_get_payment_statistics_response_dto_instance.to_dict()
# create an instance of FinanceGetPaymentStatisticsResponseDTO from a dict
finance_get_payment_statistics_response_dto_from_dict = FinanceGetPaymentStatisticsResponseDTO.from_dict(finance_get_payment_statistics_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
