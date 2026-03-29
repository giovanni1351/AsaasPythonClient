# SubscriptionConfigureInvoiceRequestDTO

## Properties

| Name                       | Type                                                    | Description                                                                                           | Notes      |
| -------------------------- | ------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ---------- |
| **municipal_service_id**   | **str**                                                 | Identificador único do serviço municipal                                                              | [optional] |
| **municipal_service_code** | **str**                                                 | Código de serviço municipal                                                                           | [optional] |
| **municipal_service_name** | **str**                                                 | Nome do serviço municipal                                                                             | [optional] |
| **update_payment**         | **bool**                                                | Atualizar o valor da cobrança com os impostos da nota já descontados.                                 | [optional] |
| **deductions**             | **float**                                               | Deduções. As deduções não alteram o valor total da nota fiscal, mas alteram a base de cálculo do ISS. | [optional] |
| **effective_date_period**  | **str**                                                 | Quando a nota fiscal será emitida                                                                     | [optional] |
| **received_only**          | **bool**                                                | Emitir apenas para cobranças pagas                                                                    | [optional] |
| **days_before_due_date**   | **int**                                                 | Quantidade de dias antes do vencimento da cobrança                                                    | [optional] |
| **observations**           | **str**                                                 | Observações adicionais da nota fiscal                                                                 | [optional] |
| **taxes**                  | [**InvoiceTaxesRequestDTO**](InvoiceTaxesRequestDTO.md) |                                                                                                       |

## Example

```python
from asaas.models.subscription_configure_invoice_request_dto import SubscriptionConfigureInvoiceRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionConfigureInvoiceRequestDTO from a JSON string
subscription_configure_invoice_request_dto_instance = SubscriptionConfigureInvoiceRequestDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionConfigureInvoiceRequestDTO.to_json())

# convert the object into a dict
subscription_configure_invoice_request_dto_dict = subscription_configure_invoice_request_dto_instance.to_dict()
# create an instance of SubscriptionConfigureInvoiceRequestDTO from a dict
subscription_configure_invoice_request_dto_from_dict = SubscriptionConfigureInvoiceRequestDTO.from_dict(subscription_configure_invoice_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
