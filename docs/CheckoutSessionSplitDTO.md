# CheckoutSessionSplitDTO

Configurações do split

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**wallet_id** | **str** | Identificador da carteira Asaas que receberá a transferência | 
**fixed_value** | **float** | Valor fixo a ser transferido para a conta quando a cobrança for recebida | [optional] 
**percentage_value** | **float** | Percentual sobre o valor líquido da cobrança a ser transferido quando for recebida | [optional] 
**total_fixed_value** | **float** | (Somente parcelamentos). Valor que será feito split referente ao valor total que será parcelado. | [optional] 

## Example

```python
from asaas.models.checkout_session_split_dto import CheckoutSessionSplitDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSessionSplitDTO from a JSON string
checkout_session_split_dto_instance = CheckoutSessionSplitDTO.from_json(json)
# print the JSON string representation of the object
print(CheckoutSessionSplitDTO.to_json())

# convert the object into a dict
checkout_session_split_dto_dict = checkout_session_split_dto_instance.to_dict()
# create an instance of CheckoutSessionSplitDTO from a dict
checkout_session_split_dto_from_dict = CheckoutSessionSplitDTO.from_dict(checkout_session_split_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


