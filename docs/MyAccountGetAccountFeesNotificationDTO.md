# MyAccountGetAccountFeesNotificationDTO

Taxas de notificação

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_call_fee_value** | **float** | Taxas por ligação de robô de voz | [optional] 
**whats_app_fee_value** | **float** | Taxas por notificações via WhatsApp | [optional] 
**messaging_fee_value** | **float** | Taxas por envio de e-mails e SMS | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_notification_dto import MyAccountGetAccountFeesNotificationDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesNotificationDTO from a JSON string
my_account_get_account_fees_notification_dto_instance = MyAccountGetAccountFeesNotificationDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesNotificationDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_notification_dto_dict = my_account_get_account_fees_notification_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesNotificationDTO from a dict
my_account_get_account_fees_notification_dto_from_dict = MyAccountGetAccountFeesNotificationDTO.from_dict(my_account_get_account_fees_notification_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


