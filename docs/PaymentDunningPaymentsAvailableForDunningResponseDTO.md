# PaymentDunningPaymentsAvailableForDunningResponseDTO

## Properties

| Name            | Type                                                                                                                              | Description                                                    | Notes      |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- | ---------- |
| **object**      | **str**                                                                                                                           | Tipo de objeto                                                 | [optional] |
| **has_more**    | **bool**                                                                                                                          | Indica se há mais uma página a ser buscada                     | [optional] |
| **total_count** | **int**                                                                                                                           | Quantidade total de itens para os filtros informados           | [optional] |
| **limit**       | **int**                                                                                                                           | Quantidade de objetos por página                               | [optional] |
| **offset**      | **int**                                                                                                                           | Posição do objeto a partir do qual a página deve ser carregada | [optional] |
| **data**        | [**List[PaymentDunningPaymentsAvailableForDunningResponseDataDTO]**](PaymentDunningPaymentsAvailableForDunningResponseDataDTO.md) | Lista de objetos                                               | [optional] |

## Example

```python
from asaas.models.payment_dunning_payments_available_for_dunning_response_dto import PaymentDunningPaymentsAvailableForDunningResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDunningPaymentsAvailableForDunningResponseDTO from a JSON string
payment_dunning_payments_available_for_dunning_response_dto_instance = PaymentDunningPaymentsAvailableForDunningResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDunningPaymentsAvailableForDunningResponseDTO.to_json())

# convert the object into a dict
payment_dunning_payments_available_for_dunning_response_dto_dict = payment_dunning_payments_available_for_dunning_response_dto_instance.to_dict()
# create an instance of PaymentDunningPaymentsAvailableForDunningResponseDTO from a dict
payment_dunning_payments_available_for_dunning_response_dto_from_dict = PaymentDunningPaymentsAvailableForDunningResponseDTO.from_dict(payment_dunning_payments_available_for_dunning_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
