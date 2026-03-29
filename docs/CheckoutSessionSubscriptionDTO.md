# CheckoutSessionSubscriptionDTO

Detalhes da assinatura, obrigatório se chargeTypes incluir `RECURRENT`

## Properties

| Name              | Type                                                                        | Description                                  | Notes      |
| ----------------- | --------------------------------------------------------------------------- | -------------------------------------------- | ---------- |
| **cycle**         | [**CheckoutSessionSubscriptionCycle**](CheckoutSessionSubscriptionCycle.md) |                                              | [optional] |
| **end_date**      | **date**                                                                    | Data limite para vencimento das cobranças    | [optional] |
| **next_due_date** | **date**                                                                    | Vencimento do próximo pagamento a ser gerado | [optional] |

## Example

```python
from asaas.models.checkout_session_subscription_dto import CheckoutSessionSubscriptionDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSessionSubscriptionDTO from a JSON string
checkout_session_subscription_dto_instance = CheckoutSessionSubscriptionDTO.from_json(json)
# print the JSON string representation of the object
print(CheckoutSessionSubscriptionDTO.to_json())

# convert the object into a dict
checkout_session_subscription_dto_dict = checkout_session_subscription_dto_instance.to_dict()
# create an instance of CheckoutSessionSubscriptionDTO from a dict
checkout_session_subscription_dto_from_dict = CheckoutSessionSubscriptionDTO.from_dict(checkout_session_subscription_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
