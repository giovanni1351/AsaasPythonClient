# InvoiceCancelRequestDTO

## Properties

| Name                     | Type     | Description                           | Notes      |
| ------------------------ | -------- | ------------------------------------- | ---------- |
| **cancel_only_on_asaas** | **bool** | Cancelar nota fiscal somente no Asaas | [optional] |

## Example

```python
from asaas.models.invoice_cancel_request_dto import InvoiceCancelRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InvoiceCancelRequestDTO from a JSON string
invoice_cancel_request_dto_instance = InvoiceCancelRequestDTO.from_json(json)
# print the JSON string representation of the object
print(InvoiceCancelRequestDTO.to_json())

# convert the object into a dict
invoice_cancel_request_dto_dict = invoice_cancel_request_dto_instance.to_dict()
# create an instance of InvoiceCancelRequestDTO from a dict
invoice_cancel_request_dto_from_dict = InvoiceCancelRequestDTO.from_dict(invoice_cancel_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
