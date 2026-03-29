# PaymentRefundedSplitResponseDTO

Lista de splits estornados, se houver

## Properties

| Name      | Type      | Description                     | Notes      |
| --------- | --------- | ------------------------------- | ---------- |
| **id**    | **str**   | Identificador único do split    | [optional] |
| **value** | **float** | Valor estornado                 | [optional] |
| **done**  | **bool**  | Indica se o split foi estornado | [optional] |

## Example

```python
from asaas.models.payment_refunded_split_response_dto import PaymentRefundedSplitResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentRefundedSplitResponseDTO from a JSON string
payment_refunded_split_response_dto_instance = PaymentRefundedSplitResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentRefundedSplitResponseDTO.to_json())

# convert the object into a dict
payment_refunded_split_response_dto_dict = payment_refunded_split_response_dto_instance.to_dict()
# create an instance of PaymentRefundedSplitResponseDTO from a dict
payment_refunded_split_response_dto_from_dict = PaymentRefundedSplitResponseDTO.from_dict(payment_refunded_split_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
