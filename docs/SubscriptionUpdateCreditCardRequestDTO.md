# SubscriptionUpdateCreditCardRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**credit_card** | [**CreditCardRequestDTO**](CreditCardRequestDTO.md) |  | 
**credit_card_holder_info** | [**CreditCardHolderInfoRequestDTO**](CreditCardHolderInfoRequestDTO.md) |  | 
**credit_card_token** | **str** | Token do cartão de crédito para uso da funcionalidade de tokenização de cartão de crédito. Caso informado, os campos acima não são obrigatórios. | [optional] 
**remote_ip** | **str** | IP de onde o cliente está fazendo a compra. Não deve ser informado o IP do seu servidor. | 

## Example

```python
from asaas.models.subscription_update_credit_card_request_dto import SubscriptionUpdateCreditCardRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionUpdateCreditCardRequestDTO from a JSON string
subscription_update_credit_card_request_dto_instance = SubscriptionUpdateCreditCardRequestDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionUpdateCreditCardRequestDTO.to_json())

# convert the object into a dict
subscription_update_credit_card_request_dto_dict = subscription_update_credit_card_request_dto_instance.to_dict()
# create an instance of SubscriptionUpdateCreditCardRequestDTO from a dict
subscription_update_credit_card_request_dto_from_dict = SubscriptionUpdateCreditCardRequestDTO.from_dict(subscription_update_credit_card_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


