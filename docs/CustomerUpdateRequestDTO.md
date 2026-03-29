# CustomerUpdateRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Nome do cliente | [optional] 
**cpf_cnpj** | **str** | CPF ou CNPJ do cliente | [optional] 
**email** | **str** | Email do cliente | [optional] 
**phone** | **str** | Fone fixo | [optional] 
**mobile_phone** | **str** | Fone celular | [optional] 
**address** | **str** | Logradouro | [optional] 
**address_number** | **str** | Número do endereço | [optional] 
**complement** | **str** | Complemento do endereço | [optional] 
**province** | **str** | Bairro | [optional] 
**postal_code** | **str** | CEP do endereço | [optional] 
**external_reference** | **str** | Identificador do cliente no seu sistema | [optional] 
**notification_disabled** | **bool** | true para desabilitar o envio de notificações de cobrança | [optional] 
**additional_emails** | **str** | Emails adicionais para envio de notificações de cobrança separados por \&quot;,\&quot; | [optional] 
**municipal_inscription** | **str** | Inscrição municipal do cliente | [optional] 
**state_inscription** | **str** | Inscrição estadual do cliente | [optional] 
**observations** | **str** | Observações adicionais | [optional] 
**group_name** | **str** | Nome do grupo ao qual o cliente pertence | [optional] 
**company** | **str** | Empresa | [optional] 
**foreign_customer** | **bool** | informe true caso seja pagador estrangeiro | [optional] 

## Example

```python
from asaas.models.customer_update_request_dto import CustomerUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerUpdateRequestDTO from a JSON string
customer_update_request_dto_instance = CustomerUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(CustomerUpdateRequestDTO.to_json())

# convert the object into a dict
customer_update_request_dto_dict = customer_update_request_dto_instance.to_dict()
# create an instance of CustomerUpdateRequestDTO from a dict
customer_update_request_dto_from_dict = CustomerUpdateRequestDTO.from_dict(customer_update_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


