# AccountInfoCityDTO

Informações da cidade cadastrada em sua conta

## Properties

| Name              | Type                                                | Description                            | Notes      |
| ----------------- | --------------------------------------------------- | -------------------------------------- | ---------- |
| **object**        | **str**                                             | Tipo de objeto                         | [optional] |
| **id**            | **int**                                             | Identificador único da cidade no Asaas | [optional] |
| **ibge_code**     | **str**                                             | Código do IBGE                         | [optional] |
| **name**          | **str**                                             | Nome da cidade                         | [optional] |
| **district_code** | **str**                                             | Código do distrito                     | [optional] |
| **district**      | **str**                                             | Nome do distrito                       | [optional] |
| **state**         | [**AccountInfoCityState**](AccountInfoCityState.md) |                                        | [optional] |

## Example

```python
from asaas.models.account_info_city_dto import AccountInfoCityDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountInfoCityDTO from a JSON string
account_info_city_dto_instance = AccountInfoCityDTO.from_json(json)
# print the JSON string representation of the object
print(AccountInfoCityDTO.to_json())

# convert the object into a dict
account_info_city_dto_dict = account_info_city_dto_instance.to_dict()
# create an instance of AccountInfoCityDTO from a dict
account_info_city_dto_from_dict = AccountInfoCityDTO.from_dict(account_info_city_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
