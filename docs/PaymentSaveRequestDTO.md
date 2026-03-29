# PaymentSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer** | **str** | Identificador único do cliente no Asaas | 
**billing_type** | [**PaymentSaveRequestBillingType**](PaymentSaveRequestBillingType.md) |  | 
**value** | **float** | Valor da cobrança | 
**due_date** | **date** | Data de vencimento da cobrança | 
**description** | **str** | Descrição da cobrança (máx. 500 caracteres) | [optional] 
**days_after_due_date_to_registration_cancellation** | **int** | Dias após o vencimento para cancelamento do registro (somente para boleto bancário) | [optional] 
**external_reference** | **str** | Campo livre para busca | [optional] 
**installment_count** | **int** | Número de parcelas (somente no caso de cobrança parcelada) | [optional] 
**total_value** | **float** | Informe o valor total de uma cobrança que será parcelada (somente no caso de cobrança parcelada). Caso enviado este campo o installmentValue não é necessário, o cálculo por parcela será automático. | [optional] 
**installment_value** | **float** | Valor de cada parcela (somente no caso de cobrança parcelada). Envie este campo em caso de querer definir o valor de cada parcela. | [optional] 
**discount** | [**PaymentDiscountDTO**](PaymentDiscountDTO.md) |  | [optional] 
**interest** | [**PaymentInterestRequestDTO**](PaymentInterestRequestDTO.md) |  | [optional] 
**fine** | [**PaymentFineRequestDTO**](PaymentFineRequestDTO.md) |  | [optional] 
**postal_service** | **bool** | Define se a cobrança será enviada via Correios | [optional] 
**split** | [**List[PaymentSplitRequestDTO]**](PaymentSplitRequestDTO.md) | Configurações do split | [optional] 
**callback** | [**PaymentCallbackRequestDTO**](PaymentCallbackRequestDTO.md) |  | [optional] 
**pix_automatic_authorization_id** | **str** | Identificador único da autorização do Pix Automático no Asaas | [optional] 

## Example

```python
from asaas.models.payment_save_request_dto import PaymentSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSaveRequestDTO from a JSON string
payment_save_request_dto_instance = PaymentSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSaveRequestDTO.to_json())

# convert the object into a dict
payment_save_request_dto_dict = payment_save_request_dto_instance.to_dict()
# create an instance of PaymentSaveRequestDTO from a dict
payment_save_request_dto_from_dict = PaymentSaveRequestDTO.from_dict(payment_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


