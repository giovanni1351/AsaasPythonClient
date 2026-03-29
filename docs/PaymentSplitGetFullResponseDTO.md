# PaymentSplitGetFullResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único do split pago no Asaas | [optional] 
**wallet_id** | **str** | Identificador da carteira Asaas que será transferido | [optional] 
**fixed_value** | **float** | Valor fixo a ser transferido para a conta quando a cobrança for recebida | [optional] 
**percentual_value** | **float** | Percentual sobre o valor líquido da cobrança a ser transferido quando for recebida | [optional] 
**total_value** | **float** | Valor total do split que será enviado. Os valores exibidos podem sofrer alteração após a confirmação ou alteração da cobrança. | [optional] 
**cancellation_reason** | [**PaymentSplitGetFullResponsePaymentSplitCancellationReason**](PaymentSplitGetFullResponsePaymentSplitCancellationReason.md) |  | [optional] 
**status** | [**PaymentSplitGetFullResponsePaymentSplitStatus**](PaymentSplitGetFullResponsePaymentSplitStatus.md) |  | [optional] 
**external_reference** | **str** | Identificador do split no seu sistema | [optional] 
**description** | **str** | Descrição do split | [optional] 
**origin_account_id** | **str** | Identificador único da conta de origem do split | [optional] 
**destination_account_id** | **str** | Identificador único da conta de destino do split | [optional] 
**credit_date** | **date** | Data de pagamento do split | [optional] 
**payment** | [**PaymentSplitPaymentInfoResponseDTO**](PaymentSplitPaymentInfoResponseDTO.md) |  | [optional] 

## Example

```python
from asaas.models.payment_split_get_full_response_dto import PaymentSplitGetFullResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSplitGetFullResponseDTO from a JSON string
payment_split_get_full_response_dto_instance = PaymentSplitGetFullResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSplitGetFullResponseDTO.to_json())

# convert the object into a dict
payment_split_get_full_response_dto_dict = payment_split_get_full_response_dto_instance.to_dict()
# create an instance of PaymentSplitGetFullResponseDTO from a dict
payment_split_get_full_response_dto_from_dict = PaymentSplitGetFullResponseDTO.from_dict(payment_split_get_full_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


