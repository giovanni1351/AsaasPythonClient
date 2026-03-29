# PaymentGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** | Tipo do objeto | [optional] 
**id** | **str** | Identificador único da cobrança no Asaas | [optional] 
**date_created** | **date** | Data de criação da cobrança | [optional] 
**customer** | **str** | Identificador único do cliente ao qual a cobrança pertence | [optional] 
**subscription** | **str** | Identificador único da assinatura (quando cobrança recorrente) | [optional] 
**installment** | **str** | Identificador único do parcelamento (quando cobrança parcelada) | [optional] 
**checkout_session** | **str** | Identificador único do checkout | [optional] 
**payment_link** | **str** | Identificador único do link de pagamentos ao qual a cobrança pertence | [optional] 
**value** | **float** | Valor da cobrança | [optional] 
**net_value** | **float** | Valor líquido da cobrança após desconto da tarifa do Asaas | [optional] 
**original_value** | **float** | Valor original da cobrança (preenchido quando paga com juros e multa) | [optional] 
**interest_value** | **float** | Valor calculado de juros e multa que deve ser pago após o vencimento da cobrança | [optional] 
**description** | **str** | Descrição da cobrança | [optional] 
**billing_type** | [**PaymentGetResponseBillingType**](PaymentGetResponseBillingType.md) |  | [optional] 
**credit_card** | [**PaymentSaveWithCreditCardCreditCardDTO**](PaymentSaveWithCreditCardCreditCardDTO.md) |  | [optional] 
**can_be_paid_after_due_date** | **bool** | Informa se a cobrança pode ser paga após o vencimento (Somente para boleto) | [optional] 
**pix_transaction** | **str** | Identificador único da transação Pix à qual a cobrança pertence | [optional] 
**pix_qr_code_id** | **str** | Identificador único do QrCode estático gerado para determinada chave Pix | [optional] 
**status** | [**PaymentGetResponsePaymentStatus**](PaymentGetResponsePaymentStatus.md) |  | [optional] 
**due_date** | **date** | Data de vencimento da cobrança | [optional] 
**original_due_date** | **date** | Vencimento original no ato da criação da cobrança | [optional] 
**payment_date** | **date** | Data de liquidação da cobrança no Asaas | [optional] 
**client_payment_date** | **date** | Data em que o cliente efetuou o pagamento do boleto | [optional] 
**installment_number** | **int** | Número da parcela | [optional] 
**invoice_url** | **str** | URL da fatura | [optional] 
**invoice_number** | **str** | Número da fatura | [optional] 
**external_reference** | **str** | Campo livre para busca | [optional] 
**deleted** | **bool** | Determina se a cobrança foi removida | [optional] 
**anticipated** | **bool** | Define se a cobrança foi antecipada ou está em processo de antecipação | [optional] 
**anticipable** | **bool** | Determina se a cobrança é antecipável | [optional] 
**credit_date** | **date** | Indica a data que o crédito ficou disponível | [optional] 
**estimated_credit_date** | **date** | Data estimada de quando o crédito ficará disponível | [optional] 
**transaction_receipt_url** | **str** | URL do comprovante de confirmação, recebimento, estorno ou remoção. | [optional] 
**nosso_numero** | **str** | Identificação única do boleto | [optional] 
**bank_slip_url** | **str** | URL para download do boleto | [optional] 
**discount** | [**PaymentDiscountDTO**](PaymentDiscountDTO.md) |  | [optional] 
**fine** | [**PaymentFineResponseDTO**](PaymentFineResponseDTO.md) |  | [optional] 
**interest** | [**PaymentInterestResponseDTO**](PaymentInterestResponseDTO.md) |  | [optional] 
**split** | [**List[PaymentSplitGetResponseDTO]**](PaymentSplitGetResponseDTO.md) | Configurações do split | [optional] 
**postal_service** | **bool** | Define se a cobrança será enviada via Correios | [optional] 
**days_after_due_date_to_registration_cancellation** | **int** | Dias após o vencimento para cancelamento do registro (somente para boleto bancário) | [optional] 
**chargeback** | [**PaymentChargebackResponseDTO**](PaymentChargebackResponseDTO.md) |  | [optional] 
**escrow** | [**PaymentEscrowGetResponseDTO**](PaymentEscrowGetResponseDTO.md) |  | [optional] 
**refunds** | [**List[PaymentRefundGetResponseDTO]**](PaymentRefundGetResponseDTO.md) | Informações de estorno | [optional] 

## Example

```python
from asaas.models.payment_get_response_dto import PaymentGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentGetResponseDTO from a JSON string
payment_get_response_dto_instance = PaymentGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentGetResponseDTO.to_json())

# convert the object into a dict
payment_get_response_dto_dict = payment_get_response_dto_instance.to_dict()
# create an instance of PaymentGetResponseDTO from a dict
payment_get_response_dto_from_dict = PaymentGetResponseDTO.from_dict(payment_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


