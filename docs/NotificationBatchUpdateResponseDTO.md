# NotificationBatchUpdateResponseDTO

## Properties

| Name              | Type                                                                  | Description                           | Notes      |
| ----------------- | --------------------------------------------------------------------- | ------------------------------------- | ---------- |
| **notifications** | [**List[NotificationGetResponseDTO]**](NotificationGetResponseDTO.md) | Lista de informações das notificações | [optional] |

## Example

```python
from asaas.models.notification_batch_update_response_dto import NotificationBatchUpdateResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of NotificationBatchUpdateResponseDTO from a JSON string
notification_batch_update_response_dto_instance = NotificationBatchUpdateResponseDTO.from_json(json)
# print the JSON string representation of the object
print(NotificationBatchUpdateResponseDTO.to_json())

# convert the object into a dict
notification_batch_update_response_dto_dict = notification_batch_update_response_dto_instance.to_dict()
# create an instance of NotificationBatchUpdateResponseDTO from a dict
notification_batch_update_response_dto_from_dict = NotificationBatchUpdateResponseDTO.from_dict(notification_batch_update_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
