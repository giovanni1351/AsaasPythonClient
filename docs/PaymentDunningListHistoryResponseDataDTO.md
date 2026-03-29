# PaymentDunningListHistoryResponseDataDTO

Lista de objetos

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**PaymentDunningListHistoryResponseDataPaymentDunningHistoryStatus**](PaymentDunningListHistoryResponseDataPaymentDunningHistoryStatus.md) |  | [optional] 
**description** | **str** | Descrição do evento | [optional] 
**event_date** | **str** | Data em que ocorreu o evento | [optional] 

## Example

```python
from asaas.models.payment_dunning_list_history_response_data_dto import PaymentDunningListHistoryResponseDataDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDunningListHistoryResponseDataDTO from a JSON string
payment_dunning_list_history_response_data_dto_instance = PaymentDunningListHistoryResponseDataDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDunningListHistoryResponseDataDTO.to_json())

# convert the object into a dict
payment_dunning_list_history_response_data_dto_dict = payment_dunning_list_history_response_data_dto_instance.to_dict()
# create an instance of PaymentDunningListHistoryResponseDataDTO from a dict
payment_dunning_list_history_response_data_dto_from_dict = PaymentDunningListHistoryResponseDataDTO.from_dict(payment_dunning_list_history_response_data_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


