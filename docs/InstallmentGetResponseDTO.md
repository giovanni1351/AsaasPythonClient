# InstallmentGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo do objeto | [optional] 
**id** | **str** | Identificador único do parcelamento no Asaas | [optional] 
**value** | **float** | Valor do parcelamento | [optional] 
**net_value** | **float** | Valor líquido do parcelamento | [optional] 
**payment_value** | **float** | Valor de cada parcela | [optional] 
**installment_count** | **int** | Número de parcelas | [optional] 
**billing_type** | [**InstallmentGetResponseBillingType**](InstallmentGetResponseBillingType.md) |  | [optional] 
**payment_date** | **date** | Data de liquidação da cobrança no Asaas | [optional] 
**description** | **str** | Descrição do parcelamento | [optional] 
**expiration_day** | **int** | Data de vencimento de cada parcela | [optional] 
**date_created** | **date** | Data de criação do parcelamento | [optional] 
**customer** | **str** | Identificador único do cliente ao qual o parcelamento pertence | [optional] 
**payment_link** | **str** | Identificador único do link de pagamentos ao qual o parcelamento pertence | [optional] 
**checkout_session** | **str** | Identificador único do checkout | [optional] 
**transaction_receipt_url** | **str** | URL do comprovante de confirmação, recebimento, estorno ou remoção. | [optional] 
**chargeback** | [**PaymentChargebackResponseDTO**](PaymentChargebackResponseDTO.md) |  | [optional] 
**credit_card** | [**PaymentSaveWithCreditCardCreditCardDTO**](PaymentSaveWithCreditCardCreditCardDTO.md) |  | [optional] 
**deleted** | **bool** | Indica se o parcelamento foi removido | [optional] 
**refunds** | [**List[InstallmentRefundResponseDTO]**](InstallmentRefundResponseDTO.md) | Informações de estorno | [optional] 

## Example

```python
from asaas.models.installment_get_response_dto import InstallmentGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentGetResponseDTO from a JSON string
installment_get_response_dto_instance = InstallmentGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentGetResponseDTO.to_json())

# convert the object into a dict
installment_get_response_dto_dict = installment_get_response_dto_instance.to_dict()
# create an instance of InstallmentGetResponseDTO from a dict
installment_get_response_dto_from_dict = InstallmentGetResponseDTO.from_dict(installment_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


