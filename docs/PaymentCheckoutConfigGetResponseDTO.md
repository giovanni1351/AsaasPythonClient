# PaymentCheckoutConfigGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo de objeto | [optional] 
**logo_background_color** | **str** | Cor de fundo do logo | [optional] 
**info_background_color** | **str** | Cor de fundo das suas informações | [optional] 
**font_color** | **str** | Cor da fonte das suas informações | [optional] 
**enabled** | **bool** | Indica se a personalização está habilitada | [optional] [default to True]
**logo_url** | **str** | Link para download da logo | [optional] 
**observations** | **str** | Observações da análise de personalização da fatura | [optional] 
**status** | [**PaymentCheckoutConfigGetResponseInvoiceConfigStatus**](PaymentCheckoutConfigGetResponseInvoiceConfigStatus.md) |  | [optional] 

## Example

```python
from asaas.models.payment_checkout_config_get_response_dto import PaymentCheckoutConfigGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentCheckoutConfigGetResponseDTO from a JSON string
payment_checkout_config_get_response_dto_instance = PaymentCheckoutConfigGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentCheckoutConfigGetResponseDTO.to_json())

# convert the object into a dict
payment_checkout_config_get_response_dto_dict = payment_checkout_config_get_response_dto_instance.to_dict()
# create an instance of PaymentCheckoutConfigGetResponseDTO from a dict
payment_checkout_config_get_response_dto_from_dict = PaymentCheckoutConfigGetResponseDTO.from_dict(payment_checkout_config_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


