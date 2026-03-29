# PaymentDocumentGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo do objeto | [optional] 
**id** | **str** | Identificador único do documento | [optional] 
**name** | **str** | Nome do documento | [optional] 
**type** | [**PaymentDocumentGetResponsePaymentDocumentType**](PaymentDocumentGetResponsePaymentDocumentType.md) |  | [optional] 
**available_after_payment** | **bool** | Disponível somente após o pagamento | [optional] 
**file** | [**PaymentDocumentFileResponseDTO**](PaymentDocumentFileResponseDTO.md) |  | [optional] 
**deleted** | **bool** | Indica se o arquivo foi removido | [optional] 

## Example

```python
from asaas.models.payment_document_get_response_dto import PaymentDocumentGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDocumentGetResponseDTO from a JSON string
payment_document_get_response_dto_instance = PaymentDocumentGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDocumentGetResponseDTO.to_json())

# convert the object into a dict
payment_document_get_response_dto_dict = payment_document_get_response_dto_instance.to_dict()
# create an instance of PaymentDocumentGetResponseDTO from a dict
payment_document_get_response_dto_from_dict = PaymentDocumentGetResponseDTO.from_dict(payment_document_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


