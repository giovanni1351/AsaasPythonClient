# InstallmentSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**installment_count** | **int** | Número de parcelas | 
**customer** | **str** | Identificador único do cliente no Asaas | 
**value** | **float** | Valor de cada parcela | 
**total_value** | **float** | Valor total do parcelamento | [optional] 
**billing_type** | [**InstallmentSaveRequestBillingType**](InstallmentSaveRequestBillingType.md) |  | 
**due_date** | **date** | Data de vencimento da primeira parcela | 
**description** | **str** | Descrição do parcelamento (máx. 500 caracteres) | [optional] 
**postal_service** | **bool** | Define se a cobrança será enviada via Correios | [optional] 
**days_after_due_date_to_registration_cancellation** | **int** | Dias após o vencimento para cancelamento do registro (somente para boleto bancário) | [optional] 
**payment_external_reference** | **str** | Campo livre para busca | [optional] 
**discount** | [**PaymentDiscountDTO**](PaymentDiscountDTO.md) |  | [optional] 
**interest** | [**PaymentInterestRequestDTO**](PaymentInterestRequestDTO.md) |  | [optional] 
**fine** | [**PaymentFineRequestDTO**](PaymentFineRequestDTO.md) |  | [optional] 
**splits** | [**List[InstallmentSplitRequestDTO]**](InstallmentSplitRequestDTO.md) | Configurações do split | [optional] 

## Example

```python
from asaas.models.installment_save_request_dto import InstallmentSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentSaveRequestDTO from a JSON string
installment_save_request_dto_instance = InstallmentSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentSaveRequestDTO.to_json())

# convert the object into a dict
installment_save_request_dto_dict = installment_save_request_dto_instance.to_dict()
# create an instance of InstallmentSaveRequestDTO from a dict
installment_save_request_dto_from_dict = InstallmentSaveRequestDTO.from_dict(installment_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


