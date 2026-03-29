# PaymentSplitRequestDTO

Configurações do split

## Properties

| Name                   | Type      | Description                                                                                      | Notes      |
| ---------------------- | --------- | ------------------------------------------------------------------------------------------------ | ---------- |
| **wallet_id**          | **str**   | Identificador da carteira Asaas que será transferido                                             |
| **fixed_value**        | **float** | Valor fixo a ser transferido para a conta quando a cobrança for recebida                         | [optional] |
| **percentual_value**   | **float** | Percentual sobre o valor líquido da cobrança a ser transferido quando for recebida               | [optional] |
| **total_fixed_value**  | **float** | (Somente parcelamentos). Valor que será feito split referente ao valor total que será parcelado. | [optional] |
| **external_reference** | **str**   | Identificador do split no seu sistema                                                            | [optional] |
| **description**        | **str**   | Descrição do split                                                                               | [optional] |

## Example

```python
from asaas.models.payment_split_request_dto import PaymentSplitRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSplitRequestDTO from a JSON string
payment_split_request_dto_instance = PaymentSplitRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSplitRequestDTO.to_json())

# convert the object into a dict
payment_split_request_dto_dict = payment_split_request_dto_instance.to_dict()
# create an instance of PaymentSplitRequestDTO from a dict
payment_split_request_dto_from_dict = PaymentSplitRequestDTO.from_dict(payment_split_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
