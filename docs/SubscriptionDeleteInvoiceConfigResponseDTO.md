# SubscriptionDeleteInvoiceConfigResponseDTO

## Properties

| Name        | Type     | Description                                 | Notes      |
| ----------- | -------- | ------------------------------------------- | ---------- |
| **deleted** | **bool** | Informa se as configurações foram removidas | [optional] |
| **id**      | **str**  | Identificador único da assinatura no Asaas  | [optional] |

## Example

```python
from asaas.models.subscription_delete_invoice_config_response_dto import SubscriptionDeleteInvoiceConfigResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionDeleteInvoiceConfigResponseDTO from a JSON string
subscription_delete_invoice_config_response_dto_instance = SubscriptionDeleteInvoiceConfigResponseDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionDeleteInvoiceConfigResponseDTO.to_json())

# convert the object into a dict
subscription_delete_invoice_config_response_dto_dict = subscription_delete_invoice_config_response_dto_instance.to_dict()
# create an instance of SubscriptionDeleteInvoiceConfigResponseDTO from a dict
subscription_delete_invoice_config_response_dto_from_dict = SubscriptionDeleteInvoiceConfigResponseDTO.from_dict(subscription_delete_invoice_config_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
