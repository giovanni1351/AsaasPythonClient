# PaymentLinkFileImageResponseDTO

Informações da imagem do link de pagamentos

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**original_name** | **str** | Nome original da imagem | [optional] 
**size** | **int** | Tamanho da imagem | [optional] 
**extension** | **str** | Extensão da imagem | [optional] 
**preview_url** | **str** | Link para download do preview da imagem | [optional] 
**download_url** | **str** | Link para download da imagem | [optional] 

## Example

```python
from asaas.models.payment_link_file_image_response_dto import PaymentLinkFileImageResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLinkFileImageResponseDTO from a JSON string
payment_link_file_image_response_dto_instance = PaymentLinkFileImageResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLinkFileImageResponseDTO.to_json())

# convert the object into a dict
payment_link_file_image_response_dto_dict = payment_link_file_image_response_dto_instance.to_dict()
# create an instance of PaymentLinkFileImageResponseDTO from a dict
payment_link_file_image_response_dto_from_dict = PaymentLinkFileImageResponseDTO.from_dict(payment_link_file_image_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


