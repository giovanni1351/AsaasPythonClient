# WebhookConfigGetResponseDTO

## Properties

| Name                         | Type                                                                                      | Description                                                         | Notes      |
| ---------------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ---------- |
| **id**                       | **str**                                                                                   | Identificador único do Webhook                                      | [optional] |
| **name**                     | **str**                                                                                   | Nome do Webhook                                                     | [optional] |
| **url**                      | **str**                                                                                   | URL do Webhook                                                      | [optional] |
| **email**                    | **str**                                                                                   | E-mail que receberá notificações sobre o Webhook                    | [optional] |
| **enabled**                  | **bool**                                                                                  | Indica se o Webhook está ativo                                      | [optional] |
| **interrupted**              | **bool**                                                                                  | Definir se a fila de sincronização está interrompida                | [optional] |
| **api_version**              | **int**                                                                                   | Versão da API                                                       | [optional] |
| **has_auth_token**           | **bool**                                                                                  | Indica se existe um token de autenticação registrado para o webhook | [optional] |
| **send_type**                | [**WebhookConfigGetResponseWebhookSendType**](WebhookConfigGetResponseWebhookSendType.md) |                                                                     | [optional] |
| **penalized_requests_count** | **int**                                                                                   | Quantidade de requests penalizados                                  | [optional] |
| **events**                   | [**List[WebhookConfigGetResponseWebhookEvent]**](WebhookConfigGetResponseWebhookEvent.md) | Lista de eventos enviados pelo Webhook                              | [optional] |

## Example

```python
from asaas.models.webhook_config_get_response_dto import WebhookConfigGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookConfigGetResponseDTO from a JSON string
webhook_config_get_response_dto_instance = WebhookConfigGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(WebhookConfigGetResponseDTO.to_json())

# convert the object into a dict
webhook_config_get_response_dto_dict = webhook_config_get_response_dto_instance.to_dict()
# create an instance of WebhookConfigGetResponseDTO from a dict
webhook_config_get_response_dto_from_dict = WebhookConfigGetResponseDTO.from_dict(webhook_config_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
