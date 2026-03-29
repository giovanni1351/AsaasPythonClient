# RecurringPixTransactionListItemsResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[PixRecurringTransactionGetItemResponseDTO]**](PixRecurringTransactionGetItemResponseDTO.md) | Lista de objetos | [optional] 

## Example

```python
from asaas.models.recurring_pix_transaction_list_items_response_dto import RecurringPixTransactionListItemsResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of RecurringPixTransactionListItemsResponseDTO from a JSON string
recurring_pix_transaction_list_items_response_dto_instance = RecurringPixTransactionListItemsResponseDTO.from_json(json)
# print the JSON string representation of the object
print(RecurringPixTransactionListItemsResponseDTO.to_json())

# convert the object into a dict
recurring_pix_transaction_list_items_response_dto_dict = recurring_pix_transaction_list_items_response_dto_instance.to_dict()
# create an instance of RecurringPixTransactionListItemsResponseDTO from a dict
recurring_pix_transaction_list_items_response_dto_from_dict = RecurringPixTransactionListItemsResponseDTO.from_dict(recurring_pix_transaction_list_items_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


