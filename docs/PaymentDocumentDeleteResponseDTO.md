# PaymentDocumentDeleteResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted** | **bool** | Indica se o arquivo foi removido | [optional] 
**id** | **str** | Identificador único do documento | [optional] 

## Example

```python
from asaas.models.payment_document_delete_response_dto import PaymentDocumentDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDocumentDeleteResponseDTO from a JSON string
payment_document_delete_response_dto_instance = PaymentDocumentDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDocumentDeleteResponseDTO.to_json())

# convert the object into a dict
payment_document_delete_response_dto_dict = payment_document_delete_response_dto_instance.to_dict()
# create an instance of PaymentDocumentDeleteResponseDTO from a dict
payment_document_delete_response_dto_from_dict = PaymentDocumentDeleteResponseDTO.from_dict(payment_document_delete_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


