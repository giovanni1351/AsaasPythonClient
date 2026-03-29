# NotificationBatchUpdateItemRequestDTO

Lista de informações das notificações

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único da notificação a ser atualizada | 
**enabled** | **bool** | Habilita/desabilita a notificação | [optional] 
**email_enabled_for_provider** | **bool** | habilita/desabilita o email enviado para você | [optional] 
**sms_enabled_for_provider** | **bool** | habilita/desabilita o SMS enviado para você | [optional] 
**email_enabled_for_customer** | **bool** | habilita/desabilita o email enviado para o seu cliente | [optional] 
**sms_enabled_for_customer** | **bool** | habilita/desabilita o SMS enviado para o seu cliente | [optional] 
**phone_call_enabled_for_customer** | **bool** | habilita/desabilita a notificação por voz enviada para o seu cliente | [optional] 
**whatsapp_enabled_for_customer** | **bool** | habilita/desabilita a mensagem de WhatsApp para seu cliente | [optional] 
**schedule_offset** | **int** | Especifica quantos dias antes do vencimento a notificação deve se enviada.  Para o evento  &#x60;PAYMENT_DUEDATE_WARNING&#x60; os valores aceitos são: &#x60;0&#x60;, &#x60;5&#x60;, &#x60;10&#x60;, &#x60;15&#x60; e &#x60;30&#x60;  Para o evento &#x60;PAYMENT_OVERDUE&#x60; os valores aceitos são: &#x60;1&#x60;, &#x60;7&#x60;, &#x60;15&#x60; e &#x60;30&#x60; | [optional] 

## Example

```python
from asaas.models.notification_batch_update_item_request_dto import NotificationBatchUpdateItemRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of NotificationBatchUpdateItemRequestDTO from a JSON string
notification_batch_update_item_request_dto_instance = NotificationBatchUpdateItemRequestDTO.from_json(json)
# print the JSON string representation of the object
print(NotificationBatchUpdateItemRequestDTO.to_json())

# convert the object into a dict
notification_batch_update_item_request_dto_dict = notification_batch_update_item_request_dto_instance.to_dict()
# create an instance of NotificationBatchUpdateItemRequestDTO from a dict
notification_batch_update_item_request_dto_from_dict = NotificationBatchUpdateItemRequestDTO.from_dict(notification_batch_update_item_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


