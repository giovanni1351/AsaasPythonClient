# CheckoutSessionCallbackDTO

Informações de redirecionamento automático após pagamento na tela do checkout

## Properties

| Name            | Type    | Description                                     | Notes      |
| --------------- | ------- | ----------------------------------------------- | ---------- |
| **success_url** | **str** | URL de direcionamento para checkout com sucesso |
| **cancel_url**  | **str** | URL de direciomento para checkout cancelado     |
| **expired_url** | **str** | URL de direcionamento para checkout expirado    | [optional] |

## Example

```python
from asaas.models.checkout_session_callback_dto import CheckoutSessionCallbackDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSessionCallbackDTO from a JSON string
checkout_session_callback_dto_instance = CheckoutSessionCallbackDTO.from_json(json)
# print the JSON string representation of the object
print(CheckoutSessionCallbackDTO.to_json())

# convert the object into a dict
checkout_session_callback_dto_dict = checkout_session_callback_dto_instance.to_dict()
# create an instance of CheckoutSessionCallbackDTO from a dict
checkout_session_callback_dto_from_dict = CheckoutSessionCallbackDTO.from_dict(checkout_session_callback_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
