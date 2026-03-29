# WalletGetResponseDTO

Lista de objetos

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo de objeto | [optional] 
**id** | **str** | Identificador da carteira | [optional] 

## Example

```python
from asaas.models.wallet_get_response_dto import WalletGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of WalletGetResponseDTO from a JSON string
wallet_get_response_dto_instance = WalletGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(WalletGetResponseDTO.to_json())

# convert the object into a dict
wallet_get_response_dto_dict = wallet_get_response_dto_instance.to_dict()
# create an instance of WalletGetResponseDTO from a dict
wallet_get_response_dto_from_dict = WalletGetResponseDTO.from_dict(wallet_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


