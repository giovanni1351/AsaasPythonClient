# AccountDocumentDeleteResponseDTO

## Properties

| Name        | Type     | Description                               | Notes      |
| ----------- | -------- | ----------------------------------------- | ---------- |
| **deleted** | **bool** | Indica se o documento foi removido        | [optional] |
| **id**      | **str**  | Identificador único do documento no Asaas | [optional] |

## Example

```python
from asaas.models.account_document_delete_response_dto import AccountDocumentDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountDocumentDeleteResponseDTO from a JSON string
account_document_delete_response_dto_instance = AccountDocumentDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AccountDocumentDeleteResponseDTO.to_json())

# convert the object into a dict
account_document_delete_response_dto_dict = account_document_delete_response_dto_instance.to_dict()
# create an instance of AccountDocumentDeleteResponseDTO from a dict
account_document_delete_response_dto_from_dict = AccountDocumentDeleteResponseDTO.from_dict(account_document_delete_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
