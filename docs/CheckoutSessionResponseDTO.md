# CheckoutSessionResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**billing_types** | [**List[CheckoutSessionResponseBillingType]**](CheckoutSessionResponseBillingType.md) | Formas de pagamento | [optional] 
**charge_types** | [**List[CheckoutSessionResponseChargeType]**](CheckoutSessionResponseChargeType.md) | Tipos de cobrança | [optional] 
**minutes_to_expire** | **int** | Tempo em minutos para expiração do checkout | [optional] 
**external_reference** | **str** | Identificador do checkout no seu sistema | [optional] 
**callback** | [**CheckoutSessionCallbackDTO**](CheckoutSessionCallbackDTO.md) |  | [optional] 
**items** | [**List[CheckoutSessionItemsDTO]**](CheckoutSessionItemsDTO.md) | Lista de itens no checkout | [optional] 
**customer_data** | [**CheckoutSessionCustomerDataDTO**](CheckoutSessionCustomerDataDTO.md) |  | [optional] 
**subscription** | [**CheckoutSessionSubscriptionDTO**](CheckoutSessionSubscriptionDTO.md) |  | [optional] 
**installment** | [**CheckoutSessionInstallmentDTO**](CheckoutSessionInstallmentDTO.md) |  | [optional] 
**split** | [**List[CheckoutSessionSplitDTO]**](CheckoutSessionSplitDTO.md) | Configurações do split | [optional] 

## Example

```python
from asaas.models.checkout_session_response_dto import CheckoutSessionResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSessionResponseDTO from a JSON string
checkout_session_response_dto_instance = CheckoutSessionResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CheckoutSessionResponseDTO.to_json())

# convert the object into a dict
checkout_session_response_dto_dict = checkout_session_response_dto_instance.to_dict()
# create an instance of CheckoutSessionResponseDTO from a dict
checkout_session_response_dto_from_dict = CheckoutSessionResponseDTO.from_dict(checkout_session_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


