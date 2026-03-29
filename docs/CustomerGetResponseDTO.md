# CustomerGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo de objeto | [optional] 
**id** | **str** | Identificador único do cliente no Asaas | [optional] 
**date_created** | **str** | Data de criação do cliente | [optional] 
**name** | **str** | Nome do cliente | [optional] 
**email** | **str** | E-mail do cliente | [optional] 
**phone** | **str** | Telefone do cliente | [optional] 
**mobile_phone** | **str** | Celular do cliente | [optional] 
**address** | **str** | Endereço do cliente | [optional] 
**address_number** | **str** | Número do endereço do cliente | [optional] 
**complement** | **str** | Complemento do endereço do cliente | [optional] 
**province** | **str** | Bairro do endereço do cliente | [optional] 
**city** | **int** | Identificador único da cidade no Asaas | [optional] 
**city_name** | **str** | Cidade do endereço do cliente | [optional] 
**state** | **str** | Estado do endereço do cliente | [optional] 
**country** | **str** | País do cliente | [optional] 
**postal_code** | **str** | CEP do endereço do cliente | [optional] 
**cpf_cnpj** | **str** | CPF ou CNPJ do cliente | [optional] 
**person_type** | [**CustomerGetResponsePersonType**](CustomerGetResponsePersonType.md) |  | [optional] 
**deleted** | **bool** | Indica se é um cliente deletado | [optional] 
**additional_emails** | **str** | E-mails adicionais do cliente | [optional] 
**external_reference** | **str** | Referência externa do cliente | [optional] 
**notification_disabled** | **bool** | Indica se as notificações estão desabilitadas | [optional] 
**observations** | **str** | Observações do cliente | [optional] 
**foreign_customer** | **bool** | indica se o pagador é estrangeiro | [optional] 

## Example

```python
from asaas.models.customer_get_response_dto import CustomerGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerGetResponseDTO from a JSON string
customer_get_response_dto_instance = CustomerGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CustomerGetResponseDTO.to_json())

# convert the object into a dict
customer_get_response_dto_dict = customer_get_response_dto_instance.to_dict()
# create an instance of CustomerGetResponseDTO from a dict
customer_get_response_dto_from_dict = CustomerGetResponseDTO.from_dict(customer_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


