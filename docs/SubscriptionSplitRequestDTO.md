# SubscriptionSplitRequestDTO

Informações de split

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**wallet_id** | **str** | Identificador da carteira Asaas que será transferido | 
**fixed_value** | **float** | Valor fixo a ser transferido para a conta quando a cobrança for recebida | [optional] 
**percentual_value** | **float** | Percentual sobre o valor líquido da cobrança a ser transferido quando for recebida | [optional] 
**external_reference** | **str** | Identificador do split no seu sistema | [optional] 
**description** | **str** | Descrição do split | [optional] 

## Example

```python
from asaas.models.subscription_split_request_dto import SubscriptionSplitRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionSplitRequestDTO from a JSON string
subscription_split_request_dto_instance = SubscriptionSplitRequestDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionSplitRequestDTO.to_json())

# convert the object into a dict
subscription_split_request_dto_dict = subscription_split_request_dto_instance.to_dict()
# create an instance of SubscriptionSplitRequestDTO from a dict
subscription_split_request_dto_from_dict = SubscriptionSplitRequestDTO.from_dict(subscription_split_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


