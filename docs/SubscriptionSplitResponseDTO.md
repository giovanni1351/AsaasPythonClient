# SubscriptionSplitResponseDTO

Informações de split

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**wallet_id** | **str** | Identificador da carteira Asaas que será transferido | [optional] 
**fixed_value** | **float** | Valor fixo a ser transferido para a conta quando a cobrança for recebida | [optional] 
**percentual_value** | **float** | Percentual sobre o valor líquido da cobrança a ser transferido quando for recebida | [optional] 
**external_reference** | **str** | Identificador do split no seu sistema | [optional] 
**description** | **str** | Descrição do split | [optional] 
**status** | [**SubscriptionSplitResponseSubscriptionSplitStatus**](SubscriptionSplitResponseSubscriptionSplitStatus.md) |  | [optional] 
**disabled_reason** | [**SubscriptionSplitResponseSubscriptionSplitDisabledReason**](SubscriptionSplitResponseSubscriptionSplitDisabledReason.md) |  | [optional] 

## Example

```python
from asaas.models.subscription_split_response_dto import SubscriptionSplitResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionSplitResponseDTO from a JSON string
subscription_split_response_dto_instance = SubscriptionSplitResponseDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionSplitResponseDTO.to_json())

# convert the object into a dict
subscription_split_response_dto_dict = subscription_split_response_dto_instance.to_dict()
# create an instance of SubscriptionSplitResponseDTO from a dict
subscription_split_response_dto_from_dict = SubscriptionSplitResponseDTO.from_dict(subscription_split_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


