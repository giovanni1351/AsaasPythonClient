# CreditBureauReportGetResponseDTO

## Properties

| Name             | Type     | Description                                                                                           | Notes      |
| ---------------- | -------- | ----------------------------------------------------------------------------------------------------- | ---------- |
| **id**           | **str**  | Identificador único da consulta no Asaas                                                              | [optional] |
| **date_created** | **date** | Data da realização da consulta                                                                        | [optional] |
| **cpf_cnpj**     | **str**  | CPF ou CNPJ consultado manualmente                                                                    | [optional] |
| **customer**     | **str**  | Identificador único do cliente no Asaas                                                               | [optional] |
| **download_url** | **str**  | Url para download da consulta. Disponível até as 23:59 do dia da consulta.                            | [optional] |
| **report_file**  | **str**  | PDF da consulta realizada em Base64 (este campo apenas é retornado no momento da criação da consulta) | [optional] |

## Example

```python
from asaas.models.credit_bureau_report_get_response_dto import CreditBureauReportGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CreditBureauReportGetResponseDTO from a JSON string
credit_bureau_report_get_response_dto_instance = CreditBureauReportGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CreditBureauReportGetResponseDTO.to_json())

# convert the object into a dict
credit_bureau_report_get_response_dto_dict = credit_bureau_report_get_response_dto_instance.to_dict()
# create an instance of CreditBureauReportGetResponseDTO from a dict
credit_bureau_report_get_response_dto_from_dict = CreditBureauReportGetResponseDTO.from_dict(credit_bureau_report_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
