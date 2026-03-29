# AccountDocumentGetResponseDTO

## Properties

| Name       | Type                                                                                                      | Description                               | Notes      |
| ---------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------- | ---------- |
| **id**     | **str**                                                                                                   | Identificador único do documento no Asaas | [optional] |
| **status** | [**AccountDocumentGetResponseAccountDocumentStatus**](AccountDocumentGetResponseAccountDocumentStatus.md) |                                           | [optional] |

## Example

```python
from asaas.models.account_document_get_response_dto import AccountDocumentGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountDocumentGetResponseDTO from a JSON string
account_document_get_response_dto_instance = AccountDocumentGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AccountDocumentGetResponseDTO.to_json())

# convert the object into a dict
account_document_get_response_dto_dict = account_document_get_response_dto_instance.to_dict()
# create an instance of AccountDocumentGetResponseDTO from a dict
account_document_get_response_dto_from_dict = AccountDocumentGetResponseDTO.from_dict(account_document_get_response_dto_dict)
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
