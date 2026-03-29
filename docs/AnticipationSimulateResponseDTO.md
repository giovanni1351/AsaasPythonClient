# AnticipationSimulateResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**installment** | **str** | Identificador único do parcelamento a ser antecipado | [optional] 
**payment** | **str** | Identificador único da cobrança a ser antecipada | [optional] 
**anticipation_date** | **date** | Data de solicitação da antecipação | [optional] 
**due_date** | **date** | Data de vencimento da solicitação | [optional] 
**fee** | **float** | Taxa de antecipação | [optional] 
**anticipation_days** | **int** | Quantidade de dias que foram antecipados | [optional] 
**net_value** | **float** | Valor líquido descontada a taxa de antecipação | [optional] 
**total_value** | **float** | Valor total da cobrança a ser antecipada | [optional] 
**value** | **float** | Valor da antecipação | [optional] 
**is_documentation_required** | **bool** | Determina a obrigatoriedade do envio de notas fiscais eletrônicas ou contratos de prestação de serviços na solicitação da antecipação | [optional] 

## Example

```python
from asaas.models.anticipation_simulate_response_dto import AnticipationSimulateResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AnticipationSimulateResponseDTO from a JSON string
anticipation_simulate_response_dto_instance = AnticipationSimulateResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AnticipationSimulateResponseDTO.to_json())

# convert the object into a dict
anticipation_simulate_response_dto_dict = anticipation_simulate_response_dto_instance.to_dict()
# create an instance of AnticipationSimulateResponseDTO from a dict
anticipation_simulate_response_dto_from_dict = AnticipationSimulateResponseDTO.from_dict(anticipation_simulate_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


