# InstallmentRefundResponseDTO

Informações de estorno

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date_created** | **datetime** | Data da criação do estorno | [optional] 
**status** | [**InstallmentRefundResponsePaymentRefundStatus**](InstallmentRefundResponsePaymentRefundStatus.md) |  | [optional] 
**value** | **float** | Valor do estorno | [optional] 
**end_to_end_identifier** | **str** | (Apenas pix) Identificador da transação Pix no Banco Central | [optional] 
**description** | **str** | Descrição do estorno | [optional] 
**effective_date** | **datetime** | (Apenas pix) Data de efetivação do estorno | [optional] 
**transaction_receipt_url** | **str** | Link do recibo da transação | [optional] 
**refunded_splits** | [**List[PaymentRefundedSplitResponseDTO]**](PaymentRefundedSplitResponseDTO.md) | Lista de splits estornados, se houver | [optional] 
**payment_id** | **str** | Identificador único da cobrança no Asaas | [optional] 

## Example

```python
from asaas.models.installment_refund_response_dto import InstallmentRefundResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentRefundResponseDTO from a JSON string
installment_refund_response_dto_instance = InstallmentRefundResponseDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentRefundResponseDTO.to_json())

# convert the object into a dict
installment_refund_response_dto_dict = installment_refund_response_dto_instance.to_dict()
# create an instance of InstallmentRefundResponseDTO from a dict
installment_refund_response_dto_from_dict = InstallmentRefundResponseDTO.from_dict(installment_refund_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


