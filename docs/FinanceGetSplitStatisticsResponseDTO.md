# FinanceGetSplitStatisticsResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**income** | **float** | Valores a receber | [optional] 
**value** | **float** | Valores a serem enviados | [optional] 

## Example

```python
from asaas.models.finance_get_split_statistics_response_dto import FinanceGetSplitStatisticsResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FinanceGetSplitStatisticsResponseDTO from a JSON string
finance_get_split_statistics_response_dto_instance = FinanceGetSplitStatisticsResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FinanceGetSplitStatisticsResponseDTO.to_json())

# convert the object into a dict
finance_get_split_statistics_response_dto_dict = finance_get_split_statistics_response_dto_instance.to_dict()
# create an instance of FinanceGetSplitStatisticsResponseDTO from a dict
finance_get_split_statistics_response_dto_from_dict = FinanceGetSplitStatisticsResponseDTO.from_dict(finance_get_split_statistics_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


