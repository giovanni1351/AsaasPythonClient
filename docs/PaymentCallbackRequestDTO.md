# PaymentCallbackRequestDTO

Informações de redirecionamento automático após pagamento do link de pagamento

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success_url** | **str** | URL que o cliente será redirecionado após o pagamento com sucesso da fatura ou link de pagamento | 
**auto_redirect** | **bool** | Definir se o cliente será redirecionado automaticamente ou será apenas informado com um botão para retornar ao site. O padrão é true, caso queira desativar informar false | [optional] 

## Example

```python
from asaas.models.payment_callback_request_dto import PaymentCallbackRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentCallbackRequestDTO from a JSON string
payment_callback_request_dto_instance = PaymentCallbackRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentCallbackRequestDTO.to_json())

# convert the object into a dict
payment_callback_request_dto_dict = payment_callback_request_dto_instance.to_dict()
# create an instance of PaymentCallbackRequestDTO from a dict
payment_callback_request_dto_from_dict = PaymentCallbackRequestDTO.from_dict(payment_callback_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


