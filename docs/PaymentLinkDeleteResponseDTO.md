# PaymentLinkDeleteResponseDTO

## Properties

| Name        | Type     | Description                                            | Notes      |
| ----------- | -------- | ------------------------------------------------------ | ---------- |
| **deleted** | **bool** | Indica se o link de pagamento foi removido             | [optional] |
| **id**      | **str**  | Identificador único do seu link de pagamentos no Asaas | [optional] |

## Example

```python
from asaas.models.payment_link_delete_response_dto import PaymentLinkDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLinkDeleteResponseDTO from a JSON string
payment_link_delete_response_dto_instance = PaymentLinkDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLinkDeleteResponseDTO.to_json())

# convert the object into a dict
payment_link_delete_response_dto_dict = payment_link_delete_response_dto_instance.to_dict()
# create an instance of PaymentLinkDeleteResponseDTO from a dict
payment_link_delete_response_dto_from_dict = PaymentLinkDeleteResponseDTO.from_dict(payment_link_delete_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
