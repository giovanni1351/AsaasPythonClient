# WebhookConfigUpdateRequestDTO

## Properties

| Name            | Type                                                                                          | Description                                          | Notes      |
| --------------- | --------------------------------------------------------------------------------------------- | ---------------------------------------------------- | ---------- |
| **name**        | **str**                                                                                       | Nome do Webhook                                      | [optional] |
| **url**         | **str**                                                                                       | URL de destino dos eventos                           | [optional] |
| **send_type**   | [**WebhookConfigUpdateRequestWebhookSendType**](WebhookConfigUpdateRequestWebhookSendType.md) |                                                      | [optional] |
| **enabled**     | **bool**                                                                                      | Definir se o Webhook está ativo                      | [optional] |
| **interrupted** | **bool**                                                                                      | Definir se a fila de sincronização está interrompida | [optional] |
| **auth_token**  | **str**                                                                                       | Token de autenticação do Webhook                     | [optional] |
| **events**      | [**List[WebhookConfigUpdateRequestWebhookEvent]**](WebhookConfigUpdateRequestWebhookEvent.md) | Lista dos eventos que este Webhook irá observar      | [optional] |

## Example

```python
from asaas.models.webhook_config_update_request_dto import WebhookConfigUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookConfigUpdateRequestDTO from a JSON string
webhook_config_update_request_dto_instance = WebhookConfigUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(WebhookConfigUpdateRequestDTO.to_json())

# convert the object into a dict
webhook_config_update_request_dto_dict = webhook_config_update_request_dto_instance.to_dict()
# create an instance of WebhookConfigUpdateRequestDTO from a dict
webhook_config_update_request_dto_from_dict = WebhookConfigUpdateRequestDTO.from_dict(webhook_config_update_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
