# AccountDocumentGroupResponseDTO

Lista de objetos

## Properties

| Name                               | Type                                                                                                          | Description                                                              | Notes      |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ---------- |
| **id**                             | **str**                                                                                                       | Identificador único do grupo de documentos no Asaas                      | [optional] |
| **status**                         | [**AccountDocumentGroupResponseAccountDocumentStatus**](AccountDocumentGroupResponseAccountDocumentStatus.md) |                                                                          | [optional] |
| **type**                           | [**AccountDocumentGroupResponseAccountDocumentType**](AccountDocumentGroupResponseAccountDocumentType.md)     |                                                                          | [optional] |
| **title**                          | **str**                                                                                                       | Título do grupo de documentos                                            | [optional] |
| **description**                    | **str**                                                                                                       | Descrição                                                                | [optional] |
| **responsible**                    | [**AccountDocumentResponsibleResponseDTO**](AccountDocumentResponsibleResponseDTO.md)                         |                                                                          | [optional] |
| **onboarding_url**                 | **str**                                                                                                       | URL para envio dos documentos                                            | [optional] |
| **onboarding_url_expiration_date** | **datetime**                                                                                                  | Data de expiração da URL de envio dos documentos                         | [optional] |
| **documents**                      | [**List[AccountDocumentGetResponseDTO]**](AccountDocumentGetResponseDTO.md)                                   | Os documentos que já foram enviados com seus respectivos identificadores | [optional] |

## Example

```python
from asaas.models.account_document_group_response_dto import AccountDocumentGroupResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountDocumentGroupResponseDTO from a JSON string
account_document_group_response_dto_instance = AccountDocumentGroupResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AccountDocumentGroupResponseDTO.to_json())

# convert the object into a dict
account_document_group_response_dto_dict = account_document_group_response_dto_instance.to_dict()
# create an instance of AccountDocumentGroupResponseDTO from a dict
account_document_group_response_dto_from_dict = AccountDocumentGroupResponseDTO.from_dict(account_document_group_response_dto_dict)
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
