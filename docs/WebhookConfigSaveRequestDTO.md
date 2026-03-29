# WebhookConfigSaveRequestDTO

Array com as configurações de Webhooks desejadas

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Nome do Webhook | [optional] 
**url** | **str** | URL de destino dos eventos | [optional] 
**email** | **str** | E-mail que receberá notificações sobre o Webhook | [optional] 
**enabled** | **bool** | Definir se o Webhook está ativo | [optional] 
**interrupted** | **bool** | Definir se a fila de sincronização está interrompida | [optional] 
**api_version** | **int** | Versão da API | [optional] 
**auth_token** | **str** | Token de autenticação do Webhook | [optional] 
**send_type** | [**WebhookConfigSaveRequestWebhookSendType**](WebhookConfigSaveRequestWebhookSendType.md) |  | [optional] 
**events** | [**List[WebhookConfigSaveRequestWebhookEvent]**](WebhookConfigSaveRequestWebhookEvent.md) | Lista de eventos enviados pelo Webhook | [optional] 

## Example

```python
from asaas.models.webhook_config_save_request_dto import WebhookConfigSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookConfigSaveRequestDTO from a JSON string
webhook_config_save_request_dto_instance = WebhookConfigSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(WebhookConfigSaveRequestDTO.to_json())

# convert the object into a dict
webhook_config_save_request_dto_dict = webhook_config_save_request_dto_instance.to_dict()
# create an instance of WebhookConfigSaveRequestDTO from a dict
webhook_config_save_request_dto_from_dict = WebhookConfigSaveRequestDTO.from_dict(webhook_config_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


