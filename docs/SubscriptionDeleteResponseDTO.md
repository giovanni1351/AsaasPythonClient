# SubscriptionDeleteResponseDTO

## Properties

| Name        | Type     | Description                                | Notes      |
| ----------- | -------- | ------------------------------------------ | ---------- |
| **deleted** | **bool** | Informa se a assinatura foi removida       | [optional] |
| **id**      | **str**  | Identificador único da assinatura no Asaas | [optional] |

## Example

```python
from asaas.models.subscription_delete_response_dto import SubscriptionDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionDeleteResponseDTO from a JSON string
subscription_delete_response_dto_instance = SubscriptionDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionDeleteResponseDTO.to_json())

# convert the object into a dict
subscription_delete_response_dto_dict = subscription_delete_response_dto_instance.to_dict()
# create an instance of SubscriptionDeleteResponseDTO from a dict
subscription_delete_response_dto_from_dict = SubscriptionDeleteResponseDTO.from_dict(subscription_delete_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
