# PaymentUpdateRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**billing_type** | [**PaymentUpdateRequestBillingType**](PaymentUpdateRequestBillingType.md) |  | 
**value** | **float** | Valor da cobrança | 
**due_date** | **date** | Data de vencimento da cobrança | 
**description** | **str** | Descrição da cobrança (máx. 500 caracteres) | [optional] 
**days_after_due_date_to_registration_cancellation** | **int** | Dias após o vencimento para cancelamento do registro (somente para boleto bancário) | [optional] 
**external_reference** | **str** | Campo livre para busca | [optional] 
**discount** | [**PaymentDiscountDTO**](PaymentDiscountDTO.md) |  | [optional] 
**interest** | [**PaymentInterestRequestDTO**](PaymentInterestRequestDTO.md) |  | [optional] 
**fine** | [**PaymentFineRequestDTO**](PaymentFineRequestDTO.md) |  | [optional] 
**postal_service** | **bool** | Define se a cobrança será enviada via Correios | [optional] 
**split** | [**List[PaymentSplitRequestDTO]**](PaymentSplitRequestDTO.md) | Configurações do split | [optional] 
**callback** | [**PaymentCallbackRequestDTO**](PaymentCallbackRequestDTO.md) |  | [optional] 

## Example

```python
from asaas.models.payment_update_request_dto import PaymentUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentUpdateRequestDTO from a JSON string
payment_update_request_dto_instance = PaymentUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentUpdateRequestDTO.to_json())

# convert the object into a dict
payment_update_request_dto_dict = payment_update_request_dto_instance.to_dict()
# create an instance of PaymentUpdateRequestDTO from a dict
payment_update_request_dto_from_dict = PaymentUpdateRequestDTO.from_dict(payment_update_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


