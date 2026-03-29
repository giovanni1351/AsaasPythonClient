# NotificationBatchUpdateRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer** | **str** | Identificador único do cliente no Asaas | 
**notifications** | [**List[NotificationBatchUpdateItemRequestDTO]**](NotificationBatchUpdateItemRequestDTO.md) | Lista de informações das notificações | [optional] 

## Example

```python
from asaas.models.notification_batch_update_request_dto import NotificationBatchUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of NotificationBatchUpdateRequestDTO from a JSON string
notification_batch_update_request_dto_instance = NotificationBatchUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(NotificationBatchUpdateRequestDTO.to_json())

# convert the object into a dict
notification_batch_update_request_dto_dict = notification_batch_update_request_dto_instance.to_dict()
# create an instance of NotificationBatchUpdateRequestDTO from a dict
notification_batch_update_request_dto_from_dict = NotificationBatchUpdateRequestDTO.from_dict(notification_batch_update_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


