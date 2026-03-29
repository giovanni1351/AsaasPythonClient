# PaymentLeanSaveWithCreditCardResponseDTO

## Properties

| Name                           | Type                                                                                                            | Description                                                                      | Notes      |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ---------- |
| **object**                     | **str**                                                                                                         | Tipo do objeto                                                                   | [optional] |
| **id**                         | **str**                                                                                                         | Identificador único da cobrança no Asaas                                         | [optional] |
| **date_created**               | **date**                                                                                                        | Data de criação da cobrança                                                      | [optional] |
| **customer_id**                | **str**                                                                                                         | Identificador único do cliente ao qual a cobrança pertence                       | [optional] |
| **subscription_id**            | **str**                                                                                                         | Identificador único da assinatura (quando cobrança recorrente)                   | [optional] |
| **installment_id**             | **str**                                                                                                         | Identificador único do parcelamento (quando cobrança parcelada)                  | [optional] |
| **payment_link_id**            | **str**                                                                                                         | Identificador único do link de pagamentos ao qual a cobrança pertence            | [optional] |
| **value**                      | **float**                                                                                                       | Valor da cobrança                                                                | [optional] |
| **net_value**                  | **float**                                                                                                       | Valor líquido da cobrança após desconto da tarifa do Asaas                       | [optional] |
| **original_value**             | **float**                                                                                                       | Valor original da cobrança (preenchido quando paga com juros e multa)            | [optional] |
| **interest_value**             | **float**                                                                                                       | Valor calculado de juros e multa que deve ser pago após o vencimento da cobrança | [optional] |
| **description**                | **str**                                                                                                         | Descrição da cobrança                                                            | [optional] |
| **billing_type**               | [**PaymentLeanSaveWithCreditCardResponseBillingType**](PaymentLeanSaveWithCreditCardResponseBillingType.md)     |                                                                                  | [optional] |
| **can_be_paid_after_due_date** | **bool**                                                                                                        | Informa se a cobrança pode ser paga após o vencimento (Somente para boleto)      | [optional] |
| **confirmed_date**             | **date**                                                                                                        | Data de confirmação da cobrança                                                  | [optional] |
| **pix_transaction_id**         | **str**                                                                                                         | Identificador único da transação Pix à qual a cobrança pertence                  | [optional] |
| **status**                     | [**PaymentLeanSaveWithCreditCardResponsePaymentStatus**](PaymentLeanSaveWithCreditCardResponsePaymentStatus.md) |                                                                                  | [optional] |
| **due_date**                   | **date**                                                                                                        | Data de vencimento da cobrança                                                   | [optional] |
| **original_due_date**          | **date**                                                                                                        | Vencimento original no ato da criação da cobrança                                | [optional] |
| **payment_date**               | **date**                                                                                                        | Data de liquidação da cobrança no Asaas                                          | [optional] |
| **customer_payment_date**      | **date**                                                                                                        | Data em que o cliente efetuou o pagamento do boleto                              | [optional] |
| **installment_number**         | **int**                                                                                                         | Número da parcela                                                                | [optional] |
| **external_reference**         | **str**                                                                                                         | Campo livre para busca                                                           | [optional] |
| **deleted**                    | **bool**                                                                                                        | Determina se a cobrança foi removida                                             | [optional] |
| **anticipated**                | **bool**                                                                                                        | Define se a cobrança foi antecipada ou está em processo de antecipação           | [optional] |
| **anticipable**                | **bool**                                                                                                        | Determina se a cobrança é antecipável                                            | [optional] |
| **credit_date**                | **str**                                                                                                         | Data de crédito da cobrança                                                      | [optional] |
| **transaction_receipt_url**    | **str**                                                                                                         | URL do comprovante de confirmação, recebimento, estorno ou remoção.              | [optional] |
| **duplicated_payment_id**      | **str**                                                                                                         | Identificador de cobrança duplicada (caso verdadeiro)                            | [optional] |
| **discount**                   | [**PaymentDiscountDTO**](PaymentDiscountDTO.md)                                                                 |                                                                                  | [optional] |
| **fine**                       | [**PaymentFineResponseDTO**](PaymentFineResponseDTO.md)                                                         |                                                                                  | [optional] |
| **interest**                   | [**PaymentInterestResponseDTO**](PaymentInterestResponseDTO.md)                                                 |                                                                                  | [optional] |
| **postal_service**             | **bool**                                                                                                        | Define se a cobrança será enviada via Correios                                   | [optional] |
| **credit_card**                | [**PaymentSaveWithCreditCardCreditCardDTO**](PaymentSaveWithCreditCardCreditCardDTO.md)                         |                                                                                  | [optional] |

## Example

```python
from asaas.models.payment_lean_save_with_credit_card_response_dto import PaymentLeanSaveWithCreditCardResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLeanSaveWithCreditCardResponseDTO from a JSON string
payment_lean_save_with_credit_card_response_dto_instance = PaymentLeanSaveWithCreditCardResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLeanSaveWithCreditCardResponseDTO.to_json())

# convert the object into a dict
payment_lean_save_with_credit_card_response_dto_dict = payment_lean_save_with_credit_card_response_dto_instance.to_dict()
# create an instance of PaymentLeanSaveWithCreditCardResponseDTO from a dict
payment_lean_save_with_credit_card_response_dto_from_dict = PaymentLeanSaveWithCreditCardResponseDTO.from_dict(payment_lean_save_with_credit_card_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
