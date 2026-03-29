# InvoiceSaveRequestDTO

## Properties

| Name                       | Type                                                    | Description                                                                                                                   | Notes      |
| -------------------------- | ------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ---------- |
| **payment**                | **str**                                                 | Identificador único da cobrança no Asaas                                                                                      | [optional] |
| **installment**            | **str**                                                 | Identificador único do parcelamento no Asaas                                                                                  | [optional] |
| **customer**               | **str**                                                 | Identificador único do cliente no Asaas                                                                                       | [optional] |
| **service_description**    | **str**                                                 | Descrição dos serviços da nota fiscal                                                                                         |
| **observations**           | **str**                                                 | Observações adicionais                                                                                                        |
| **external_reference**     | **str**                                                 | Identificador da nota fiscal no seu sistema                                                                                   | [optional] |
| **value**                  | **float**                                               | Valor total                                                                                                                   |
| **deductions**             | **float**                                               | Deduções. As deduções não alteram o valor total da nota fiscal, mas alteram a base de cálculo do ISS                          |
| **effective_date**         | **date**                                                | Data de emissão da nota fiscal                                                                                                |
| **municipal_service_id**   | **str**                                                 | Identificador único do serviço municipal                                                                                      | [optional] |
| **municipal_service_code** | **str**                                                 | Código de serviço municipal                                                                                                   | [optional] |
| **municipal_service_name** | **str**                                                 | Nome do serviço municipal. Se não for informado, será utilizado o atributo municipalServiceCode como nome para identificação. |
| **update_payment**         | **bool**                                                | Atualizar o valor da cobrança com os impostos da nota já descontados.                                                         | [optional] |
| **taxes**                  | [**InvoiceTaxesRequestDTO**](InvoiceTaxesRequestDTO.md) |                                                                                                                               |

## Example

```python
from asaas.models.invoice_save_request_dto import InvoiceSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InvoiceSaveRequestDTO from a JSON string
invoice_save_request_dto_instance = InvoiceSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(InvoiceSaveRequestDTO.to_json())

# convert the object into a dict
invoice_save_request_dto_dict = invoice_save_request_dto_instance.to_dict()
# create an instance of InvoiceSaveRequestDTO from a dict
invoice_save_request_dto_from_dict = InvoiceSaveRequestDTO.from_dict(invoice_save_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
