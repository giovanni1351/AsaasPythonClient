# NotificationGetResponseDTO

Lista de informações das notificações

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo do objeto | [optional] 
**id** | **str** | Identificador único da notificação | [optional] 
**customer** | **str** | Identificador único do cliente | [optional] 
**enabled** | **bool** | Indica se a notificação está habilitada | [optional] 
**email_enabled_for_provider** | **bool** | Indica se o e-mail enviado para você está habilitado ou desabilitado | [optional] 
**sms_enabled_for_provider** | **bool** | Indica se o SMS enviado para você está habilitado ou desabilitado | [optional] 
**email_enabled_for_customer** | **bool** | Indica se o e-mail enviado para o cliente está habilitado ou desabilitado | [optional] 
**sms_enabled_for_customer** | **bool** | Indica se o SMS enviado para o cliente está habilitado ou desabilitado | [optional] 
**phone_call_enabled_for_customer** | **bool** | Indica se notificação por voz para o cliente está habilitada ou desabilitada | [optional] 
**whatsapp_enabled_for_customer** | **bool** | Indica se a notificação por Whatsapp enviado para o cliente está habilitada ou desabilitada | [optional] 
**event** | [**NotificationGetResponseNotificationEvent**](NotificationGetResponseNotificationEvent.md) |  | [optional] 
**schedule_offset** | **int** | Especifica quantos dias antes do vencimento a notificação deve se enviada. Válido para os eventos &#x60;PAYMENT_DUEDATE_WARNING&#x60; e &#x60;PAYMENT_OVERDUE&#x60; | [optional] 
**deleted** | **bool** | Indica se a notificação foi deletada | [optional] [default to True]

## Example

```python
from asaas.models.notification_get_response_dto import NotificationGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of NotificationGetResponseDTO from a JSON string
notification_get_response_dto_instance = NotificationGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(NotificationGetResponseDTO.to_json())

# convert the object into a dict
notification_get_response_dto_dict = notification_get_response_dto_instance.to_dict()
# create an instance of NotificationGetResponseDTO from a dict
notification_get_response_dto_from_dict = NotificationGetResponseDTO.from_dict(notification_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


