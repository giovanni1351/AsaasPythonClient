# asaas-client

## Requirements.

Python 3.9+

## Installation & Usage

### uv add

```sh
uv add "git+https://github.com/giovanni1351/AsaasPythonClient.git"
```

### pip install

If the python package is hosted on a repository, you can install directly using:

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```

(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/giovanni1351/AsaasPythonClient.git`)

Then import the package:

```python
import asaas
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```

(or `sudo python setup.py install` to install the package for all users)

Then import the package:

```python
import asaas
```

### Tests

Execute `pytest` to run the tests.

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python

import asaas
from asaas.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api-sandbox.asaas.com
# See configuration.py for a list of all supported configuration parameters.
configuration = asaas.Configuration(
    host = "https://api-sandbox.asaas.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: Authorization
configuration.api_key['Authorization'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'


# Enter a context with an instance of the API client
with asaas.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = asaas.AesEmSandboxApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # (Apenas sandbox) Confirmar o pagamento
        api_response = api_instance.confirmar_pagamento(id, body=body)
        print("The response of AesEmSandboxApi->confirmar_pagamento:\n")
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AesEmSandboxApi->confirmar_pagamento: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *https://api-sandbox.asaas.com*

| Class                              | Method                                                                                                                                                                                                 | HTTP request                                                        | Description                                                                     |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| _AesEmSandboxApi_                  | [**confirmar_pagamento**](AesEmSandboxApi.md#confirmar_pagamento)                                                                                                                                      | **POST** /v3/sandbox/payment/{id}/confirm                           | (Apenas sandbox) Confirmar o pagamento                                          |
| _AesEmSandboxApi_                  | [**forcar_vencimento**](AesEmSandboxApi.md#forcar_vencimento)                                                                                                                                          | **POST** /v3/sandbox/payment/{id}/overdue                           | (Apenas sandbox) Forçar o vencimento de uma cobrança                            |
| _AntecipaesApi_                    | [**atualizar_status_da_antecipacao_automatica**](AntecipaesApi.md#atualizar_status_da_antecipacao_automatica)                                                                                          | **PUT** /v3/anticipations/configurations                            | Atualizar status da antecipação automática                                      |
| _AntecipaesApi_                    | [**cancelar_antecipacao**](AntecipaesApi.md#cancelar_antecipacao)                                                                                                                                      | **POST** /v3/anticipations/{id}/cancel                              | Cancelar antecipação                                                            |
| _AntecipaesApi_                    | [**listar_antecipacoes**](AntecipaesApi.md#listar_antecipacoes)                                                                                                                                        | **GET** /v3/anticipations                                           | Listar antecipações                                                             |
| _AntecipaesApi_                    | [**recuperar_limites_de_antecipacoes**](AntecipaesApi.md#recuperar_limites_de_antecipacoes)                                                                                                            | **GET** /v3/anticipations/limits                                    | Recuperar limites de antecipações                                               |
| _AntecipaesApi_                    | [**recuperar_status_da_antecipacao_automatica**](AntecipaesApi.md#recuperar_status_da_antecipacao_automatica)                                                                                          | **GET** /v3/anticipations/configurations                            | Recuperar status da antecipação automática                                      |
| _AntecipaesApi_                    | [**recuperar_uma_unica_antecipacao**](AntecipaesApi.md#recuperar_uma_unica_antecipacao)                                                                                                                | **GET** /v3/anticipations/{id}                                      | Recuperar uma única antecipação                                                 |
| _AntecipaesApi_                    | [**simular_antecipao**](AntecipaesApi.md#simular_antecipao)                                                                                                                                            | **POST** /v3/anticipations/simulate                                 | Simular antecipação                                                             |
| _AntecipaesApi_                    | [**solicitar_antecipacao**](AntecipaesApi.md#solicitar_antecipacao)                                                                                                                                    | **POST** /v3/anticipations                                          | Solicitar antecipação                                                           |
| _AssinaturasApi_                   | [**atualizar_assinatura_existente**](AssinaturasApi.md#atualizar_assinatura_existente)                                                                                                                 | **PUT** /v3/subscriptions/{id}                                      | Atualizar assinatura existente                                                  |
| _AssinaturasApi_                   | [**atualizar_cartao_de_credito_assinatura**](AssinaturasApi.md#atualizar_cartao_de_credito_assinatura)                                                                                                 | **PUT** /v3/subscriptions/{id}/creditCard                           | Atualiza o cartão de crédito sem efetuar cobrança                               |
| _AssinaturasApi_                   | [**atualizar_configuracao_para_emissao_de_notas_fiscais**](AssinaturasApi.md#atualizar_configuracao_para_emissao_de_notas_fiscais)                                                                     | **PUT** /v3/subscriptions/{id}/invoiceSettings                      | Atualizar configuração para emissão de Notas Fiscais                            |
| _AssinaturasApi_                   | [**criar_assinatura_com_cartao_de_credito**](AssinaturasApi.md#criar_assinatura_com_cartao_de_credito)                                                                                                 | **POST** /v3/subscriptions/                                         | Criar assinatura com cartão de crédito                                          |
| _AssinaturasApi_                   | [**criar_configuracao_para_emissao_de_notas_fiscais**](AssinaturasApi.md#criar_configuracao_para_emissao_de_notas_fiscais)                                                                             | **POST** /v3/subscriptions/{id}/invoiceSettings                     | Criar configuração para emissão de Notas Fiscais                                |
| _AssinaturasApi_                   | [**criar_nova_assinatura**](AssinaturasApi.md#criar_nova_assinatura)                                                                                                                                   | **POST** /v3/subscriptions                                          | Criar nova assinatura                                                           |
| _AssinaturasApi_                   | [**gerar_carne_de_assinatura**](AssinaturasApi.md#gerar_carne_de_assinatura)                                                                                                                           | **GET** /v3/subscriptions/{id}/paymentBook                          | Gerar carnê de assinatura                                                       |
| _AssinaturasApi_                   | [**listar_assinaturas**](AssinaturasApi.md#listar_assinaturas)                                                                                                                                         | **GET** /v3/subscriptions                                           | Listar assinaturas                                                              |
| _AssinaturasApi_                   | [**listar_cobrancas_de_uma_assinatura**](AssinaturasApi.md#listar_cobrancas_de_uma_assinatura)                                                                                                         | **GET** /v3/subscriptions/{id}/payments                             | Listar cobranças de uma assinatura                                              |
| _AssinaturasApi_                   | [**listar_notas_fiscais_das_cobrancas_de_uma_assinatura**](AssinaturasApi.md#listar_notas_fiscais_das_cobrancas_de_uma_assinatura)                                                                     | **GET** /v3/subscriptions/{id}/invoices                             | Listar notas fiscais das cobranças de uma assinatura                            |
| _AssinaturasApi_                   | [**recuperar_configuracao_para_emissao_de_notas_fiscais**](AssinaturasApi.md#recuperar_configuracao_para_emissao_de_notas_fiscais)                                                                     | **GET** /v3/subscriptions/{id}/invoiceSettings                      | Recuperar configuração para emissão de notas fiscais                            |
| _AssinaturasApi_                   | [**recuperar_uma_unica_assinatura**](AssinaturasApi.md#recuperar_uma_unica_assinatura)                                                                                                                 | **GET** /v3/subscriptions/{id}                                      | Recuperar uma única assinatura                                                  |
| _AssinaturasApi_                   | [**remover_assinatura**](AssinaturasApi.md#remover_assinatura)                                                                                                                                         | **DELETE** /v3/subscriptions/{id}                                   | Remover assinatura                                                              |
| _AssinaturasApi_                   | [**remover_configuracao_para_emissao_de_notas_fiscais**](AssinaturasApi.md#remover_configuracao_para_emissao_de_notas_fiscais)                                                                         | **DELETE** /v3/subscriptions/{id}/invoiceSettings                   | Remover configuração para emissão de Notas Fiscais                              |
| _CartoDeCrditoApi_                 | [**recuperar_configuracao_de_pre_autorizacao**](CartoDeCrditoApi.md#recuperar_configuracao_de_pre_autorizacao)                                                                                         | **GET** /v3/creditCard/preAuthorization/config                      | Recuperar configuração da pré-autorização                                       |
| _CartoDeCrditoApi_                 | [**salvar_ou_atualizar_configuracao_de_pre_autorizacao**](CartoDeCrditoApi.md#salvar_ou_atualizar_configuracao_de_pre_autorizacao)                                                                     | **POST** /v3/creditCard/preAuthorization/config                     | Salvar ou atualizar configuração da pré-autorização                             |
| _CartoDeCrditoApi_                 | [**tokenizacao_de_cartao_de_credito**](CartoDeCrditoApi.md#tokenizacao_de_cartao_de_credito)                                                                                                           | **POST** /v3/creditCard/tokenizeCreditCard                          | Tokenização de cartão de crédito                                                |
| _ChargebackApi_                    | [**criar_disputa_de_chargeback**](ChargebackApi.md#criar_disputa_de_chargeback)                                                                                                                        | **POST** /v3/chargebacks/{id}/dispute                               | Criar disputa de chargeback                                                     |
| _ChargebackApi_                    | [**listar_chargebacks**](ChargebackApi.md#listar_chargebacks)                                                                                                                                          | **GET** /v3/chargebacks/                                            | Listar chargebacks                                                              |
| _ChargebackApi_                    | [**recuperar_um_unico_chargeback**](ChargebackApi.md#recuperar_um_unico_chargeback)                                                                                                                    | **GET** /v3/payments/{id}/chargeback                                | Recuperar um único chargeback                                                   |
| _CheckoutApi_                      | [**cancelar_um_checkout**](CheckoutApi.md#cancelar_um_checkout)                                                                                                                                        | **POST** /v3/checkouts/{id}/cancel                                  | Cancelar um checkout                                                            |
| _CheckoutApi_                      | [**criar_novo_checkout**](CheckoutApi.md#criar_novo_checkout)                                                                                                                                          | **POST** /v3/checkouts                                              | Criar novo checkout                                                             |
| _ClientesApi_                      | [**atualizar_cliente_existente**](ClientesApi.md#atualizar_cliente_existente)                                                                                                                          | **PUT** /v3/customers/{id}                                          | Atualizar cliente existente                                                     |
| _ClientesApi_                      | [**criar_novo_cliente**](ClientesApi.md#criar_novo_cliente)                                                                                                                                            | **POST** /v3/customers                                              | Criar novo cliente                                                              |
| _ClientesApi_                      | [**listar_clientes**](ClientesApi.md#listar_clientes)                                                                                                                                                  | **GET** /v3/customers                                               | Listar clientes                                                                 |
| _ClientesApi_                      | [**recuperar_notificacoes_de_um_cliente**](ClientesApi.md#recuperar_notificacoes_de_um_cliente)                                                                                                        | **GET** /v3/customers/{id}/notifications                            | Recuperar notificações de um cliente                                            |
| _ClientesApi_                      | [**recuperar_um_unico_cliente**](ClientesApi.md#recuperar_um_unico_cliente)                                                                                                                            | **GET** /v3/customers/{id}                                          | Recuperar um único cliente                                                      |
| _ClientesApi_                      | [**remover_cliente**](ClientesApi.md#remover_cliente)                                                                                                                                                  | **DELETE** /v3/customers/{id}                                       | Remover cliente                                                                 |
| _ClientesApi_                      | [**restaurar_cliente_removido**](ClientesApi.md#restaurar_cliente_removido)                                                                                                                            | **POST** /v3/customers/{id}/restore                                 | Restaurar cliente removido                                                      |
| _CobranasApi_                      | [**atualizar_cobranca_existente**](CobranasApi.md#atualizar_cobranca_existente)                                                                                                                        | **PUT** /v3/payments/{id}                                           | Atualizar cobrança existente                                                    |
| _CobranasApi_                      | [**capturar_cobranca_com_pre_autorizacao**](CobranasApi.md#capturar_cobranca_com_pre_autorizacao)                                                                                                      | **POST** /v3/payments/{id}/captureAuthorizedPayment                 | Capturar cobrança com Pré-Autorização                                           |
| _CobranasApi_                      | [**confirmar_recebimento_em_dinheiro**](CobranasApi.md#confirmar_recebimento_em_dinheiro)                                                                                                              | **POST** /v3/payments/{id}/receiveInCash                            | Confirmar recebimento em dinheiro                                               |
| _CobranasApi_                      | [**criar_cobranca_com_cartao_de_credito**](CobranasApi.md#criar_cobranca_com_cartao_de_credito)                                                                                                        | **POST** /v3/payments/                                              | Criar cobrança com cartão de crédito                                            |
| _CobranasApi_                      | [**criar_nova_cobranca**](CobranasApi.md#criar_nova_cobranca)                                                                                                                                          | **POST** /v3/payments                                               | Criar nova cobrança                                                             |
| _CobranasApi_                      | [**desfazer_confirmacao_de_recebimento_em_dinheiro**](CobranasApi.md#desfazer_confirmacao_de_recebimento_em_dinheiro)                                                                                  | **POST** /v3/payments/{id}/undoReceivedInCash                       | Desfazer confirmação de recebimento em dinheiro                                 |
| _CobranasApi_                      | [**estornar_cobranca**](CobranasApi.md#estornar_cobranca)                                                                                                                                              | **POST** /v3/payments/{id}/refund                                   | Estornar cobrança                                                               |
| _CobranasApi_                      | [**excluir_cobranca**](CobranasApi.md#excluir_cobranca)                                                                                                                                                | **DELETE** /v3/payments/{id}                                        | Excluir cobrança                                                                |
| _CobranasApi_                      | [**informacoes_sobre_visualizacao_da_cobranca**](CobranasApi.md#informacoes_sobre_visualizacao_da_cobranca)                                                                                            | **GET** /v3/payments/{id}/viewingInfo                               | Informações sobre visualização da cobrança                                      |
| _CobranasApi_                      | [**listar_cobrancas**](CobranasApi.md#listar_cobrancas)                                                                                                                                                | **GET** /v3/payments                                                | Listar cobranças                                                                |
| _CobranasApi_                      | [**obter_linha_digitavel_do_boleto**](CobranasApi.md#obter_linha_digitavel_do_boleto)                                                                                                                  | **GET** /v3/payments/{id}/identificationField                       | Obter linha digitável do boleto                                                 |
| _CobranasApi_                      | [**obter_qr_code_para_pagamentos_via_pix**](CobranasApi.md#obter_qr_code_para_pagamentos_via_pix)                                                                                                      | **GET** /v3/payments/{id}/pixQrCode                                 | Obter QR Code para pagamentos via Pix                                           |
| _CobranasApi_                      | [**pagar_uma_cobranca_com_cartao_de_credito**](CobranasApi.md#pagar_uma_cobranca_com_cartao_de_credito)                                                                                                | **POST** /v3/payments/{id}/payWithCreditCard                        | Pagar uma cobrança com cartão de crédito                                        |
| _CobranasApi_                      | [**recuperando_limites_de_cobrancas**](CobranasApi.md#recuperando_limites_de_cobrancas)                                                                                                                | **GET** /v3/payments/limits                                         | Recuperando limites de cobranças                                                |
| _CobranasApi_                      | [**recuperar_informacoes_de_pagamento_de_uma_cobranca**](CobranasApi.md#recuperar_informacoes_de_pagamento_de_uma_cobranca)                                                                            | **GET** /v3/payments/{id}/billingInfo                               | Recuperar informações de pagamento de uma cobrança                              |
| _CobranasApi_                      | [**recuperar_status_de_uma_cobranca**](CobranasApi.md#recuperar_status_de_uma_cobranca)                                                                                                                | **GET** /v3/payments/{id}/status                                    | Recuperar status de uma cobrança                                                |
| _CobranasApi_                      | [**recuperar_uma_unica_cobranca**](CobranasApi.md#recuperar_uma_unica_cobranca)                                                                                                                        | **GET** /v3/payments/{id}                                           | Recuperar uma única cobrança                                                    |
| _CobranasApi_                      | [**restaurar_cobranca_removida**](CobranasApi.md#restaurar_cobranca_removida)                                                                                                                          | **POST** /v3/payments/{id}/restore                                  | Restaurar cobrança removida                                                     |
| _CobranasApi_                      | [**simulador_de_vendas**](CobranasApi.md#simulador_de_vendas)                                                                                                                                          | **POST** /v3/payments/simulate                                      | Simulador de vendas                                                             |
| _CobranasComDadosResumidosApi_     | [**atualizar_cobranca_existente_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#atualizar_cobranca_existente_com_dados_resumidos_na_resposta)                                       | **PUT** /v3/lean/payments/{id}                                      | Atualizar cobrança existente com dados resumidos na resposta                    |
| _CobranasComDadosResumidosApi_     | [**capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta)                     | **POST** /v3/lean/payments/{id}/captureAuthorizedPayment            | Capturar cobrança com Pré-Autorização com dados resumidos na resposta           |
| _CobranasComDadosResumidosApi_     | [**confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta)                             | **POST** /v3/lean/payments/{id}/receiveInCash                       | Confirmar recebimento em dinheiro com dados resumidos na resposta               |
| _CobranasComDadosResumidosApi_     | [**criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta)                       | **POST** /v3/lean/payments/                                         | Criar cobrança com cartão de crédito com dados resumidos na resposta            |
| _CobranasComDadosResumidosApi_     | [**criar_nova_cobranca_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#criar_nova_cobranca_com_dados_resumidos_na_resposta)                                                         | **POST** /v3/lean/payments                                          | Criar nova cobrança com dados resumidos na resposta                             |
| _CobranasComDadosResumidosApi_     | [**desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta) | **POST** /v3/lean/payments/{id}/undoReceivedInCash                  | Desfazer confirmação de recebimento em dinheiro com dados resumidos na resposta |
| _CobranasComDadosResumidosApi_     | [**estornar_cobranca_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#estornar_cobranca_com_dados_resumidos_na_resposta)                                                             | **POST** /v3/lean/payments/{id}/refund                              | Estornar cobrança com dados resumidos na resposta                               |
| _CobranasComDadosResumidosApi_     | [**excluir_cobranca_com_dados_resumidos**](CobranasComDadosResumidosApi.md#excluir_cobranca_com_dados_resumidos)                                                                                       | **DELETE** /v3/lean/payments/{id}                                   | Excluir cobrança com dados resumidos                                            |
| _CobranasComDadosResumidosApi_     | [**listar_cobrancas_com_dados_resumidos**](CobranasComDadosResumidosApi.md#listar_cobrancas_com_dados_resumidos)                                                                                       | **GET** /v3/lean/payments                                           | Listar cobranças com dados resumidos                                            |
| _CobranasComDadosResumidosApi_     | [**recuperar_uma_unica_cobranca_com_dados_resumidos**](CobranasComDadosResumidosApi.md#recuperar_uma_unica_cobranca_com_dados_resumidos)                                                               | **GET** /v3/lean/payments/{id}                                      | Recuperar uma única cobrança com dados resumidos                                |
| _CobranasComDadosResumidosApi_     | [**restaurar_cobranca_removida_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#restaurar_cobranca_removida_com_dados_resumidos_na_resposta)                                         | **POST** /v3/lean/payments/{id}/restore                             | Restaurar cobrança removida com dados resumidos na resposta                     |
| _ConfiguraesDeWebhooksApi_         | [**atualizar_webhook_existente**](ConfiguraesDeWebhooksApi.md#atualizar_webhook_existente)                                                                                                             | **PUT** /v3/webhooks/{id}                                           | Atualizar webhook existente                                                     |
| _ConfiguraesDeWebhooksApi_         | [**criar_novo_webhook**](ConfiguraesDeWebhooksApi.md#criar_novo_webhook)                                                                                                                               | **POST** /v3/webhooks                                               | Criar novo webhook                                                              |
| _ConfiguraesDeWebhooksApi_         | [**listar_webhooks**](ConfiguraesDeWebhooksApi.md#listar_webhooks)                                                                                                                                     | **GET** /v3/webhooks                                                | Listar webhooks                                                                 |
| _ConfiguraesDeWebhooksApi_         | [**recuperar_um_unico_webhook**](ConfiguraesDeWebhooksApi.md#recuperar_um_unico_webhook)                                                                                                               | **GET** /v3/webhooks/{id}                                           | Recuperar um único webhook                                                      |
| _ConfiguraesDeWebhooksApi_         | [**remover_penalizacao_webhook**](ConfiguraesDeWebhooksApi.md#remover_penalizacao_webhook)                                                                                                             | **POST** /v3/webhooks/{id}/removeBackoff                            | Remover penalização de webhook                                                  |
| _ConfiguraesDeWebhooksApi_         | [**remover_webhook**](ConfiguraesDeWebhooksApi.md#remover_webhook)                                                                                                                                     | **DELETE** /v3/webhooks/{id}                                        | Remover um webhook                                                              |
| _ConsultaSerasaApi_                | [**listar_consultas**](ConsultaSerasaApi.md#listar_consultas)                                                                                                                                          | **GET** /v3/creditBureauReport                                      | Listar consultas                                                                |
| _ConsultaSerasaApi_                | [**realizar_consulta**](ConsultaSerasaApi.md#realizar_consulta)                                                                                                                                        | **POST** /v3/creditBureauReport                                     | Realizar consulta                                                               |
| _ConsultaSerasaApi_                | [**recuperar_uma_consulta**](ConsultaSerasaApi.md#recuperar_uma_consulta)                                                                                                                              | **GET** /v3/creditBureauReport/{id}                                 | Recuperar uma consulta                                                          |
| _ContaEscrowApi_                   | [**criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas**](ContaEscrowApi.md#criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas)                                           | **POST** /v3/accounts/escrow                                        | Criar configuração padrão da Conta Escrow para todas as subcontas               |
| _ContaEscrowApi_                   | [**encerrar_garantia_da_cobranca_na_conta_escrow**](ContaEscrowApi.md#encerrar_garantia_da_cobranca_na_conta_escrow)                                                                                   | **POST** /v3/escrow/{id}/finish                                     | Encerrar garantia da cobrança na Conta Escrow                                   |
| _ContaEscrowApi_                   | [**recuperar_configuracao_da_conta_escrow_para_a_subconta**](ContaEscrowApi.md#recuperar_configuracao_da_conta_escrow_para_a_subconta)                                                                 | **GET** /v3/accounts/{id}/escrow                                    | Recuperar configuração da Conta Escrow para a subconta                          |
| _ContaEscrowApi_                   | [**recuperar_configuracao_padrao_da_conta_escrow**](ContaEscrowApi.md#recuperar_configuracao_padrao_da_conta_escrow)                                                                                   | **GET** /v3/accounts/escrow                                         | Recuperar configuração padrão da Conta Escrow                                   |
| _ContaEscrowApi_                   | [**recuperar_garantia_da_cobranca_na_conta_escrow**](ContaEscrowApi.md#recuperar_garantia_da_cobranca_na_conta_escrow)                                                                                 | **GET** /v3/payments/{id}/escrow                                    | Recuperar garantia da cobrança na Conta Escrow                                  |
| _ContaEscrowApi_                   | [**salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta**](ContaEscrowApi.md#salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta)                                             | **POST** /v3/accounts/{id}/escrow                                   | Salvar ou atualizar configuração da Conta Escrow para a subconta                |
| _DocumentosDeCobranasApi_          | [**atualizar_definicoes_de_um_documento_da_cobranca**](DocumentosDeCobranasApi.md#atualizar_definicoes_de_um_documento_da_cobranca)                                                                    | **PUT** /v3/payments/{id}/documents/{documentId}                    | Atualizar definições de um documento da cobrança                                |
| _DocumentosDeCobranasApi_          | [**excluir_documento_de_uma_cobranca**](DocumentosDeCobranasApi.md#excluir_documento_de_uma_cobranca)                                                                                                  | **DELETE** /v3/payments/{id}/documents/{documentId}                 | Excluir documento de uma cobrança                                               |
| _DocumentosDeCobranasApi_          | [**fazer_upload_de_documentos_da_cobranca**](DocumentosDeCobranasApi.md#fazer_upload_de_documentos_da_cobranca)                                                                                        | **POST** /v3/payments/{id}/documents                                | Fazer upload de documentos da cobrança                                          |
| _DocumentosDeCobranasApi_          | [**listar_documentos_de_uma_cobranca**](DocumentosDeCobranasApi.md#listar_documentos_de_uma_cobranca)                                                                                                  | **GET** /v3/payments/{id}/documents                                 | Listar documentos de uma cobrança                                               |
| _DocumentosDeCobranasApi_          | [**recuperar_um_unico_documento_da_cobranca**](DocumentosDeCobranasApi.md#recuperar_um_unico_documento_da_cobranca)                                                                                    | **GET** /v3/payments/{id}/documents/{documentId}                    | Recuperar um único documento da cobrança                                        |
| _EnvioDeDocumentosWhiteLabelApi_   | [**atualizar_documento_enviado**](EnvioDeDocumentosWhiteLabelApi.md#atualizar_documento_enviado)                                                                                                       | **POST** /v3/myAccount/documents/files/{id}                         | Atualizar documento enviado                                                     |
| _EnvioDeDocumentosWhiteLabelApi_   | [**enviar_documentos**](EnvioDeDocumentosWhiteLabelApi.md#enviar_documentos)                                                                                                                           | **POST** /v3/myAccount/documents/{id}                               | Enviar documentos                                                               |
| _EnvioDeDocumentosWhiteLabelApi_   | [**remover_documento_enviado**](EnvioDeDocumentosWhiteLabelApi.md#remover_documento_enviado)                                                                                                           | **DELETE** /v3/myAccount/documents/files/{id}                       | Remover documento enviado                                                       |
| _EnvioDeDocumentosWhiteLabelApi_   | [**verificar_documentos_pendentes**](EnvioDeDocumentosWhiteLabelApi.md#verificar_documentos_pendentes)                                                                                                 | **GET** /v3/myAccount/documents                                     | Verificar documentos pendentes                                                  |
| _EnvioDeDocumentosWhiteLabelApi_   | [**visualizar_documento_enviado**](EnvioDeDocumentosWhiteLabelApi.md#visualizar_documento_enviado)                                                                                                     | **GET** /v3/myAccount/documents/files/{id}                          | Visualizar documento enviado                                                    |
| _EstornosApi_                      | [**estornar_boleto**](EstornosApi.md#estornar_boleto)                                                                                                                                                  | **POST** /v3/payments/{id}/bankSlip/refund                          | Estornar boleto                                                                 |
| _EstornosApi_                      | [**listar_estornos_de_uma_cobranca**](EstornosApi.md#listar_estornos_de_uma_cobranca)                                                                                                                  | **GET** /v3/payments/{id}/refunds                                   | Listar estornos de uma cobrança                                                 |
| _ExtratoApi_                       | [**recuperar_extrato**](ExtratoApi.md#recuperar_extrato)                                                                                                                                               | **GET** /v3/financialTransactions                                   | Recuperar extrato                                                               |
| _InformaesEPersonalizaoDaContaApi_ | [**aprovar_conta**](InformaesEPersonalizaoDaContaApi.md#aprovar_conta)                                                                                                                                 | **POST** /v3/sandbox/myAccount/approve                              | (Apenas Sandbox) Aprovar conta                                                  |
| _InformaesEPersonalizaoDaContaApi_ | [**atualizar_dados_comerciais**](InformaesEPersonalizaoDaContaApi.md#atualizar_dados_comerciais)                                                                                                       | **POST** /v3/myAccount/commercialInfo/                              | Atualizar dados comerciais                                                      |
| _InformaesEPersonalizaoDaContaApi_ | [**consultar_situacao_cadastral_da_conta**](InformaesEPersonalizaoDaContaApi.md#consultar_situacao_cadastral_da_conta)                                                                                 | **GET** /v3/myAccount/status/                                       | Consultar situação cadastral da conta                                           |
| _InformaesEPersonalizaoDaContaApi_ | [**excluir_subconta_white_label**](InformaesEPersonalizaoDaContaApi.md#excluir_subconta_white_label)                                                                                                   | **DELETE** /v3/myAccount/                                           | Excluir subconta White Label                                                    |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_configuracoes_de_personalizacao**](InformaesEPersonalizaoDaContaApi.md#recuperar_configuracoes_de_personalizacao)                                                                         | **GET** /v3/myAccount/paymentCheckoutConfig/                        | Recuperar configurações de personalização                                       |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_dados_comerciais**](InformaesEPersonalizaoDaContaApi.md#recuperar_dados_comerciais)                                                                                                       | **GET** /v3/myAccount/commercialInfo/                               | Recuperar dados comerciais                                                      |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_numero_de_conta_no_asaas**](InformaesEPersonalizaoDaContaApi.md#recuperar_numero_de_conta_no_asaas)                                                                                       | **GET** /v3/myAccount/accountNumber                                 | Recuperar número de conta no Asaas                                              |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_taxas_da_conta**](InformaesEPersonalizaoDaContaApi.md#recuperar_taxas_da_conta)                                                                                                           | **GET** /v3/myAccount/fees/                                         | Recuperar taxas da conta                                                        |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_walletid**](InformaesEPersonalizaoDaContaApi.md#recuperar_walletid)                                                                                                                       | **GET** /v3/wallets/                                                | Recuperar WalletId                                                              |
| _InformaesEPersonalizaoDaContaApi_ | [**salvar_personalizacao_da_fatura**](InformaesEPersonalizaoDaContaApi.md#salvar_personalizacao_da_fatura)                                                                                             | **POST** /v3/myAccount/paymentCheckoutConfig/                       | Salvar personalização da fatura                                                 |
| _InformaesFinanceirasApi_          | [**estatisticas_de_cobrancas**](InformaesFinanceirasApi.md#estatisticas_de_cobrancas)                                                                                                                  | **GET** /v3/finance/payment/statistics                              | Estatísticas de cobranças                                                       |
| _InformaesFinanceirasApi_          | [**recuperar_saldo_da_conta**](InformaesFinanceirasApi.md#recuperar_saldo_da_conta)                                                                                                                    | **GET** /v3/finance/balance                                         | Recuperar saldo da conta                                                        |
| _InformaesFinanceirasApi_          | [**recuperar_valores_de_split**](InformaesFinanceirasApi.md#recuperar_valores_de_split)                                                                                                                | **GET** /v3/finance/split/statistics                                | Recuperar valores de split                                                      |
| _InformaesFiscaisApi_              | [**configurar_portal_emissor_de_notas_fiscais**](InformaesFiscaisApi.md#configurar_portal_emissor_de_notas_fiscais)                                                                                    | **POST** /v3/fiscalInfo/nationalPortal                              | Configurar portal emissor de notas fiscais                                      |
| _InformaesFiscaisApi_              | [**criar_e_atualizar_informacoes_fiscais**](InformaesFiscaisApi.md#criar_e_atualizar_informacoes_fiscais)                                                                                              | **POST** /v3/fiscalInfo/                                            | Criar e atualizar informações fiscais                                           |
| _InformaesFiscaisApi_              | [**listar_codigos_de_classificacoes_tributarias**](InformaesFiscaisApi.md#listar_codigos_de_classificacoes_tributarias)                                                                                | **GET** /v3/fiscalInfo/taxClassificationCodes                       | Listar códigos de classificações tributárias                                    |
| _InformaesFiscaisApi_              | [**listar_codigos_de_operadores_de_indicacoes**](InformaesFiscaisApi.md#listar_codigos_de_operadores_de_indicacoes)                                                                                    | **GET** /v3/fiscalInfo/operationIndicatorCodes                      | Listar códigos de indicadores de operações                                      |
| _InformaesFiscaisApi_              | [**listar_codigos_de_situacoes_tributarias**](InformaesFiscaisApi.md#listar_codigos_de_situacoes_tributarias)                                                                                          | **GET** /v3/fiscalInfo/taxSituationCodes                            | Listar códigos de situações tributárias                                         |
| _InformaesFiscaisApi_              | [**listar_codigos_nbs**](InformaesFiscaisApi.md#listar_codigos_nbs)                                                                                                                                    | **GET** /v3/fiscalInfo/nbsCodes                                     | Listar códigos NBS                                                              |
| _InformaesFiscaisApi_              | [**listar_codigos_servicos_federais**](InformaesFiscaisApi.md#listar_codigos_servicos_federais)                                                                                                        | **GET** /v3/fiscalInfo/federalServiceCodes                          | Listar códigos de serviços federais                                             |
| _InformaesFiscaisApi_              | [**listar_configuracoes_municipais**](InformaesFiscaisApi.md#listar_configuracoes_municipais)                                                                                                          | **GET** /v3/fiscalInfo/municipalOptions                             | Listar configurações municipais                                                 |
| _InformaesFiscaisApi_              | [**listar_servicos_municipais**](InformaesFiscaisApi.md#listar_servicos_municipais)                                                                                                                    | **GET** /v3/fiscalInfo/services                                     | Listar serviços municipais                                                      |
| _InformaesFiscaisApi_              | [**recuperar_informacoes_fiscais**](InformaesFiscaisApi.md#recuperar_informacoes_fiscais)                                                                                                              | **GET** /v3/fiscalInfo/                                             | Recuperar informações fiscais                                                   |
| _LinkDePagamentosApi_              | [**adicionar_uma_imagem_aum_link_de_pagamentos**](LinkDePagamentosApi.md#adicionar_uma_imagem_aum_link_de_pagamentos)                                                                                  | **POST** /v3/paymentLinks/{id}/images                               | Adicionar uma imagem a um link de pagamentos                                    |
| _LinkDePagamentosApi_              | [**atualizar_um_link_de_pagamentos**](LinkDePagamentosApi.md#atualizar_um_link_de_pagamentos)                                                                                                          | **PUT** /v3/paymentLinks/{id}                                       | Atualizar um link de pagamentos                                                 |
| _LinkDePagamentosApi_              | [**criar_um_link_de_pagamentos**](LinkDePagamentosApi.md#criar_um_link_de_pagamentos)                                                                                                                  | **POST** /v3/paymentLinks                                           | Criar um link de pagamentos                                                     |
| _LinkDePagamentosApi_              | [**definir_imagem_principal_do_link_de_pagamentos**](LinkDePagamentosApi.md#definir_imagem_principal_do_link_de_pagamentos)                                                                            | **PUT** /v3/paymentLinks/{paymentLinkId}/images/{imageId}/setAsMain | Definir imagem principal do link de pagamentos                                  |
| _LinkDePagamentosApi_              | [**listar_imagens_de_um_link_de_pagamentos**](LinkDePagamentosApi.md#listar_imagens_de_um_link_de_pagamentos)                                                                                          | **GET** /v3/paymentLinks/{id}/images                                | Listar imagens de um link de pagamentos                                         |
| _LinkDePagamentosApi_              | [**listar_links_de_pagamentos**](LinkDePagamentosApi.md#listar_links_de_pagamentos)                                                                                                                    | **GET** /v3/paymentLinks                                            | Listar links de pagamentos                                                      |
| _LinkDePagamentosApi_              | [**recuperar_um_unico_link_de_pagamentos**](LinkDePagamentosApi.md#recuperar_um_unico_link_de_pagamentos)                                                                                              | **GET** /v3/paymentLinks/{id}                                       | Recuperar um único link de pagamentos                                           |
| _LinkDePagamentosApi_              | [**recuperar_uma_unica_imagem_do_link_de_pagamentos**](LinkDePagamentosApi.md#recuperar_uma_unica_imagem_do_link_de_pagamentos)                                                                        | **GET** /v3/paymentLinks/{paymentLinkId}/images/{imageId}           | Recuperar uma única imagem do link de pagamentos                                |
| _LinkDePagamentosApi_              | [**remover_um_link_de_pagamentos**](LinkDePagamentosApi.md#remover_um_link_de_pagamentos)                                                                                                              | **DELETE** /v3/paymentLinks/{id}                                    | Remover um link de pagamentos                                                   |
| _LinkDePagamentosApi_              | [**remover_uma_imagem_do_link_de_pagamentos**](LinkDePagamentosApi.md#remover_uma_imagem_do_link_de_pagamentos)                                                                                        | **DELETE** /v3/paymentLinks/{paymentLinkId}/images/{imageId}        | Remover uma imagem do link de pagamentos                                        |
| _LinkDePagamentosApi_              | [**restaurar_um_link_de_pagamentos**](LinkDePagamentosApi.md#restaurar_um_link_de_pagamentos)                                                                                                          | **POST** /v3/paymentLinks/{id}/restore                              | Restaurar um link de pagamentos                                                 |
| _NegativaesApi_                    | [**cancelar_negativacao**](NegativaesApi.md#cancelar_negativacao)                                                                                                                                      | **POST** /v3/paymentDunnings/{id}/cancel                            | Cancelar negativação                                                            |
| _NegativaesApi_                    | [**criar_uma_negativacao**](NegativaesApi.md#criar_uma_negativacao)                                                                                                                                    | **POST** /v3/paymentDunnings                                        | Criar uma negativação                                                           |
| _NegativaesApi_                    | [**listar_cobrancas_disponiveis_para_negativacao**](NegativaesApi.md#listar_cobrancas_disponiveis_para_negativacao)                                                                                    | **GET** /v3/paymentDunnings/paymentsAvailableForDunning             | Listar cobranças disponíveis para negativação                                   |
| _NegativaesApi_                    | [**listar_historico_de_eventos**](NegativaesApi.md#listar_historico_de_eventos)                                                                                                                        | **GET** /v3/paymentDunnings/{id}/history                            | Listar histórico de eventos                                                     |
| _NegativaesApi_                    | [**listar_negativacoes**](NegativaesApi.md#listar_negativacoes)                                                                                                                                        | **GET** /v3/paymentDunnings                                         | Listar negativações                                                             |
| _NegativaesApi_                    | [**listar_pagamentos_recebidos**](NegativaesApi.md#listar_pagamentos_recebidos)                                                                                                                        | **GET** /v3/paymentDunnings/{id}/partialPayments                    | Listar pagamentos recebidos                                                     |
| _NegativaesApi_                    | [**recuperar_uma_unica_negativacao**](NegativaesApi.md#recuperar_uma_unica_negativacao)                                                                                                                | **GET** /v3/paymentDunnings/{id}                                    | Recuperar uma única negativação                                                 |
| _NegativaesApi_                    | [**reenviar_documentos**](NegativaesApi.md#reenviar_documentos)                                                                                                                                        | **POST** /v3/paymentDunnings/{id}/documents                         | Reenviar documentos                                                             |
| _NegativaesApi_                    | [**simular_uma_negativacao**](NegativaesApi.md#simular_uma_negativacao)                                                                                                                                | **POST** /v3/paymentDunnings/simulate                               | Simular uma negativação                                                         |
| _NotasFiscaisApi_                  | [**agendar_nota_fiscal**](NotasFiscaisApi.md#agendar_nota_fiscal)                                                                                                                                      | **POST** /v3/invoices                                               | Agendar nota fiscal                                                             |
| _NotasFiscaisApi_                  | [**atualizar_nota_fiscal**](NotasFiscaisApi.md#atualizar_nota_fiscal)                                                                                                                                  | **PUT** /v3/invoices/{id}                                           | Atualizar nota fiscal                                                           |
| _NotasFiscaisApi_                  | [**cancelar_uma_nota_fiscal**](NotasFiscaisApi.md#cancelar_uma_nota_fiscal)                                                                                                                            | **POST** /v3/invoices/{id}/cancel                                   | Cancelar uma nota fiscal                                                        |
| _NotasFiscaisApi_                  | [**emitir_uma_nota_fiscal**](NotasFiscaisApi.md#emitir_uma_nota_fiscal)                                                                                                                                | **POST** /v3/invoices/{id}/authorize                                | Emitir uma nota fiscal                                                          |
| _NotasFiscaisApi_                  | [**listar_notas_fiscais**](NotasFiscaisApi.md#listar_notas_fiscais)                                                                                                                                    | **GET** /v3/invoices                                                | Listar notas fiscais                                                            |
| _NotasFiscaisApi_                  | [**recuperar_uma_nota_fiscal**](NotasFiscaisApi.md#recuperar_uma_nota_fiscal)                                                                                                                          | **GET** /v3/invoices/{id}                                           | Recuperar uma única nota fiscal                                                 |
| _NotificaesApi_                    | [**atualizar_notificacao_existente**](NotificaesApi.md#atualizar_notificacao_existente)                                                                                                                | **PUT** /v3/notifications/{id}                                      | Atualizar notificação existente                                                 |
| _NotificaesApi_                    | [**atualizar_notificacoes_existentes_em_lote**](NotificaesApi.md#atualizar_notificacoes_existentes_em_lote)                                                                                            | **PUT** /v3/notifications/batch                                     | Atualizar notificações existentes em lote                                       |
| _PagamentoDeContasApi_             | [**cancelar_pagamento_de_contas**](PagamentoDeContasApi.md#cancelar_pagamento_de_contas)                                                                                                               | **POST** /v3/bill/{id}/cancel                                       | Cancelar pagamento de contas                                                    |
| _PagamentoDeContasApi_             | [**criar_um_pagamento_de_conta**](PagamentoDeContasApi.md#criar_um_pagamento_de_conta)                                                                                                                 | **POST** /v3/bill                                                   | Criar um pagamento de conta                                                     |
| _PagamentoDeContasApi_             | [**listar_pagamento_de_contas**](PagamentoDeContasApi.md#listar_pagamento_de_contas)                                                                                                                   | **GET** /v3/bill                                                    | Listar pagamento de contas                                                      |
| _PagamentoDeContasApi_             | [**recuperar_um_unico_pagamento_de_conta**](PagamentoDeContasApi.md#recuperar_um_unico_pagamento_de_conta)                                                                                             | **GET** /v3/bill/{id}                                               | Recuperar um único pagamento de conta                                           |
| _PagamentoDeContasApi_             | [**simular_um_pagamento_de_conta**](PagamentoDeContasApi.md#simular_um_pagamento_de_conta)                                                                                                             | **POST** /v3/bill/simulate                                          | Simular um pagamento de conta                                                   |
| _ParcelamentosApi_                 | [**atualizar_splits_do_parcelamento**](ParcelamentosApi.md#atualizar_splits_do_parcelamento)                                                                                                           | **PUT** /v3/installments/{id}/splits                                | Atualizar splits do parcelamento                                                |
| _ParcelamentosApi_                 | [**cancelar_cobrancas_de_um_parcelamento**](ParcelamentosApi.md#cancelar_cobrancas_de_um_parcelamento)                                                                                                 | **DELETE** /v3/installments/{id}/payments                           | Cancelar cobranças de um parcelamento (pendentes e vencidas)                    |
| _ParcelamentosApi_                 | [**criar_parcelamento**](ParcelamentosApi.md#criar_parcelamento)                                                                                                                                       | **POST** /v3/installments                                           | Criar parcelamento                                                              |
| _ParcelamentosApi_                 | [**criar_parcelamento_com_carto_de_crdito**](ParcelamentosApi.md#criar_parcelamento_com_carto_de_crdito)                                                                                               | **POST** /v3/installments/                                          | Criar parcelamento com cartão de crédito                                        |
| _ParcelamentosApi_                 | [**estornar_parcelamento**](ParcelamentosApi.md#estornar_parcelamento)                                                                                                                                 | **POST** /v3/installments/{id}/refund                               | Estornar parcelamento                                                           |
| _ParcelamentosApi_                 | [**gerar_carne_de_parcelamento**](ParcelamentosApi.md#gerar_carne_de_parcelamento)                                                                                                                     | **GET** /v3/installments/{id}/paymentBook                           | Gerar carnê de parcelamento                                                     |
| _ParcelamentosApi_                 | [**listar_cobranas_de_um_parcelamento**](ParcelamentosApi.md#listar_cobranas_de_um_parcelamento)                                                                                                       | **GET** /v3/installments/{id}/payments                              | Listar cobranças de um parcelamento                                             |
| _ParcelamentosApi_                 | [**listar_parcelamentos**](ParcelamentosApi.md#listar_parcelamentos)                                                                                                                                   | **GET** /v3/installments                                            | Listar parcelamentos                                                            |
| _ParcelamentosApi_                 | [**recuperar_um_unico_parcelamento**](ParcelamentosApi.md#recuperar_um_unico_parcelamento)                                                                                                             | **GET** /v3/installments/{id}                                       | Recuperar um único parcelamento                                                 |
| _ParcelamentosApi_                 | [**remover_parcelamento**](ParcelamentosApi.md#remover_parcelamento)                                                                                                                                   | **DELETE** /v3/installments/{id}                                    | Remover parcelamento                                                            |
| _PixApi_                           | [**consulta_de_fichas_disponiveis_no_balde**](PixApi.md#consulta_de_fichas_disponiveis_no_balde)                                                                                                       | **GET** /v3/pix/tokenBucket/addressKey                              | Consulta de fichas disponíveis no balde                                         |
| _PixApi_                           | [**criar_qrcode_estatico**](PixApi.md#criar_qrcode_estatico)                                                                                                                                           | **POST** /v3/pix/qrCodes/static                                     | Criar QR Code estático                                                          |
| _PixApi_                           | [**criar_uma_chave**](PixApi.md#criar_uma_chave)                                                                                                                                                       | **POST** /v3/pix/addressKeys                                        | Criar uma chave                                                                 |
| _PixApi_                           | [**deletar_qrcode_estatico**](PixApi.md#deletar_qrcode_estatico)                                                                                                                                       | **DELETE** /v3/pix/qrCodes/static/{id}                              | Deletar QR Code estático                                                        |
| _PixApi_                           | [**listar_chaves**](PixApi.md#listar_chaves)                                                                                                                                                           | **GET** /v3/pix/addressKeys                                         | Listar chaves                                                                   |
| _PixApi_                           | [**recuperar_uma_unica_chave**](PixApi.md#recuperar_uma_unica_chave)                                                                                                                                   | **GET** /v3/pix/addressKeys/{id}                                    | Recuperar uma única chave                                                       |
| _PixApi_                           | [**remover_chave**](PixApi.md#remover_chave)                                                                                                                                                           | **DELETE** /v3/pix/addressKeys/{id}                                 | Remover chave                                                                   |
| _PixAutomticoApi_                  | [**cancelar_uma_autorizacao_pix_automatico**](PixAutomticoApi.md#cancelar_uma_autorizacao_pix_automatico)                                                                                              | **DELETE** /v3/pix/automatic/authorizations/{id}                    | Cancelar uma autorização                                                        |
| _PixAutomticoApi_                  | [**criar_uma_autorizacao_pix_automatico**](PixAutomticoApi.md#criar_uma_autorizacao_pix_automatico)                                                                                                    | **POST** /v3/pix/automatic/authorizations                           | Criar uma autorização                                                           |
| _PixAutomticoApi_                  | [**listar_autorizacoes_pix_automatico**](PixAutomticoApi.md#listar_autorizacoes_pix_automatico)                                                                                                        | **GET** /v3/pix/automatic/authorizations                            | Listar autorizações                                                             |
| _PixAutomticoApi_                  | [**listar_instrucoes_de_pagamento_pix_automatico**](PixAutomticoApi.md#listar_instrucoes_de_pagamento_pix_automatico)                                                                                  | **GET** /v3/pix/automatic/paymentInstructions                       | Listar instruções de pagamento                                                  |
| _PixAutomticoApi_                  | [**recuperar_uma_unica_autorizacao_pix_automatico**](PixAutomticoApi.md#recuperar_uma_unica_autorizacao_pix_automatico)                                                                                | **GET** /v3/pix/automatic/authorizations/{id}                       | Recuperar uma única autorização                                                 |
| _PixAutomticoApi_                  | [**recuperar_uma_unica_instrucao_de_pagamento_pix_automatico**](PixAutomticoApi.md#recuperar_uma_unica_instrucao_de_pagamento_pix_automatico)                                                          | **GET** /v3/pix/automatic/paymentInstructions/{id}                  | Recuperar uma única instrução de pagamento                                      |
| _PixRecorrenteApi_                 | [**cancelar_item_de_uma_recorrencia**](PixRecorrenteApi.md#cancelar_item_de_uma_recorrencia)                                                                                                           | **POST** /v3/pix/transactions/recurrings/items/{id}/cancel          | Cancelar item de uma recorrência                                                |
| _PixRecorrenteApi_                 | [**cancelar_uma_recorrencia**](PixRecorrenteApi.md#cancelar_uma_recorrencia)                                                                                                                           | **POST** /v3/pix/transactions/recurrings/{id}/cancel                | Cancelar uma recorrência                                                        |
| _PixRecorrenteApi_                 | [**listar_itens_de_uma_recorrencia**](PixRecorrenteApi.md#listar_itens_de_uma_recorrencia)                                                                                                             | **GET** /v3/pix/transactions/recurrings/{id}/items                  | Listar itens de uma recorrência                                                 |
| _PixRecorrenteApi_                 | [**listar_recorrencias**](PixRecorrenteApi.md#listar_recorrencias)                                                                                                                                     | **GET** /v3/pix/transactions/recurrings                             | Listar recorrências                                                             |
| _PixRecorrenteApi_                 | [**recuperar_uma_unica_recorrencia**](PixRecorrenteApi.md#recuperar_uma_unica_recorrencia)                                                                                                             | **GET** /v3/pix/transactions/recurrings/{id}                        | Recuperar uma única recorrência                                                 |
| _RecargasDeCelularApi_             | [**buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga**](RecargasDeCelularApi.md#buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga)                 | **GET** /v3/mobilePhoneRecharges/{phoneNumber}/provider             | Buscar qual provedor o número pertence e os valores disponíveis para recarga    |
| _RecargasDeCelularApi_             | [**cancelar_uma_recarga_de_celular**](RecargasDeCelularApi.md#cancelar_uma_recarga_de_celular)                                                                                                         | **POST** /v3/mobilePhoneRecharges/{id}/cancel                       | Cancelar uma recarga de celular                                                 |
| _RecargasDeCelularApi_             | [**listar_recargas_de_celular**](RecargasDeCelularApi.md#listar_recargas_de_celular)                                                                                                                   | **GET** /v3/mobilePhoneRecharges                                    | Listar recargas de celular                                                      |
| _RecargasDeCelularApi_             | [**recuperar_uma_unica_recarga_de_celular**](RecargasDeCelularApi.md#recuperar_uma_unica_recarga_de_celular)                                                                                           | **GET** /v3/mobilePhoneRecharges/{id}                               | Recuperar uma única recarga de celular                                          |
| _RecargasDeCelularApi_             | [**solicitar_recarga**](RecargasDeCelularApi.md#solicitar_recarga)                                                                                                                                     | **POST** /v3/mobilePhoneRecharges                                   | Solicitar recarga                                                               |
| _SplitsApi_                        | [**listar_splits_pagos**](SplitsApi.md#listar_splits_pagos)                                                                                                                                            | **GET** /v3/payments/splits/paid                                    | Listar splits pagos                                                             |
| _SplitsApi_                        | [**listar_splits_recebidos**](SplitsApi.md#listar_splits_recebidos)                                                                                                                                    | **GET** /v3/payments/splits/received                                | Listar splits recebidos                                                         |
| _SplitsApi_                        | [**recuperar_um_unico_split_pago**](SplitsApi.md#recuperar_um_unico_split_pago)                                                                                                                        | **GET** /v3/payments/splits/paid/{id}                               | Recuperar um único split pago                                                   |
| _SplitsApi_                        | [**recuperar_um_unico_split_recebido**](SplitsApi.md#recuperar_um_unico_split_recebido)                                                                                                                | **GET** /v3/payments/splits/received/{id}                           | Recuperar um único split recebido                                               |
| _SubcontasAsaasApi_                | [**atualizar_chave_de_api_de_uma_subconta**](SubcontasAsaasApi.md#atualizar_chave_de_api_de_uma_subconta)                                                                                              | **PUT** /v3/accounts/{id}/accessTokens/{accessTokenId}              | Atualizar chave de API de uma subconta                                          |
| _SubcontasAsaasApi_                | [**criar_chave_de_api_para_uma_subconta**](SubcontasAsaasApi.md#criar_chave_de_api_para_uma_subconta)                                                                                                  | **POST** /v3/accounts/{id}/accessTokens                             | Criar chave de API para uma subconta                                            |
| _SubcontasAsaasApi_                | [**criar_subconta**](SubcontasAsaasApi.md#criar_subconta)                                                                                                                                              | **POST** /v3/accounts                                               | Criar subconta                                                                  |
| _SubcontasAsaasApi_                | [**excluir_chave_de_api_de_uma_subconta**](SubcontasAsaasApi.md#excluir_chave_de_api_de_uma_subconta)                                                                                                  | **DELETE** /v3/accounts/{id}/accessTokens/{accessTokenId}           | Excluir chave de API de uma subconta                                            |
| _SubcontasAsaasApi_                | [**listar_chaves_de_api_de_uma_subconta**](SubcontasAsaasApi.md#listar_chaves_de_api_de_uma_subconta)                                                                                                  | **GET** /v3/accounts/{id}/accessTokens                              | Listar chaves de API de uma subconta                                            |
| _SubcontasAsaasApi_                | [**listar_subcontas**](SubcontasAsaasApi.md#listar_subcontas)                                                                                                                                          | **GET** /v3/accounts                                                | Listar subcontas                                                                |
| _SubcontasAsaasApi_                | [**recuperar_uma_unica_subconta**](SubcontasAsaasApi.md#recuperar_uma_unica_subconta)                                                                                                                  | **GET** /v3/accounts/{id}                                           | Recuperar uma única subconta                                                    |
| _TransaesPixApi_                   | [**cancelar_uma_transacao_agendada**](TransaesPixApi.md#cancelar_uma_transacao_agendada)                                                                                                               | **POST** /v3/pix/transactions/{id}/cancel                           | Cancelar uma transação agendada                                                 |
| _TransaesPixApi_                   | [**decodificar_um_qrcode_para_pagamento**](TransaesPixApi.md#decodificar_um_qrcode_para_pagamento)                                                                                                     | **POST** /v3/pix/qrCodes/decode                                     | Decodificar um QRCode para pagamento                                            |
| _TransaesPixApi_                   | [**listar_transacoes**](TransaesPixApi.md#listar_transacoes)                                                                                                                                           | **GET** /v3/pix/transactions                                        | Listar transações                                                               |
| _TransaesPixApi_                   | [**pagar_um_qrcode**](TransaesPixApi.md#pagar_um_qrcode)                                                                                                                                               | **POST** /v3/pix/qrCodes/pay                                        | Pagar um QRCode                                                                 |
| _TransaesPixApi_                   | [**recuperar_uma_unica_transacao**](TransaesPixApi.md#recuperar_uma_unica_transacao)                                                                                                                   | **GET** /v3/pix/transactions/{id}                                   | Recuperar uma única transação                                                   |
| _TransfernciasApi_                 | [**cancelar_uma_transferncia**](TransfernciasApi.md#cancelar_uma_transferncia)                                                                                                                         | **DELETE** /v3/transfers/{id}/cancel                                | Cancelar uma transferência                                                      |
| _TransfernciasApi_                 | [**listar_transferencias**](TransfernciasApi.md#listar_transferencias)                                                                                                                                 | **GET** /v3/transfers                                               | Listar transferências                                                           |
| _TransfernciasApi_                 | [**recuperar_uma_unica_transferencia**](TransfernciasApi.md#recuperar_uma_unica_transferencia)                                                                                                         | **GET** /v3/transfers/{id}                                          | Recuperar uma única transferência                                               |
| _TransfernciasApi_                 | [**transferir_para_conta_asaas**](TransfernciasApi.md#transferir_para_conta_asaas)                                                                                                                     | **POST** /v3/transfers/                                             | Transferir para conta Asaas                                                     |
| _TransfernciasApi_                 | [**transferir_para_conta_de_outra_instituicao_ou_chave_pix**](TransfernciasApi.md#transferir_para_conta_de_outra_instituicao_ou_chave_pix)                                                             | **POST** /v3/transfers                                              | Transferir para conta de outra Instituição ou chave Pix                         |

## Documentation For Models

- [AccountDocumentDeleteResponseDTO](AccountDocumentDeleteResponseDTO.md)
- [AccountDocumentGetResponseAccountDocumentStatus](AccountDocumentGetResponseAccountDocumentStatus.md)
- [AccountDocumentGetResponseDTO](AccountDocumentGetResponseDTO.md)
- [AccountDocumentGroupResponseAccountDocumentStatus](AccountDocumentGroupResponseAccountDocumentStatus.md)
- [AccountDocumentGroupResponseAccountDocumentType](AccountDocumentGroupResponseAccountDocumentType.md)
- [AccountDocumentGroupResponseDTO](AccountDocumentGroupResponseDTO.md)
- [AccountDocumentResponsibleResponseAccountDocumentResponsibleType](AccountDocumentResponsibleResponseAccountDocumentResponsibleType.md)
- [AccountDocumentResponsibleResponseDTO](AccountDocumentResponsibleResponseDTO.md)
- [AccountDocumentSaveRequestAccountDocumentType](AccountDocumentSaveRequestAccountDocumentType.md)
- [AccountDocumentShowResponseDTO](AccountDocumentShowResponseDTO.md)
- [AccountGetResponseCompanyType](AccountGetResponseCompanyType.md)
- [AccountGetResponseDTO](AccountGetResponseDTO.md)
- [AccountGetResponsePersonType](AccountGetResponsePersonType.md)
- [AccountInfoCityDTO](AccountInfoCityDTO.md)
- [AccountInfoCityState](AccountInfoCityState.md)
- [AccountInfoCommercialInfoExpirationResponseDTO](AccountInfoCommercialInfoExpirationResponseDTO.md)
- [AccountInfoGetResponseCompanyType](AccountInfoGetResponseCompanyType.md)
- [AccountInfoGetResponseDTO](AccountInfoGetResponseDTO.md)
- [AccountInfoGetResponsePersonType](AccountInfoGetResponsePersonType.md)
- [AccountInfoGetResponseStatus](AccountInfoGetResponseStatus.md)
- [AccountInfoSaveRequestCompanyType](AccountInfoSaveRequestCompanyType.md)
- [AccountInfoSaveRequestDTO](AccountInfoSaveRequestDTO.md)
- [AccountInfoSaveRequestPersonType](AccountInfoSaveRequestPersonType.md)
- [AccountListResponseDTO](AccountListResponseDTO.md)
- [AccountNumberDTO](AccountNumberDTO.md)
- [AccountPaymentEscrowConfigDTO](AccountPaymentEscrowConfigDTO.md)
- [AccountSaveOrUpdatePaymentEscrowConfigRequestDTO](AccountSaveOrUpdatePaymentEscrowConfigRequestDTO.md)
- [AccountSaveRequestCompanyType](AccountSaveRequestCompanyType.md)
- [AccountSaveRequestDTO](AccountSaveRequestDTO.md)
- [AccountSaveResponseCompanyType](AccountSaveResponseCompanyType.md)
- [AccountSaveResponseDTO](AccountSaveResponseDTO.md)
- [AccountSaveResponsePersonType](AccountSaveResponsePersonType.md)
- [AnticipationConfigurationGetResponseDTO](AnticipationConfigurationGetResponseDTO.md)
- [AnticipationConfigurationUpdateRequestDTO](AnticipationConfigurationUpdateRequestDTO.md)
- [AnticipationGetResponseAnticipationStatus](AnticipationGetResponseAnticipationStatus.md)
- [AnticipationGetResponseDTO](AnticipationGetResponseDTO.md)
- [AnticipationLimitsInfoResponseDTO](AnticipationLimitsInfoResponseDTO.md)
- [AnticipationLimitsResponseDTO](AnticipationLimitsResponseDTO.md)
- [AnticipationListRequestAnticipationStatus](AnticipationListRequestAnticipationStatus.md)
- [AnticipationListResponseDTO](AnticipationListResponseDTO.md)
- [AnticipationSimulateRequestDTO](AnticipationSimulateRequestDTO.md)
- [AnticipationSimulateResponseDTO](AnticipationSimulateResponseDTO.md)
- [BankSlipBillingInfoResponseDTO](BankSlipBillingInfoResponseDTO.md)
- [BillGetResponseBillStatus](BillGetResponseBillStatus.md)
- [BillGetResponseDTO](BillGetResponseDTO.md)
- [BillListResponseDTO](BillListResponseDTO.md)
- [BillSaveRequestDTO](BillSaveRequestDTO.md)
- [BillSimulateBankSlipInfoResponseDTO](BillSimulateBankSlipInfoResponseDTO.md)
- [BillSimulateRequestDTO](BillSimulateRequestDTO.md)
- [BillSimulateResponseDTO](BillSimulateResponseDTO.md)
- [ChargebackCreditCardResponseCreditCardBrand](ChargebackCreditCardResponseCreditCardBrand.md)
- [ChargebackCreditCardResponseDTO](ChargebackCreditCardResponseDTO.md)
- [ChargebackListRequestChargebackStatus](ChargebackListRequestChargebackStatus.md)
- [ChargebackListRequestCreditCardBrand](ChargebackListRequestCreditCardBrand.md)
- [ChargebackListResponseDTO](ChargebackListResponseDTO.md)
- [ChargebackSaveDisputeResponseChargebackDisputeStatus](ChargebackSaveDisputeResponseChargebackDisputeStatus.md)
- [ChargebackSaveDisputeResponseDTO](ChargebackSaveDisputeResponseDTO.md)
- [CheckoutSessionCallbackDTO](CheckoutSessionCallbackDTO.md)
- [CheckoutSessionCustomerDataDTO](CheckoutSessionCustomerDataDTO.md)
- [CheckoutSessionInstallmentDTO](CheckoutSessionInstallmentDTO.md)
- [CheckoutSessionItemsDTO](CheckoutSessionItemsDTO.md)
- [CheckoutSessionResponseBillingType](CheckoutSessionResponseBillingType.md)
- [CheckoutSessionResponseChargeType](CheckoutSessionResponseChargeType.md)
- [CheckoutSessionResponseDTO](CheckoutSessionResponseDTO.md)
- [CheckoutSessionSaveRequestBillingType](CheckoutSessionSaveRequestBillingType.md)
- [CheckoutSessionSaveRequestChargeType](CheckoutSessionSaveRequestChargeType.md)
- [CheckoutSessionSaveRequestDTO](CheckoutSessionSaveRequestDTO.md)
- [CheckoutSessionSplitDTO](CheckoutSessionSplitDTO.md)
- [CheckoutSessionSubscriptionCycle](CheckoutSessionSubscriptionCycle.md)
- [CheckoutSessionSubscriptionDTO](CheckoutSessionSubscriptionDTO.md)
- [CreditBureauReportGetResponseDTO](CreditBureauReportGetResponseDTO.md)
- [CreditBureauReportListResponseDTO](CreditBureauReportListResponseDTO.md)
- [CreditBureauReportSaveRequestDTO](CreditBureauReportSaveRequestDTO.md)
- [CreditCardHolderInfoRequestDTO](CreditCardHolderInfoRequestDTO.md)
- [CreditCardPreAuthorizationConfigRequestDTO](CreditCardPreAuthorizationConfigRequestDTO.md)
- [CreditCardPreAuthorizationConfigResponseDTO](CreditCardPreAuthorizationConfigResponseDTO.md)
- [CreditCardRequestDTO](CreditCardRequestDTO.md)
- [CreditCardTokenizeRequestDTO](CreditCardTokenizeRequestDTO.md)
- [CreditCardTokenizeResponseCreditCardBrand](CreditCardTokenizeResponseCreditCardBrand.md)
- [CreditCardTokenizeResponseDTO](CreditCardTokenizeResponseDTO.md)
- [CustomerApiAccessTokenBaseResponseDTO](CustomerApiAccessTokenBaseResponseDTO.md)
- [CustomerApiAccessTokenListResponseDTO](CustomerApiAccessTokenListResponseDTO.md)
- [CustomerApiAccessTokenSaveRequestDTO](CustomerApiAccessTokenSaveRequestDTO.md)
- [CustomerApiAccessTokenSaveResponseDTO](CustomerApiAccessTokenSaveResponseDTO.md)
- [CustomerApiAccessTokenUpdateRequestDTO](CustomerApiAccessTokenUpdateRequestDTO.md)
- [CustomerDeleteResponseDTO](CustomerDeleteResponseDTO.md)
- [CustomerGetResponseDTO](CustomerGetResponseDTO.md)
- [CustomerGetResponsePersonType](CustomerGetResponsePersonType.md)
- [CustomerListResponseDTO](CustomerListResponseDTO.md)
- [CustomerSaveRequestDTO](CustomerSaveRequestDTO.md)
- [CustomerUpdateRequestDTO](CustomerUpdateRequestDTO.md)
- [ErrorResponseDTO](ErrorResponseDTO.md)
- [ErrorResponseItemDTO](ErrorResponseItemDTO.md)
- [FinanceBalanceResponseDTO](FinanceBalanceResponseDTO.md)
- [FinanceGetPaymentStatisticsRequestBillingType](FinanceGetPaymentStatisticsRequestBillingType.md)
- [FinanceGetPaymentStatisticsRequestPaymentStatus](FinanceGetPaymentStatisticsRequestPaymentStatus.md)
- [FinanceGetPaymentStatisticsResponseDTO](FinanceGetPaymentStatisticsResponseDTO.md)
- [FinanceGetSplitStatisticsResponseDTO](FinanceGetSplitStatisticsResponseDTO.md)
- [FinancialTransactionGetResponseDTO](FinancialTransactionGetResponseDTO.md)
- [FinancialTransactionGetResponseFinancialTransactionType](FinancialTransactionGetResponseFinancialTransactionType.md)
- [FinancialTransactionListResponseDTO](FinancialTransactionListResponseDTO.md)
- [FiscalInfoFederalServiceCodeListResponseDTO](FiscalInfoFederalServiceCodeListResponseDTO.md)
- [FiscalInfoFederalServiceCodeResponseDTO](FiscalInfoFederalServiceCodeResponseDTO.md)
- [FiscalInfoGetResponseDTO](FiscalInfoGetResponseDTO.md)
- [FiscalInfoListInvoiceNbsCodesResponseDTO](FiscalInfoListInvoiceNbsCodesResponseDTO.md)
- [FiscalInfoListInvoiceNbsCodesResponseDataDTO](FiscalInfoListInvoiceNbsCodesResponseDataDTO.md)
- [FiscalInfoListMunicipalServicesResponseDTO](FiscalInfoListMunicipalServicesResponseDTO.md)
- [FiscalInfoListMunicipalServicesResponseDataDTO](FiscalInfoListMunicipalServicesResponseDataDTO.md)
- [FiscalInfoMunicipalOptionsGetResponseDTO](FiscalInfoMunicipalOptionsGetResponseDTO.md)
- [FiscalInfoMunicipalOptionsGetResponseEnotasTipoAutenticacao](FiscalInfoMunicipalOptionsGetResponseEnotasTipoAutenticacao.md)
- [FiscalInfoMunicipalOptionsNationalPortalTaxCalculationRegimeDTO](FiscalInfoMunicipalOptionsNationalPortalTaxCalculationRegimeDTO.md)
- [FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO](FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO.md)
- [FiscalInfoOperationIndicatorCodeListResponseDTO](FiscalInfoOperationIndicatorCodeListResponseDTO.md)
- [FiscalInfoOperationIndicatorCodeResponseDTO](FiscalInfoOperationIndicatorCodeResponseDTO.md)
- [FiscalInfoTaxClassificationCodeListResponseDTO](FiscalInfoTaxClassificationCodeListResponseDTO.md)
- [FiscalInfoTaxClassificationCodeResponseDTO](FiscalInfoTaxClassificationCodeResponseDTO.md)
- [FiscalInfoTaxSituationCodeListResponseDTO](FiscalInfoTaxSituationCodeListResponseDTO.md)
- [FiscalInfoTaxSituationCodeResponseDTO](FiscalInfoTaxSituationCodeResponseDTO.md)
- [FiscalInfoUpdateUseNationalPortalRequestDTO](FiscalInfoUpdateUseNationalPortalRequestDTO.md)
- [FiscalInfoUpdateUseNationalPortalResponseDTO](FiscalInfoUpdateUseNationalPortalResponseDTO.md)
- [InstallmentDeletePaymentsResponseDTO](InstallmentDeletePaymentsResponseDTO.md)
- [InstallmentDeleteResponseDTO](InstallmentDeleteResponseDTO.md)
- [InstallmentGetResponseBillingType](InstallmentGetResponseBillingType.md)
- [InstallmentGetResponseDTO](InstallmentGetResponseDTO.md)
- [InstallmentListPaymentsRequestPaymentStatus](InstallmentListPaymentsRequestPaymentStatus.md)
- [InstallmentListResponseDTO](InstallmentListResponseDTO.md)
- [InstallmentPaymentDeletedDTO](InstallmentPaymentDeletedDTO.md)
- [InstallmentRefundRequestDTO](InstallmentRefundRequestDTO.md)
- [InstallmentRefundResponseDTO](InstallmentRefundResponseDTO.md)
- [InstallmentRefundResponsePaymentRefundStatus](InstallmentRefundResponsePaymentRefundStatus.md)
- [InstallmentSaveRequestBillingType](InstallmentSaveRequestBillingType.md)
- [InstallmentSaveRequestDTO](InstallmentSaveRequestDTO.md)
- [InstallmentSaveWithCreditCardRequestBillingType](InstallmentSaveWithCreditCardRequestBillingType.md)
- [InstallmentSaveWithCreditCardRequestDTO](InstallmentSaveWithCreditCardRequestDTO.md)
- [InstallmentSplitGetResponseDTO](InstallmentSplitGetResponseDTO.md)
- [InstallmentSplitGetResponsePaymentSplitCancellationReason](InstallmentSplitGetResponsePaymentSplitCancellationReason.md)
- [InstallmentSplitGetResponsePaymentSplitStatus](InstallmentSplitGetResponsePaymentSplitStatus.md)
- [InstallmentSplitRequestDTO](InstallmentSplitRequestDTO.md)
- [InstallmentUpdateSplitRequestDTO](InstallmentUpdateSplitRequestDTO.md)
- [InstallmentUpdateSplitResponseDTO](InstallmentUpdateSplitResponseDTO.md)
- [InvoiceCancelRequestDTO](InvoiceCancelRequestDTO.md)
- [InvoiceGetResponseDTO](InvoiceGetResponseDTO.md)
- [InvoiceGetResponseInvoiceStatus](InvoiceGetResponseInvoiceStatus.md)
- [InvoiceListRequestInvoiceStatus](InvoiceListRequestInvoiceStatus.md)
- [InvoiceListResponseDTO](InvoiceListResponseDTO.md)
- [InvoiceSaveRequestDTO](InvoiceSaveRequestDTO.md)
- [InvoiceTaxesDTO](InvoiceTaxesDTO.md)
- [InvoiceTaxesRequestDTO](InvoiceTaxesRequestDTO.md)
- [InvoiceTaxesResponseDTO](InvoiceTaxesResponseDTO.md)
- [InvoiceUpdateRequestDTO](InvoiceUpdateRequestDTO.md)
- [MobilePhoneRechargeFindProviderResponseDTO](MobilePhoneRechargeFindProviderResponseDTO.md)
- [MobilePhoneRechargeFindProviderResponseValuesDTO](MobilePhoneRechargeFindProviderResponseValuesDTO.md)
- [MobilePhoneRechargeGetResponseDTO](MobilePhoneRechargeGetResponseDTO.md)
- [MobilePhoneRechargeGetResponseMobilePhoneRechargeStatus](MobilePhoneRechargeGetResponseMobilePhoneRechargeStatus.md)
- [MobilePhoneRechargeListResponseDTO](MobilePhoneRechargeListResponseDTO.md)
- [MobilePhoneRechargeSaveRequestDTO](MobilePhoneRechargeSaveRequestDTO.md)
- [MyAccountDisableAccountResponseDTO](MyAccountDisableAccountResponseDTO.md)
- [MyAccountGetAccountFeesAnticipationBankSlipDTO](MyAccountGetAccountFeesAnticipationBankSlipDTO.md)
- [MyAccountGetAccountFeesAnticipationCreditCardDTO](MyAccountGetAccountFeesAnticipationCreditCardDTO.md)
- [MyAccountGetAccountFeesAnticipationDTO](MyAccountGetAccountFeesAnticipationDTO.md)
- [MyAccountGetAccountFeesCreditBureauReportDTO](MyAccountGetAccountFeesCreditBureauReportDTO.md)
- [MyAccountGetAccountFeesInvoiceDTO](MyAccountGetAccountFeesInvoiceDTO.md)
- [MyAccountGetAccountFeesNotificationDTO](MyAccountGetAccountFeesNotificationDTO.md)
- [MyAccountGetAccountFeesPaymentBankSlipDTO](MyAccountGetAccountFeesPaymentBankSlipDTO.md)
- [MyAccountGetAccountFeesPaymentCreditCardDTO](MyAccountGetAccountFeesPaymentCreditCardDTO.md)
- [MyAccountGetAccountFeesPaymentDTO](MyAccountGetAccountFeesPaymentDTO.md)
- [MyAccountGetAccountFeesPaymentDebitCardDTO](MyAccountGetAccountFeesPaymentDebitCardDTO.md)
- [MyAccountGetAccountFeesPaymentDunningDTO](MyAccountGetAccountFeesPaymentDunningDTO.md)
- [MyAccountGetAccountFeesPaymentPixDTO](MyAccountGetAccountFeesPaymentPixDTO.md)
- [MyAccountGetAccountFeesResponseDTO](MyAccountGetAccountFeesResponseDTO.md)
- [MyAccountGetAccountFeesTransferDTO](MyAccountGetAccountFeesTransferDTO.md)
- [MyAccountGetAccountFeesTransferPixDTO](MyAccountGetAccountFeesTransferPixDTO.md)
- [MyAccountGetAccountFeesTransferTedDTO](MyAccountGetAccountFeesTransferTedDTO.md)
- [MyAccountGetAccountNumberResponseDTO](MyAccountGetAccountNumberResponseDTO.md)
- [MyAccountGetStatusResponseDTO](MyAccountGetStatusResponseDTO.md)
- [MyAccountGetStatusResponseStatus](MyAccountGetStatusResponseStatus.md)
- [NotificationBatchUpdateItemRequestDTO](NotificationBatchUpdateItemRequestDTO.md)
- [NotificationBatchUpdateRequestDTO](NotificationBatchUpdateRequestDTO.md)
- [NotificationBatchUpdateResponseDTO](NotificationBatchUpdateResponseDTO.md)
- [NotificationGetResponseDTO](NotificationGetResponseDTO.md)
- [NotificationGetResponseNotificationEvent](NotificationGetResponseNotificationEvent.md)
- [NotificationListResponseDTO](NotificationListResponseDTO.md)
- [NotificationUpdateRequestDTO](NotificationUpdateRequestDTO.md)
- [PaymentBankSlipRefundResponseDTO](PaymentBankSlipRefundResponseDTO.md)
- [PaymentBillingInfoResponseDTO](PaymentBillingInfoResponseDTO.md)
- [PaymentCallbackRequestDTO](PaymentCallbackRequestDTO.md)
- [PaymentChargebackResponseChargebackDisputeStatus](PaymentChargebackResponseChargebackDisputeStatus.md)
- [PaymentChargebackResponseChargebackReason](PaymentChargebackResponseChargebackReason.md)
- [PaymentChargebackResponseChargebackStatus](PaymentChargebackResponseChargebackStatus.md)
- [PaymentChargebackResponseDTO](PaymentChargebackResponseDTO.md)
- [PaymentCheckoutConfigGetResponseDTO](PaymentCheckoutConfigGetResponseDTO.md)
- [PaymentCheckoutConfigGetResponseInvoiceConfigStatus](PaymentCheckoutConfigGetResponseInvoiceConfigStatus.md)
- [PaymentDeleteResponseDTO](PaymentDeleteResponseDTO.md)
- [PaymentDiscountDTO](PaymentDiscountDTO.md)
- [PaymentDiscountDiscountType](PaymentDiscountDiscountType.md)
- [PaymentDocumentDeleteResponseDTO](PaymentDocumentDeleteResponseDTO.md)
- [PaymentDocumentFileResponseDTO](PaymentDocumentFileResponseDTO.md)
- [PaymentDocumentGetResponseDTO](PaymentDocumentGetResponseDTO.md)
- [PaymentDocumentGetResponsePaymentDocumentType](PaymentDocumentGetResponsePaymentDocumentType.md)
- [PaymentDocumentListResponseDTO](PaymentDocumentListResponseDTO.md)
- [PaymentDocumentSaveRequestPaymentDocumentType](PaymentDocumentSaveRequestPaymentDocumentType.md)
- [PaymentDocumentUpdateRequestDTO](PaymentDocumentUpdateRequestDTO.md)
- [PaymentDocumentUpdateRequestPaymentDocumentType](PaymentDocumentUpdateRequestPaymentDocumentType.md)
- [PaymentDunningCancelResponseDTO](PaymentDunningCancelResponseDTO.md)
- [PaymentDunningCancelResponsePaymentDunningStatus](PaymentDunningCancelResponsePaymentDunningStatus.md)
- [PaymentDunningCancelResponsePaymentDunningType](PaymentDunningCancelResponsePaymentDunningType.md)
- [PaymentDunningListHistoryResponseDTO](PaymentDunningListHistoryResponseDTO.md)
- [PaymentDunningListHistoryResponseDataDTO](PaymentDunningListHistoryResponseDataDTO.md)
- [PaymentDunningListHistoryResponseDataPaymentDunningHistoryStatus](PaymentDunningListHistoryResponseDataPaymentDunningHistoryStatus.md)
- [PaymentDunningListPartialPaymentsResponseDTO](PaymentDunningListPartialPaymentsResponseDTO.md)
- [PaymentDunningListPartialPaymentsResponseDataDTO](PaymentDunningListPartialPaymentsResponseDataDTO.md)
- [PaymentDunningListRequestPaymentDunningStatus](PaymentDunningListRequestPaymentDunningStatus.md)
- [PaymentDunningListRequestPaymentDunningType](PaymentDunningListRequestPaymentDunningType.md)
- [PaymentDunningListResponseDTO](PaymentDunningListResponseDTO.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDTO](PaymentDunningPaymentsAvailableForDunningResponseDTO.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataBillingType](PaymentDunningPaymentsAvailableForDunningResponseDataBillingType.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataDTO](PaymentDunningPaymentsAvailableForDunningResponseDataDTO.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataPaymentStatus](PaymentDunningPaymentsAvailableForDunningResponseDataPaymentStatus.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO](PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemPaymentDunningType](PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemPaymentDunningType.md)
- [PaymentDunningSaveDocumentsResponseDTO](PaymentDunningSaveDocumentsResponseDTO.md)
- [PaymentDunningSaveDocumentsResponsePaymentDunningStatus](PaymentDunningSaveDocumentsResponsePaymentDunningStatus.md)
- [PaymentDunningSaveDocumentsResponsePaymentDunningType](PaymentDunningSaveDocumentsResponsePaymentDunningType.md)
- [PaymentDunningSaveRequestPaymentDunningType](PaymentDunningSaveRequestPaymentDunningType.md)
- [PaymentDunningShowResponseDTO](PaymentDunningShowResponseDTO.md)
- [PaymentDunningShowResponsePaymentDunningStatus](PaymentDunningShowResponsePaymentDunningStatus.md)
- [PaymentDunningShowResponsePaymentDunningType](PaymentDunningShowResponsePaymentDunningType.md)
- [PaymentDunningSimulateResponseDTO](PaymentDunningSimulateResponseDTO.md)
- [PaymentDunningSimulateResponseTypeSimulationItemDTO](PaymentDunningSimulateResponseTypeSimulationItemDTO.md)
- [PaymentDunningSimulateResponseTypeSimulationItemPaymentDunningType](PaymentDunningSimulateResponseTypeSimulationItemPaymentDunningType.md)
- [PaymentEscrowGetResponseDTO](PaymentEscrowGetResponseDTO.md)
- [PaymentEscrowGetResponsePaymentEscrowFinishReason](PaymentEscrowGetResponsePaymentEscrowFinishReason.md)
- [PaymentEscrowGetResponsePaymentEscrowStatus](PaymentEscrowGetResponsePaymentEscrowStatus.md)
- [PaymentFineRequestDTO](PaymentFineRequestDTO.md)
- [PaymentFineRequestFineType](PaymentFineRequestFineType.md)
- [PaymentFineResponseDTO](PaymentFineResponseDTO.md)
- [PaymentGetResponseBillingType](PaymentGetResponseBillingType.md)
- [PaymentGetResponseDTO](PaymentGetResponseDTO.md)
- [PaymentGetResponsePaymentStatus](PaymentGetResponsePaymentStatus.md)
- [PaymentIdentificationFieldResponseDTO](PaymentIdentificationFieldResponseDTO.md)
- [PaymentInterestRequestDTO](PaymentInterestRequestDTO.md)
- [PaymentInterestResponseDTO](PaymentInterestResponseDTO.md)
- [PaymentLeanGetResponseBillingType](PaymentLeanGetResponseBillingType.md)
- [PaymentLeanGetResponseDTO](PaymentLeanGetResponseDTO.md)
- [PaymentLeanGetResponsePaymentStatus](PaymentLeanGetResponsePaymentStatus.md)
- [PaymentLeanListResponseDTO](PaymentLeanListResponseDTO.md)
- [PaymentLeanSaveWithCreditCardResponseBillingType](PaymentLeanSaveWithCreditCardResponseBillingType.md)
- [PaymentLeanSaveWithCreditCardResponseDTO](PaymentLeanSaveWithCreditCardResponseDTO.md)
- [PaymentLeanSaveWithCreditCardResponsePaymentStatus](PaymentLeanSaveWithCreditCardResponsePaymentStatus.md)
- [PaymentLimitsResponseCreationDTO](PaymentLimitsResponseCreationDTO.md)
- [PaymentLimitsResponseCreationDailyDTO](PaymentLimitsResponseCreationDailyDTO.md)
- [PaymentLimitsResponseDTO](PaymentLimitsResponseDTO.md)
- [PaymentLinkDeleteResponseDTO](PaymentLinkDeleteResponseDTO.md)
- [PaymentLinkFileDeleteResponseDTO](PaymentLinkFileDeleteResponseDTO.md)
- [PaymentLinkFileGetResponseDTO](PaymentLinkFileGetResponseDTO.md)
- [PaymentLinkFileImageResponseDTO](PaymentLinkFileImageResponseDTO.md)
- [PaymentLinkFileListResponseDTO](PaymentLinkFileListResponseDTO.md)
- [PaymentLinkGetResponseBillingType](PaymentLinkGetResponseBillingType.md)
- [PaymentLinkGetResponseChargeType](PaymentLinkGetResponseChargeType.md)
- [PaymentLinkGetResponseCycle](PaymentLinkGetResponseCycle.md)
- [PaymentLinkGetResponseDTO](PaymentLinkGetResponseDTO.md)
- [PaymentLinkListResponseDTO](PaymentLinkListResponseDTO.md)
- [PaymentLinkSaveRequestBillingType](PaymentLinkSaveRequestBillingType.md)
- [PaymentLinkSaveRequestChargeType](PaymentLinkSaveRequestChargeType.md)
- [PaymentLinkSaveRequestCycle](PaymentLinkSaveRequestCycle.md)
- [PaymentLinkSaveRequestDTO](PaymentLinkSaveRequestDTO.md)
- [PaymentLinkUpdateRequestBillingType](PaymentLinkUpdateRequestBillingType.md)
- [PaymentLinkUpdateRequestChargeType](PaymentLinkUpdateRequestChargeType.md)
- [PaymentLinkUpdateRequestCycle](PaymentLinkUpdateRequestCycle.md)
- [PaymentLinkUpdateRequestDTO](PaymentLinkUpdateRequestDTO.md)
- [PaymentListRequestBillingType](PaymentListRequestBillingType.md)
- [PaymentListRequestInvoiceStatus](PaymentListRequestInvoiceStatus.md)
- [PaymentListRequestPaymentStatus](PaymentListRequestPaymentStatus.md)
- [PaymentListResponseDTO](PaymentListResponseDTO.md)
- [PaymentPayWithCreditCardRequestDTO](PaymentPayWithCreditCardRequestDTO.md)
- [PaymentPixQrCodeResponseDTO](PaymentPixQrCodeResponseDTO.md)
- [PaymentReceiveInCashRequestDTO](PaymentReceiveInCashRequestDTO.md)
- [PaymentRefundGetResponseDTO](PaymentRefundGetResponseDTO.md)
- [PaymentRefundGetResponsePaymentRefundStatus](PaymentRefundGetResponsePaymentRefundStatus.md)
- [PaymentRefundListResponseDTO](PaymentRefundListResponseDTO.md)
- [PaymentRefundRequestDTO](PaymentRefundRequestDTO.md)
- [PaymentRefundSplitRequestDTO](PaymentRefundSplitRequestDTO.md)
- [PaymentRefundedSplitResponseDTO](PaymentRefundedSplitResponseDTO.md)
- [PaymentSaveRequestBillingType](PaymentSaveRequestBillingType.md)
- [PaymentSaveRequestDTO](PaymentSaveRequestDTO.md)
- [PaymentSaveWithCreditCardCreditCardCreditCardBrand](PaymentSaveWithCreditCardCreditCardCreditCardBrand.md)
- [PaymentSaveWithCreditCardCreditCardDTO](PaymentSaveWithCreditCardCreditCardDTO.md)
- [PaymentSaveWithCreditCardRequestBillingType](PaymentSaveWithCreditCardRequestBillingType.md)
- [PaymentSaveWithCreditCardRequestDTO](PaymentSaveWithCreditCardRequestDTO.md)
- [PaymentSimulateBankSlipResponseDTO](PaymentSimulateBankSlipResponseDTO.md)
- [PaymentSimulateCreditCardResponseDTO](PaymentSimulateCreditCardResponseDTO.md)
- [PaymentSimulateInstallmentResponseDTO](PaymentSimulateInstallmentResponseDTO.md)
- [PaymentSimulatePixResponseDTO](PaymentSimulatePixResponseDTO.md)
- [PaymentSimulateRequestBillingType](PaymentSimulateRequestBillingType.md)
- [PaymentSimulateRequestDTO](PaymentSimulateRequestDTO.md)
- [PaymentSimulateResponseDTO](PaymentSimulateResponseDTO.md)
- [PaymentSplitGetFullResponseDTO](PaymentSplitGetFullResponseDTO.md)
- [PaymentSplitGetFullResponsePaymentSplitCancellationReason](PaymentSplitGetFullResponsePaymentSplitCancellationReason.md)
- [PaymentSplitGetFullResponsePaymentSplitStatus](PaymentSplitGetFullResponsePaymentSplitStatus.md)
- [PaymentSplitGetResponseDTO](PaymentSplitGetResponseDTO.md)
- [PaymentSplitGetResponsePaymentSplitCancellationReason](PaymentSplitGetResponsePaymentSplitCancellationReason.md)
- [PaymentSplitGetResponsePaymentSplitStatus](PaymentSplitGetResponsePaymentSplitStatus.md)
- [PaymentSplitListPaidRequestPaymentSplitStatus](PaymentSplitListPaidRequestPaymentSplitStatus.md)
- [PaymentSplitListReceivedRequestPaymentSplitStatus](PaymentSplitListReceivedRequestPaymentSplitStatus.md)
- [PaymentSplitListResponseDTO](PaymentSplitListResponseDTO.md)
- [PaymentSplitPaymentInfoResponseDTO](PaymentSplitPaymentInfoResponseDTO.md)
- [PaymentSplitRequestDTO](PaymentSplitRequestDTO.md)
- [PaymentStatusResponseDTO](PaymentStatusResponseDTO.md)
- [PaymentStatusResponsePaymentStatus](PaymentStatusResponsePaymentStatus.md)
- [PaymentUpdateRequestBillingType](PaymentUpdateRequestBillingType.md)
- [PaymentUpdateRequestDTO](PaymentUpdateRequestDTO.md)
- [PaymentViewingInfoResponseDTO](PaymentViewingInfoResponseDTO.md)
- [PixAddressKeyGetResponseDTO](PixAddressKeyGetResponseDTO.md)
- [PixAddressKeyGetResponsePixAddressKeyStatus](PixAddressKeyGetResponsePixAddressKeyStatus.md)
- [PixAddressKeyGetResponsePixAddressKeyType](PixAddressKeyGetResponsePixAddressKeyType.md)
- [PixAddressKeyListRequestPixAddressKeyStatus](PixAddressKeyListRequestPixAddressKeyStatus.md)
- [PixAddressKeyListResponseDTO](PixAddressKeyListResponseDTO.md)
- [PixAddressKeyQrCodeGetResponseDTO](PixAddressKeyQrCodeGetResponseDTO.md)
- [PixAddressKeySaveRequestDTO](PixAddressKeySaveRequestDTO.md)
- [PixAddressKeySaveRequestPixAddressKeyType](PixAddressKeySaveRequestPixAddressKeyType.md)
- [PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO](PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO.md)
- [PixAutomaticRecurringPaymentInstructionGetResponseDTO](PixAutomaticRecurringPaymentInstructionGetResponseDTO.md)
- [PixAutomaticRecurringPaymentInstructionListRequestPixAutomaticRecurringPaymentInstructionStatus](PixAutomaticRecurringPaymentInstructionListRequestPixAutomaticRecurringPaymentInstructionStatus.md)
- [PixAutomaticRecurringPaymentInstructionListResponseDTO](PixAutomaticRecurringPaymentInstructionListResponseDTO.md)
- [PixOriginalTransactionResponseDTO](PixOriginalTransactionResponseDTO.md)
- [PixQrCodeDecodeReceiverDTO](PixQrCodeDecodeReceiverDTO.md)
- [PixQrCodeDecodeReceiverPersonType](PixQrCodeDecodeReceiverPersonType.md)
- [PixQrCodeDecodeReceiverPixAccountType](PixQrCodeDecodeReceiverPixAccountType.md)
- [PixQrCodeDecodeRequestDTO](PixQrCodeDecodeRequestDTO.md)
- [PixQrCodeDecodeResponseDTO](PixQrCodeDecodeResponseDTO.md)
- [PixQrCodeDecodeResponsePixQrCodeType](PixQrCodeDecodeResponsePixQrCodeType.md)
- [PixQrCodeDecodeResponsePixTransactionCashValueFinality](PixQrCodeDecodeResponsePixTransactionCashValueFinality.md)
- [PixQrCodeDecodeResponsePixTransactionOriginType](PixQrCodeDecodeResponsePixTransactionOriginType.md)
- [PixQrCodeDeleteResponseDTO](PixQrCodeDeleteResponseDTO.md)
- [PixQrCodeSaveRequestDTO](PixQrCodeSaveRequestDTO.md)
- [PixQrCodeSaveResponseDTO](PixQrCodeSaveResponseDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationGetResponseDTO](PixReceiverAutomaticRecurringAuthorizationGetResponseDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringFrequency](PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringFrequency.md)
- [PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringOriginType](PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringOriginType.md)
- [PixReceiverAutomaticRecurringAuthorizationGetResponsePixReceiverAutomaticRecurringAuthorizationStatus](PixReceiverAutomaticRecurringAuthorizationGetResponsePixReceiverAutomaticRecurringAuthorizationStatus.md)
- [PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO](PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO](PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationListRequestPixReceiverAutomaticRecurringAuthorizationStatus](PixReceiverAutomaticRecurringAuthorizationListRequestPixReceiverAutomaticRecurringAuthorizationStatus.md)
- [PixReceiverAutomaticRecurringAuthorizationListResponseDTO](PixReceiverAutomaticRecurringAuthorizationListResponseDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO](PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationSaveRequestPixAutomaticRecurringFrequency](PixReceiverAutomaticRecurringAuthorizationSaveRequestPixAutomaticRecurringFrequency.md)
- [PixRecurringTransactionExternalAccountDTO](PixRecurringTransactionExternalAccountDTO.md)
- [PixRecurringTransactionGetItemResponseDTO](PixRecurringTransactionGetItemResponseDTO.md)
- [PixRecurringTransactionGetItemResponsePixRecurringTransactionItemStatus](PixRecurringTransactionGetItemResponsePixRecurringTransactionItemStatus.md)
- [PixRecurringTransactionGetResponseDTO](PixRecurringTransactionGetResponseDTO.md)
- [PixRecurringTransactionGetResponsePixRecurringTransactionFrequency](PixRecurringTransactionGetResponsePixRecurringTransactionFrequency.md)
- [PixRecurringTransactionGetResponsePixRecurringTransactionOrigin](PixRecurringTransactionGetResponsePixRecurringTransactionOrigin.md)
- [PixRecurringTransactionGetResponsePixRecurringTransactionStatus](PixRecurringTransactionGetResponsePixRecurringTransactionStatus.md)
- [PixRecurringTransactionListResponseDTO](PixRecurringTransactionListResponseDTO.md)
- [PixTokenBucketGetAddressKeyResponseDTO](PixTokenBucketGetAddressKeyResponseDTO.md)
- [PixTransactionExternalAccountResponseDTO](PixTransactionExternalAccountResponseDTO.md)
- [PixTransactionExternalAccountResponsePixAddressKeyType](PixTransactionExternalAccountResponsePixAddressKeyType.md)
- [PixTransactionGetResponseDTO](PixTransactionGetResponseDTO.md)
- [PixTransactionGetResponsePixAddressKeyType](PixTransactionGetResponsePixAddressKeyType.md)
- [PixTransactionGetResponsePixTransactionCashValueFinality](PixTransactionGetResponsePixTransactionCashValueFinality.md)
- [PixTransactionGetResponsePixTransactionOriginType](PixTransactionGetResponsePixTransactionOriginType.md)
- [PixTransactionGetResponsePixTransactionStatus](PixTransactionGetResponsePixTransactionStatus.md)
- [PixTransactionGetResponsePixTransactionType](PixTransactionGetResponsePixTransactionType.md)
- [PixTransactionListRequestPixTransactionStatus](PixTransactionListRequestPixTransactionStatus.md)
- [PixTransactionListRequestPixTransactionType](PixTransactionListRequestPixTransactionType.md)
- [PixTransactionListResponseDTO](PixTransactionListResponseDTO.md)
- [PixTransactionQrCodePayerResponseDTO](PixTransactionQrCodePayerResponseDTO.md)
- [PixTransactionQrCodeResponseDTO](PixTransactionQrCodeResponseDTO.md)
- [PixTransactionQrCodeSaveRequestDTO](PixTransactionQrCodeSaveRequestDTO.md)
- [PixTransactionSaveRequestDTO](PixTransactionSaveRequestDTO.md)
- [RecurringPixTransactionListItemsResponseDTO](RecurringPixTransactionListItemsResponseDTO.md)
- [RecurringPixTransactionListRequestPixRecurringTransactionStatus](RecurringPixTransactionListRequestPixRecurringTransactionStatus.md)
- [SubscriptionConfigureInvoiceRequestDTO](SubscriptionConfigureInvoiceRequestDTO.md)
- [SubscriptionDeleteInvoiceConfigResponseDTO](SubscriptionDeleteInvoiceConfigResponseDTO.md)
- [SubscriptionDeleteResponseDTO](SubscriptionDeleteResponseDTO.md)
- [SubscriptionGetInvoicesRequestInvoiceStatus](SubscriptionGetInvoicesRequestInvoiceStatus.md)
- [SubscriptionGetResponseBillingType](SubscriptionGetResponseBillingType.md)
- [SubscriptionGetResponseCycle](SubscriptionGetResponseCycle.md)
- [SubscriptionGetResponseDTO](SubscriptionGetResponseDTO.md)
- [SubscriptionGetResponseSubscriptionStatus](SubscriptionGetResponseSubscriptionStatus.md)
- [SubscriptionInvoiceConfigGetResponseDTO](SubscriptionInvoiceConfigGetResponseDTO.md)
- [SubscriptionInvoiceConfigUpdateRequestDTO](SubscriptionInvoiceConfigUpdateRequestDTO.md)
- [SubscriptionListPaymentsRequestPaymentStatus](SubscriptionListPaymentsRequestPaymentStatus.md)
- [SubscriptionListRequestBillingType](SubscriptionListRequestBillingType.md)
- [SubscriptionListRequestSubscriptionStatus](SubscriptionListRequestSubscriptionStatus.md)
- [SubscriptionListResponseDTO](SubscriptionListResponseDTO.md)
- [SubscriptionSaveRequestBillingType](SubscriptionSaveRequestBillingType.md)
- [SubscriptionSaveRequestCycle](SubscriptionSaveRequestCycle.md)
- [SubscriptionSaveRequestDTO](SubscriptionSaveRequestDTO.md)
- [SubscriptionSaveWithCreditCardRequestBillingType](SubscriptionSaveWithCreditCardRequestBillingType.md)
- [SubscriptionSaveWithCreditCardRequestCycle](SubscriptionSaveWithCreditCardRequestCycle.md)
- [SubscriptionSaveWithCreditCardRequestDTO](SubscriptionSaveWithCreditCardRequestDTO.md)
- [SubscriptionSaveWithCreditCardResponseBillingType](SubscriptionSaveWithCreditCardResponseBillingType.md)
- [SubscriptionSaveWithCreditCardResponseCycle](SubscriptionSaveWithCreditCardResponseCycle.md)
- [SubscriptionSaveWithCreditCardResponseDTO](SubscriptionSaveWithCreditCardResponseDTO.md)
- [SubscriptionSaveWithCreditCardResponseSubscriptionStatus](SubscriptionSaveWithCreditCardResponseSubscriptionStatus.md)
- [SubscriptionSplitRequestDTO](SubscriptionSplitRequestDTO.md)
- [SubscriptionSplitResponseDTO](SubscriptionSplitResponseDTO.md)
- [SubscriptionSplitResponseSubscriptionSplitDisabledReason](SubscriptionSplitResponseSubscriptionSplitDisabledReason.md)
- [SubscriptionSplitResponseSubscriptionSplitStatus](SubscriptionSplitResponseSubscriptionSplitStatus.md)
- [SubscriptionUpdateCreditCardRequestDTO](SubscriptionUpdateCreditCardRequestDTO.md)
- [SubscriptionUpdateRequestBillingType](SubscriptionUpdateRequestBillingType.md)
- [SubscriptionUpdateRequestCycle](SubscriptionUpdateRequestCycle.md)
- [SubscriptionUpdateRequestDTO](SubscriptionUpdateRequestDTO.md)
- [SubscriptionUpdateRequestSubscriptionStatus](SubscriptionUpdateRequestSubscriptionStatus.md)
- [TransferBankAccountGetResponseDTO](TransferBankAccountGetResponseDTO.md)
- [TransferBankAccountSaveRequestBankAccountType](TransferBankAccountSaveRequestBankAccountType.md)
- [TransferBankAccountSaveRequestDTO](TransferBankAccountSaveRequestDTO.md)
- [TransferBankGetResponseDTO](TransferBankGetResponseDTO.md)
- [TransferBankSaveRequestDTO](TransferBankSaveRequestDTO.md)
- [TransferGetResponseDTO](TransferGetResponseDTO.md)
- [TransferGetResponseTransferStatus](TransferGetResponseTransferStatus.md)
- [TransferGetResponseTransferType](TransferGetResponseTransferType.md)
- [TransferListResponseDTO](TransferListResponseDTO.md)
- [TransferRecurringSaveRequestDTO](TransferRecurringSaveRequestDTO.md)
- [TransferRecurringSaveRequestRecurringCheckoutScheduleFrequency](TransferRecurringSaveRequestRecurringCheckoutScheduleFrequency.md)
- [TransferSaveInternalTransferAccountDTO](TransferSaveInternalTransferAccountDTO.md)
- [TransferSaveInternalTransferRequestDTO](TransferSaveInternalTransferRequestDTO.md)
- [TransferSaveInternalTransferResponseDTO](TransferSaveInternalTransferResponseDTO.md)
- [TransferSaveInternalTransferResponseTransferStatus](TransferSaveInternalTransferResponseTransferStatus.md)
- [TransferSaveInternalTransferResponseTransferType](TransferSaveInternalTransferResponseTransferType.md)
- [TransferSaveRequestDTO](TransferSaveRequestDTO.md)
- [TransferSaveRequestPixAddressKeyType](TransferSaveRequestPixAddressKeyType.md)
- [TransferSaveRequestTransferType](TransferSaveRequestTransferType.md)
- [WalletGetResponseDTO](WalletGetResponseDTO.md)
- [WalletShowResponseDTO](WalletShowResponseDTO.md)
- [WebhookConfigDeleteResponseDTO](WebhookConfigDeleteResponseDTO.md)
- [WebhookConfigGetResponseDTO](WebhookConfigGetResponseDTO.md)
- [WebhookConfigGetResponseWebhookEvent](WebhookConfigGetResponseWebhookEvent.md)
- [WebhookConfigGetResponseWebhookSendType](WebhookConfigGetResponseWebhookSendType.md)
- [WebhookConfigListResponseDTO](WebhookConfigListResponseDTO.md)
- [WebhookConfigSaveRequestDTO](WebhookConfigSaveRequestDTO.md)
- [WebhookConfigSaveRequestWebhookEvent](WebhookConfigSaveRequestWebhookEvent.md)
- [WebhookConfigSaveRequestWebhookSendType](WebhookConfigSaveRequestWebhookSendType.md)
- [WebhookConfigUpdateRequestDTO](WebhookConfigUpdateRequestDTO.md)
- [WebhookConfigUpdateRequestWebhookEvent](WebhookConfigUpdateRequestWebhookEvent.md)
- [WebhookConfigUpdateRequestWebhookSendType](WebhookConfigUpdateRequestWebhookSendType.md)

<a id="documentation-for-authorization"></a>

## Documentation For Authorization

Authentication schemes defined for the API:
<a id="Authorization"></a>

### Authorization

- **Type**: API key
- **API key parameter name**: access_token
- **Location**: HTTP header

## Author

- Giovanni Chahin Morassi
