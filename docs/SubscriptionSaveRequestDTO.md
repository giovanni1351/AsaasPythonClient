# SubscriptionSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer** | **str** | Identificador único do cliente no Asaas | 
**billing_type** | [**SubscriptionSaveRequestBillingType**](SubscriptionSaveRequestBillingType.md) |  | 
**value** | **float** | Valor da assinatura | 
**next_due_date** | **date** | Vencimento da primeira cobrança | 
**discount** | [**PaymentDiscountDTO**](PaymentDiscountDTO.md) |  | [optional] 
**interest** | [**PaymentInterestRequestDTO**](PaymentInterestRequestDTO.md) |  | [optional] 
**fine** | [**PaymentFineRequestDTO**](PaymentFineRequestDTO.md) |  | [optional] 
**cycle** | [**SubscriptionSaveRequestCycle**](SubscriptionSaveRequestCycle.md) |  | 
**description** | **str** | Descrição da assinatura (máx. 500 caracteres) | [optional] 
**end_date** | **date** | Data limite para vencimento das cobranças | [optional] 
**max_payments** | **int** | Número máximo de cobranças a serem geradas para esta assinatura | [optional] 
**external_reference** | **str** | Identificador da assinatura no seu sistema | [optional] 
**split** | [**List[SubscriptionSplitRequestDTO]**](SubscriptionSplitRequestDTO.md) | Informações de split | [optional] 
**callback** | [**PaymentCallbackRequestDTO**](PaymentCallbackRequestDTO.md) |  | [optional] 

## Example

```python
from asaas.models.subscription_save_request_dto import SubscriptionSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionSaveRequestDTO from a JSON string
subscription_save_request_dto_instance = SubscriptionSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionSaveRequestDTO.to_json())

# convert the object into a dict
subscription_save_request_dto_dict = subscription_save_request_dto_instance.to_dict()
# create an instance of SubscriptionSaveRequestDTO from a dict
subscription_save_request_dto_from_dict = SubscriptionSaveRequestDTO.from_dict(subscription_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


