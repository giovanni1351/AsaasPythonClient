# AccountDocumentShowResponseDTO

## Properties

| Name               | Type                                                                            | Description                                        | Notes      |
| ------------------ | ------------------------------------------------------------------------------- | -------------------------------------------------- | ---------- |
| **reject_reasons** | **str**                                                                         | Razão pela qual a aprovação da conta foi rejeitada | [optional] |
| **data**           | [**List[AccountDocumentGroupResponseDTO]**](AccountDocumentGroupResponseDTO.md) | Lista de objetos                                   | [optional] |

## Example

```python
from asaas.models.account_document_show_response_dto import AccountDocumentShowResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountDocumentShowResponseDTO from a JSON string
account_document_show_response_dto_instance = AccountDocumentShowResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AccountDocumentShowResponseDTO.to_json())

# convert the object into a dict
account_document_show_response_dto_dict = account_document_show_response_dto_instance.to_dict()
# create an instance of AccountDocumentShowResponseDTO from a dict
account_document_show_response_dto_from_dict = AccountDocumentShowResponseDTO.from_dict(account_document_show_response_dto_dict)
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
