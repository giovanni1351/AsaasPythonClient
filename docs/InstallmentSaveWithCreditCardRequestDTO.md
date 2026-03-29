# InstallmentSaveWithCreditCardRequestDTO

## Properties

| Name                                                 | Type                                                                                                      | Description                                                                                                                                                                  | Notes      |
| ---------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| **installment_count**                                | **int**                                                                                                   | Número de parcelas                                                                                                                                                           |
| **customer**                                         | **str**                                                                                                   | Identificador único do cliente no Asaas                                                                                                                                      |
| **value**                                            | **float**                                                                                                 | Valor de cada parcela                                                                                                                                                        |
| **total_value**                                      | **float**                                                                                                 | Valor total do parcelamento                                                                                                                                                  | [optional] |
| **billing_type**                                     | [**InstallmentSaveWithCreditCardRequestBillingType**](InstallmentSaveWithCreditCardRequestBillingType.md) |                                                                                                                                                                              |
| **due_date**                                         | **date**                                                                                                  | Data de vencimento da primeira parcela                                                                                                                                       |
| **description**                                      | **str**                                                                                                   | Descrição do parcelamento (máx. 500 caracteres)                                                                                                                              | [optional] |
| **postal_service**                                   | **bool**                                                                                                  | Define se a cobrança será enviada via Correios                                                                                                                               | [optional] |
| **days_after_due_date_to_registration_cancellation** | **int**                                                                                                   | Dias após o vencimento para cancelamento do registro (somente para boleto bancário)                                                                                          | [optional] |
| **payment_external_reference**                       | **str**                                                                                                   | Campo livre para busca                                                                                                                                                       | [optional] |
| **discount**                                         | [**PaymentDiscountDTO**](PaymentDiscountDTO.md)                                                           |                                                                                                                                                                              | [optional] |
| **interest**                                         | [**PaymentInterestRequestDTO**](PaymentInterestRequestDTO.md)                                             |                                                                                                                                                                              | [optional] |
| **fine**                                             | [**PaymentFineRequestDTO**](PaymentFineRequestDTO.md)                                                     |                                                                                                                                                                              | [optional] |
| **splits**                                           | [**List[InstallmentSplitRequestDTO]**](InstallmentSplitRequestDTO.md)                                     | Configurações do split                                                                                                                                                       | [optional] |
| **credit_card**                                      | [**CreditCardRequestDTO**](CreditCardRequestDTO.md)                                                       |                                                                                                                                                                              |
| **credit_card_holder_info**                          | [**CreditCardHolderInfoRequestDTO**](CreditCardHolderInfoRequestDTO.md)                                   |                                                                                                                                                                              |
| **credit_card_token**                                | **str**                                                                                                   | Token do cartão de crédito para uso da funcionalidade de tokenização de cartão de crédito. Caso informado, os campos creditCard e creditCardHolderInfo não são obrigatórios. | [optional] |
| **authorize_only**                                   | **bool**                                                                                                  | Realizar apenas a Pré-Autorização do parcelamento                                                                                                                            | [optional] |
| **remote_ip**                                        | **str**                                                                                                   | IP de onde o cliente está fazendo a compra. Não deve ser informado o IP do seu servidor.                                                                                     |

## Example

```python
from asaas.models.installment_save_with_credit_card_request_dto import InstallmentSaveWithCreditCardRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentSaveWithCreditCardRequestDTO from a JSON string
installment_save_with_credit_card_request_dto_instance = InstallmentSaveWithCreditCardRequestDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentSaveWithCreditCardRequestDTO.to_json())

# convert the object into a dict
installment_save_with_credit_card_request_dto_dict = installment_save_with_credit_card_request_dto_instance.to_dict()
# create an instance of InstallmentSaveWithCreditCardRequestDTO from a dict
installment_save_with_credit_card_request_dto_from_dict = InstallmentSaveWithCreditCardRequestDTO.from_dict(installment_save_with_credit_card_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
