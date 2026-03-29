# InstallmentSplitGetResponseDTO

Array de splits

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único do split pago no Asaas | [optional] 
**wallet_id** | **str** | Identificador da carteira Asaas que será transferido | [optional] 
**fixed_value** | **float** | Valor fixo a ser transferido para a conta quando a cobrança for recebida | [optional] 
**percentual_value** | **float** | Percentual sobre o valor líquido da cobrança a ser transferido quando for recebida | [optional] 
**total_value** | **float** | Valor total do split que será enviado. Os valores exibidos podem sofrer alteração após a confirmação ou alteração da cobrança. | [optional] 
**cancellation_reason** | [**InstallmentSplitGetResponsePaymentSplitCancellationReason**](InstallmentSplitGetResponsePaymentSplitCancellationReason.md) |  | [optional] 
**status** | [**InstallmentSplitGetResponsePaymentSplitStatus**](InstallmentSplitGetResponsePaymentSplitStatus.md) |  | [optional] 
**external_reference** | **str** | Identificador do split no seu sistema | [optional] 
**description** | **str** | Descrição do split | [optional] 
**installment_number** | **int** | Parcela à qual o split está vinculado | [optional] 

## Example

```python
from asaas.models.installment_split_get_response_dto import InstallmentSplitGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentSplitGetResponseDTO from a JSON string
installment_split_get_response_dto_instance = InstallmentSplitGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentSplitGetResponseDTO.to_json())

# convert the object into a dict
installment_split_get_response_dto_dict = installment_split_get_response_dto_instance.to_dict()
# create an instance of InstallmentSplitGetResponseDTO from a dict
installment_split_get_response_dto_from_dict = InstallmentSplitGetResponseDTO.from_dict(installment_split_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


