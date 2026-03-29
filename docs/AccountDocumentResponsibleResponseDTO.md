# AccountDocumentResponsibleResponseDTO

Quem são os responsáveis pelo envio desses documentos

## Properties

| Name     | Type                                                                                                                                              | Description         | Notes      |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- | ---------- |
| **name** | **str**                                                                                                                                           | Nome do responsável | [optional] |
| **type** | [**List[AccountDocumentResponsibleResponseAccountDocumentResponsibleType]**](AccountDocumentResponsibleResponseAccountDocumentResponsibleType.md) | Tipo de responsável | [optional] |

## Example

```python
from asaas.models.account_document_responsible_response_dto import AccountDocumentResponsibleResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountDocumentResponsibleResponseDTO from a JSON string
account_document_responsible_response_dto_instance = AccountDocumentResponsibleResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AccountDocumentResponsibleResponseDTO.to_json())

# convert the object into a dict
account_document_responsible_response_dto_dict = account_document_responsible_response_dto_instance.to_dict()
# create an instance of AccountDocumentResponsibleResponseDTO from a dict
account_document_responsible_response_dto_from_dict = AccountDocumentResponsibleResponseDTO.from_dict(account_document_responsible_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
