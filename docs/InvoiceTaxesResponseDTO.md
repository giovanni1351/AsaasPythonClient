# InvoiceTaxesResponseDTO

Impostos da nota fiscal

## Properties

| Name                          | Type      | Description                                      | Notes      |
| ----------------------------- | --------- | ------------------------------------------------ | ---------- |
| **nbs_code**                  | **str**   | Código NBS (Nomenclatura Brasileira de Serviços) | [optional] |
| **tax_situation_code**        | **str**   | Código de situação tributária                    | [optional] |
| **tax_classification_code**   | **str**   | Código de classificação tributária               | [optional] |
| **operation_indicator_code**  | **str**   | Código do indicador de operação                  | [optional] |
| **retain_iss**                | **bool**  | Tomador da nota fiscal deve reter ISS ou não     |
| **iss**                       | **float** | Alíquota ISS                                     |
| **pis_cofins_retention_type** | **str**   | Tipo de retenção do PIS/COFINS                   | [optional] |
| **pis_cofins_tax_status**     | **str**   | Situação tributária do PIS/COFINS                | [optional] |
| **pis**                       | **float** | Alíquota PIS                                     |
| **cofins**                    | **float** | Alíquota COFINS                                  |
| **csll**                      | **float** | Alíquota CSLL                                    |
| **inss**                      | **float** | Alíquota INSS                                    |
| **ir**                        | **float** | Alíquota IR                                      |
| **state_ibs**                 | **float** | Alíquota estadual IBS                            | [optional] |
| **state_ibs_value**           | **float** | Valor estadual IBS                               | [optional] |
| **municipal_ibs**             | **float** | Alíquota municipal IBS                           | [optional] |
| **municipal_ibs_value**       | **float** | Valor municipal IBS                              | [optional] |
| **cbs**                       | **float** | Alíquota CBS                                     | [optional] |
| **cbs_value**                 | **float** | Valor CBS                                        | [optional] |

## Example

```python
from asaas.models.invoice_taxes_response_dto import InvoiceTaxesResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InvoiceTaxesResponseDTO from a JSON string
invoice_taxes_response_dto_instance = InvoiceTaxesResponseDTO.from_json(json)
# print the JSON string representation of the object
print(InvoiceTaxesResponseDTO.to_json())

# convert the object into a dict
invoice_taxes_response_dto_dict = invoice_taxes_response_dto_instance.to_dict()
# create an instance of InvoiceTaxesResponseDTO from a dict
invoice_taxes_response_dto_from_dict = InvoiceTaxesResponseDTO.from_dict(invoice_taxes_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
