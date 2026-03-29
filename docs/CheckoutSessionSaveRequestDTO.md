# CheckoutSessionSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**billing_types** | [**List[CheckoutSessionSaveRequestBillingType]**](CheckoutSessionSaveRequestBillingType.md) | Formas de pagamento | 
**charge_types** | [**List[CheckoutSessionSaveRequestChargeType]**](CheckoutSessionSaveRequestChargeType.md) | Tipos de cobrança | 
**minutes_to_expire** | **int** | Tempo em minutos para expiração do checkout | [optional] 
**external_reference** | **str** | Identificador do checkout no seu sistema | [optional] 
**callback** | [**CheckoutSessionCallbackDTO**](CheckoutSessionCallbackDTO.md) |  | 
**items** | [**List[CheckoutSessionItemsDTO]**](CheckoutSessionItemsDTO.md) | Lista de itens no checkout | 
**customer_data** | [**CheckoutSessionCustomerDataDTO**](CheckoutSessionCustomerDataDTO.md) |  | [optional] 
**subscription** | [**CheckoutSessionSubscriptionDTO**](CheckoutSessionSubscriptionDTO.md) |  | [optional] 
**installment** | [**CheckoutSessionInstallmentDTO**](CheckoutSessionInstallmentDTO.md) |  | [optional] 
**splits** | [**List[CheckoutSessionSplitDTO]**](CheckoutSessionSplitDTO.md) | Configurações do split | [optional] 

## Example

```python
from asaas.models.checkout_session_save_request_dto import CheckoutSessionSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSessionSaveRequestDTO from a JSON string
checkout_session_save_request_dto_instance = CheckoutSessionSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(CheckoutSessionSaveRequestDTO.to_json())

# convert the object into a dict
checkout_session_save_request_dto_dict = checkout_session_save_request_dto_instance.to_dict()
# create an instance of CheckoutSessionSaveRequestDTO from a dict
checkout_session_save_request_dto_from_dict = CheckoutSessionSaveRequestDTO.from_dict(checkout_session_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


