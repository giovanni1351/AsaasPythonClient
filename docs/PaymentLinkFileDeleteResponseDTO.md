# PaymentLinkFileDeleteResponseDTO

## Properties

| Name        | Type     | Description                                                      | Notes      |
| ----------- | -------- | ---------------------------------------------------------------- | ---------- |
| **deleted** | **bool** | Indica se a imagem foi removida                                  | [optional] |
| **id**      | **str**  | Identificador único da imagem do seu link de pagamentos no Asaas | [optional] |

## Example

```python
from asaas.models.payment_link_file_delete_response_dto import PaymentLinkFileDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLinkFileDeleteResponseDTO from a JSON string
payment_link_file_delete_response_dto_instance = PaymentLinkFileDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLinkFileDeleteResponseDTO.to_json())

# convert the object into a dict
payment_link_file_delete_response_dto_dict = payment_link_file_delete_response_dto_instance.to_dict()
# create an instance of PaymentLinkFileDeleteResponseDTO from a dict
payment_link_file_delete_response_dto_from_dict = PaymentLinkFileDeleteResponseDTO.from_dict(payment_link_file_delete_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
