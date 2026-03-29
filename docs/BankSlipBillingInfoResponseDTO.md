# BankSlipBillingInfoResponseDTO

Dados do pagamento relacionados a boleto

## Properties

| Name                                                 | Type    | Description                                                                         | Notes      |
| ---------------------------------------------------- | ------- | ----------------------------------------------------------------------------------- | ---------- |
| **identification_field**                             | **str** | Linha digitável do boleto                                                           | [optional] |
| **nosso_numero**                                     | **str** | Número de identificação do boleto                                                   | [optional] |
| **bar_code**                                         | **str** | Código de barras do boleto                                                          | [optional] |
| **bank_slip_url**                                    | **str** | URL para download do boleto                                                         | [optional] |
| **days_after_due_date_to_registration_cancellation** | **int** | Dias após o vencimento para cancelamento do registro (somente para boleto bancário) | [optional] |

## Example

```python
from asaas.models.bank_slip_billing_info_response_dto import BankSlipBillingInfoResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of BankSlipBillingInfoResponseDTO from a JSON string
bank_slip_billing_info_response_dto_instance = BankSlipBillingInfoResponseDTO.from_json(json)
# print the JSON string representation of the object
print(BankSlipBillingInfoResponseDTO.to_json())

# convert the object into a dict
bank_slip_billing_info_response_dto_dict = bank_slip_billing_info_response_dto_instance.to_dict()
# create an instance of BankSlipBillingInfoResponseDTO from a dict
bank_slip_billing_info_response_dto_from_dict = BankSlipBillingInfoResponseDTO.from_dict(bank_slip_billing_info_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
