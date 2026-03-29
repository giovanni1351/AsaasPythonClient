# PaymentLinkSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Nome do link de pagamentos | 
**description** | **str** | Descrição do link de pagamentos | [optional] 
**end_date** | **str** | Data de encerramento | [optional] 
**value** | **float** | Valor do link de pagamentos, caso não informado o pagador poderá informar o quanto deseja pagar | [optional] 
**billing_type** | [**PaymentLinkSaveRequestBillingType**](PaymentLinkSaveRequestBillingType.md) |  | 
**charge_type** | [**PaymentLinkSaveRequestChargeType**](PaymentLinkSaveRequestChargeType.md) |  | 
**due_date_limit_days** | **int** | Quantidade de dias úteis que o seu cliente poderá pagar após o boleto ser gerado (Para forma de pagamento como Boleto) | [optional] 
**subscription_cycle** | [**PaymentLinkSaveRequestCycle**](PaymentLinkSaveRequestCycle.md) |  | [optional] 
**max_installment_count** | **int** | Quantidade máxima de parcelas que seu cliente poderá parcelar o valor do link de pagamentos caso a forma de cobrança selecionado seja Parcelamento. Caso não informado o valor padrão será de 1 parcela | [optional] [default to 1]
**external_reference** | **str** | Campo livre para busca | [optional] 
**notification_enabled** | **bool** | Define se os clientes cadastrados pelo link de pagamentos terão as notificações habilitadas. Caso não seja informado o valor padrão será true | [optional] [default to True]
**callback** | [**PaymentCallbackRequestDTO**](PaymentCallbackRequestDTO.md) |  | [optional] 
**is_address_required** | **bool** | True para tornar obrigatório o preenchimento de dados de endereço no checkout. | [optional] 

## Example

```python
from asaas.models.payment_link_save_request_dto import PaymentLinkSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLinkSaveRequestDTO from a JSON string
payment_link_save_request_dto_instance = PaymentLinkSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLinkSaveRequestDTO.to_json())

# convert the object into a dict
payment_link_save_request_dto_dict = payment_link_save_request_dto_instance.to_dict()
# create an instance of PaymentLinkSaveRequestDTO from a dict
payment_link_save_request_dto_from_dict = PaymentLinkSaveRequestDTO.from_dict(payment_link_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


