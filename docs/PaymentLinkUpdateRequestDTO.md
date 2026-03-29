# PaymentLinkUpdateRequestDTO

## Properties

| Name                      | Type                                                                              | Description                                                                                                                                                                                             | Notes                        |
| ------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| **name**                  | **str**                                                                           | Nome do link de pagamentos                                                                                                                                                                              | [optional]                   |
| **description**           | **str**                                                                           | Descrição do link de pagamentos                                                                                                                                                                         | [optional]                   |
| **end_date**              | **str**                                                                           | Data de encerramento                                                                                                                                                                                    | [optional]                   |
| **value**                 | **float**                                                                         | Valor do link de pagamentos, caso não informado o pagador poderá informar o quanto deseja pagar                                                                                                         | [optional]                   |
| **active**                | **bool**                                                                          | Determina se o link de pagamentos está ativo                                                                                                                                                            | [optional]                   |
| **billing_type**          | [**PaymentLinkUpdateRequestBillingType**](PaymentLinkUpdateRequestBillingType.md) |                                                                                                                                                                                                         | [optional]                   |
| **charge_type**           | [**PaymentLinkUpdateRequestChargeType**](PaymentLinkUpdateRequestChargeType.md)   |                                                                                                                                                                                                         | [optional]                   |
| **due_date_limit_days**   | **int**                                                                           | Quantidade de dias úteis que o seu cliente poderá pagar após o boleto ser gerado (Para forma de pagamento como Boleto)                                                                                  | [optional]                   |
| **subscription_cycle**    | [**PaymentLinkUpdateRequestCycle**](PaymentLinkUpdateRequestCycle.md)             |                                                                                                                                                                                                         | [optional]                   |
| **max_installment_count** | **int**                                                                           | Quantidade máxima de parcelas que seu cliente poderá parcelar o valor do link de pagamentos caso a forma de cobrança selecionado seja Parcelamento. Caso não informado o valor padrão será de 1 parcela | [optional] [default to 1]    |
| **external_reference**    | **str**                                                                           | Campo livre para busca                                                                                                                                                                                  | [optional]                   |
| **notification_enabled**  | **bool**                                                                          | Define se os clientes cadastrados pelo link de pagamentos terão as notificações habilitadas. Caso não seja informado o valor padrão será true                                                           | [optional] [default to True] |
| **callback**              | [**PaymentCallbackRequestDTO**](PaymentCallbackRequestDTO.md)                     |                                                                                                                                                                                                         | [optional]                   |

## Example

```python
from asaas.models.payment_link_update_request_dto import PaymentLinkUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLinkUpdateRequestDTO from a JSON string
payment_link_update_request_dto_instance = PaymentLinkUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLinkUpdateRequestDTO.to_json())

# convert the object into a dict
payment_link_update_request_dto_dict = payment_link_update_request_dto_instance.to_dict()
# create an instance of PaymentLinkUpdateRequestDTO from a dict
payment_link_update_request_dto_from_dict = PaymentLinkUpdateRequestDTO.from_dict(payment_link_update_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
