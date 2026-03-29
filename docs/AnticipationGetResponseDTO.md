# AnticipationGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo de objeto | [optional] 
**id** | **str** | Identificador único da antecipação no Asaas | [optional] 
**installment** | **str** | Identificador único do parcelamento a ser antecipado | [optional] 
**payment** | **str** | Identificador único da cobrança a ser antecipada. | [optional] 
**status** | [**AnticipationGetResponseAnticipationStatus**](AnticipationGetResponseAnticipationStatus.md) |  | [optional] 
**anticipation_date** | **date** | Data de solicitação da antecipação | [optional] 
**due_date** | **date** | Data de vencimento da solicitação | [optional] 
**request_date** | **date** | Data de solicitação da antecipação | [optional] 
**fee** | **float** | Taxa de antecipação | [optional] 
**anticipation_days** | **int** | Quantidade de dias que foram antecipados | [optional] 
**net_value** | **float** | Valor líquido descontada a taxa de antecipação | [optional] 
**total_value** | **float** | Valor total da cobrança a ser antecipada | [optional] 
**value** | **float** | Valor da antecipação | [optional] 
**denial_observation** | **str** | Motivo de rejeição da antecipação | [optional] 

## Example

```python
from asaas.models.anticipation_get_response_dto import AnticipationGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AnticipationGetResponseDTO from a JSON string
anticipation_get_response_dto_instance = AnticipationGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AnticipationGetResponseDTO.to_json())

# convert the object into a dict
anticipation_get_response_dto_dict = anticipation_get_response_dto_instance.to_dict()
# create an instance of AnticipationGetResponseDTO from a dict
anticipation_get_response_dto_from_dict = AnticipationGetResponseDTO.from_dict(anticipation_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


