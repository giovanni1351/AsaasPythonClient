# WebhookConfigDeleteResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted** | **bool** | Indica se o Webhook foi removido | [optional] 
**id** | **str** | Identificador único do webhook removido | [optional] 

## Example

```python
from asaas.models.webhook_config_delete_response_dto import WebhookConfigDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookConfigDeleteResponseDTO from a JSON string
webhook_config_delete_response_dto_instance = WebhookConfigDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(WebhookConfigDeleteResponseDTO.to_json())

# convert the object into a dict
webhook_config_delete_response_dto_dict = webhook_config_delete_response_dto_instance.to_dict()
# create an instance of WebhookConfigDeleteResponseDTO from a dict
webhook_config_delete_response_dto_from_dict = WebhookConfigDeleteResponseDTO.from_dict(webhook_config_delete_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


