# SubscriptionInvoiceConfigUpdateRequestDTO

## Properties

| Name                      | Type                                      | Description                                                                                           | Notes      |
| ------------------------- | ----------------------------------------- | ----------------------------------------------------------------------------------------------------- | ---------- |
| **deductions**            | **float**                                 | Deduções. As deduções não alteram o valor total da nota fiscal, mas alteram a base de cálculo do ISS. | [optional] |
| **effective_date_period** | **str**                                   | Quando a nota fiscal será emitida                                                                     | [optional] |
| **received_only**         | **bool**                                  | Emitir apenas para cobranças pagas                                                                    | [optional] |
| **days_before_due_date**  | **int**                                   | Quantidade de dias antes do vencimento da cobrança                                                    | [optional] |
| **observations**          | **str**                                   | Observações adicionais da nota fiscal                                                                 | [optional] |
| **taxes**                 | [**InvoiceTaxesDTO**](InvoiceTaxesDTO.md) |                                                                                                       |

## Example

```python
from asaas.models.subscription_invoice_config_update_request_dto import SubscriptionInvoiceConfigUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionInvoiceConfigUpdateRequestDTO from a JSON string
subscription_invoice_config_update_request_dto_instance = SubscriptionInvoiceConfigUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionInvoiceConfigUpdateRequestDTO.to_json())

# convert the object into a dict
subscription_invoice_config_update_request_dto_dict = subscription_invoice_config_update_request_dto_instance.to_dict()
# create an instance of SubscriptionInvoiceConfigUpdateRequestDTO from a dict
subscription_invoice_config_update_request_dto_from_dict = SubscriptionInvoiceConfigUpdateRequestDTO.from_dict(subscription_invoice_config_update_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
