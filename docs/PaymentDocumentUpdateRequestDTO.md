# PaymentDocumentUpdateRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**available_after_payment** | **bool** | true para disponibilizar o documento apenas após o pagamento | 
**type** | [**PaymentDocumentUpdateRequestPaymentDocumentType**](PaymentDocumentUpdateRequestPaymentDocumentType.md) |  | 

## Example

```python
from asaas.models.payment_document_update_request_dto import PaymentDocumentUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDocumentUpdateRequestDTO from a JSON string
payment_document_update_request_dto_instance = PaymentDocumentUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDocumentUpdateRequestDTO.to_json())

# convert the object into a dict
payment_document_update_request_dto_dict = payment_document_update_request_dto_instance.to_dict()
# create an instance of PaymentDocumentUpdateRequestDTO from a dict
payment_document_update_request_dto_from_dict = PaymentDocumentUpdateRequestDTO.from_dict(payment_document_update_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


