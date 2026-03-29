# PaymentDocumentFileResponseDTO

Objeto do Arquivo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**public_id** | **str** | Identificador único do documento | [optional] 
**original_name** | **str** | Nome original do documento | [optional] 
**size** | **int** | Tamanho do arquivo | [optional] 
**extension** | **str** | Extensão do arquivo | [optional] 
**preview_url** | **str** | Link para download do preview do arquivo | [optional] 
**download_url** | **str** | Link para download do arquivo | [optional] 

## Example

```python
from asaas.models.payment_document_file_response_dto import PaymentDocumentFileResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDocumentFileResponseDTO from a JSON string
payment_document_file_response_dto_instance = PaymentDocumentFileResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDocumentFileResponseDTO.to_json())

# convert the object into a dict
payment_document_file_response_dto_dict = payment_document_file_response_dto_instance.to_dict()
# create an instance of PaymentDocumentFileResponseDTO from a dict
payment_document_file_response_dto_from_dict = PaymentDocumentFileResponseDTO.from_dict(payment_document_file_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


