# PaymentLinkFileGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único da imagem do seu link de pagamentos no Asaas | [optional] 
**main** | **bool** | Determina se esta é a imagem principal | [optional] 
**image** | [**PaymentLinkFileImageResponseDTO**](PaymentLinkFileImageResponseDTO.md) |  | [optional] 

## Example

```python
from asaas.models.payment_link_file_get_response_dto import PaymentLinkFileGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLinkFileGetResponseDTO from a JSON string
payment_link_file_get_response_dto_instance = PaymentLinkFileGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLinkFileGetResponseDTO.to_json())

# convert the object into a dict
payment_link_file_get_response_dto_dict = payment_link_file_get_response_dto_instance.to_dict()
# create an instance of PaymentLinkFileGetResponseDTO from a dict
payment_link_file_get_response_dto_from_dict = PaymentLinkFileGetResponseDTO.from_dict(payment_link_file_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


