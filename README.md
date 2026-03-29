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

| Class                              | Method                                                                                                                                                                                                      | HTTP request                                                        | Description                                                                     |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| _AesEmSandboxApi_                  | [**confirmar_pagamento**](docs/AesEmSandboxApi.md#confirmar_pagamento)                                                                                                                                      | **POST** /v3/sandbox/payment/{id}/confirm                           | (Apenas sandbox) Confirmar o pagamento                                          |
| _AesEmSandboxApi_                  | [**forcar_vencimento**](docs/AesEmSandboxApi.md#forcar_vencimento)                                                                                                                                          | **POST** /v3/sandbox/payment/{id}/overdue                           | (Apenas sandbox) Forçar o vencimento de uma cobrança                            |
| _AntecipaesApi_                    | [**atualizar_status_da_antecipacao_automatica**](docs/AntecipaesApi.md#atualizar_status_da_antecipacao_automatica)                                                                                          | **PUT** /v3/anticipations/configurations                            | Atualizar status da antecipação automática                                      |
| _AntecipaesApi_                    | [**cancelar_antecipacao**](docs/AntecipaesApi.md#cancelar_antecipacao)                                                                                                                                      | **POST** /v3/anticipations/{id}/cancel                              | Cancelar antecipação                                                            |
| _AntecipaesApi_                    | [**listar_antecipacoes**](docs/AntecipaesApi.md#listar_antecipacoes)                                                                                                                                        | **GET** /v3/anticipations                                           | Listar antecipações                                                             |
| _AntecipaesApi_                    | [**recuperar_limites_de_antecipacoes**](docs/AntecipaesApi.md#recuperar_limites_de_antecipacoes)                                                                                                            | **GET** /v3/anticipations/limits                                    | Recuperar limites de antecipações                                               |
| _AntecipaesApi_                    | [**recuperar_status_da_antecipacao_automatica**](docs/AntecipaesApi.md#recuperar_status_da_antecipacao_automatica)                                                                                          | **GET** /v3/anticipations/configurations                            | Recuperar status da antecipação automática                                      |
| _AntecipaesApi_                    | [**recuperar_uma_unica_antecipacao**](docs/AntecipaesApi.md#recuperar_uma_unica_antecipacao)                                                                                                                | **GET** /v3/anticipations/{id}                                      | Recuperar uma única antecipação                                                 |
| _AntecipaesApi_                    | [**simular_antecipao**](docs/AntecipaesApi.md#simular_antecipao)                                                                                                                                            | **POST** /v3/anticipations/simulate                                 | Simular antecipação                                                             |
| _AntecipaesApi_                    | [**solicitar_antecipacao**](docs/AntecipaesApi.md#solicitar_antecipacao)                                                                                                                                    | **POST** /v3/anticipations                                          | Solicitar antecipação                                                           |
| _AssinaturasApi_                   | [**atualizar_assinatura_existente**](docs/AssinaturasApi.md#atualizar_assinatura_existente)                                                                                                                 | **PUT** /v3/subscriptions/{id}                                      | Atualizar assinatura existente                                                  |
| _AssinaturasApi_                   | [**atualizar_cartao_de_credito_assinatura**](docs/AssinaturasApi.md#atualizar_cartao_de_credito_assinatura)                                                                                                 | **PUT** /v3/subscriptions/{id}/creditCard                           | Atualiza o cartão de crédito sem efetuar cobrança                               |
| _AssinaturasApi_                   | [**atualizar_configuracao_para_emissao_de_notas_fiscais**](docs/AssinaturasApi.md#atualizar_configuracao_para_emissao_de_notas_fiscais)                                                                     | **PUT** /v3/subscriptions/{id}/invoiceSettings                      | Atualizar configuração para emissão de Notas Fiscais                            |
| _AssinaturasApi_                   | [**criar_assinatura_com_cartao_de_credito**](docs/AssinaturasApi.md#criar_assinatura_com_cartao_de_credito)                                                                                                 | **POST** /v3/subscriptions/                                         | Criar assinatura com cartão de crédito                                          |
| _AssinaturasApi_                   | [**criar_configuracao_para_emissao_de_notas_fiscais**](docs/AssinaturasApi.md#criar_configuracao_para_emissao_de_notas_fiscais)                                                                             | **POST** /v3/subscriptions/{id}/invoiceSettings                     | Criar configuração para emissão de Notas Fiscais                                |
| _AssinaturasApi_                   | [**criar_nova_assinatura**](docs/AssinaturasApi.md#criar_nova_assinatura)                                                                                                                                   | **POST** /v3/subscriptions                                          | Criar nova assinatura                                                           |
| _AssinaturasApi_                   | [**gerar_carne_de_assinatura**](docs/AssinaturasApi.md#gerar_carne_de_assinatura)                                                                                                                           | **GET** /v3/subscriptions/{id}/paymentBook                          | Gerar carnê de assinatura                                                       |
| _AssinaturasApi_                   | [**listar_assinaturas**](docs/AssinaturasApi.md#listar_assinaturas)                                                                                                                                         | **GET** /v3/subscriptions                                           | Listar assinaturas                                                              |
| _AssinaturasApi_                   | [**listar_cobrancas_de_uma_assinatura**](docs/AssinaturasApi.md#listar_cobrancas_de_uma_assinatura)                                                                                                         | **GET** /v3/subscriptions/{id}/payments                             | Listar cobranças de uma assinatura                                              |
| _AssinaturasApi_                   | [**listar_notas_fiscais_das_cobrancas_de_uma_assinatura**](docs/AssinaturasApi.md#listar_notas_fiscais_das_cobrancas_de_uma_assinatura)                                                                     | **GET** /v3/subscriptions/{id}/invoices                             | Listar notas fiscais das cobranças de uma assinatura                            |
| _AssinaturasApi_                   | [**recuperar_configuracao_para_emissao_de_notas_fiscais**](docs/AssinaturasApi.md#recuperar_configuracao_para_emissao_de_notas_fiscais)                                                                     | **GET** /v3/subscriptions/{id}/invoiceSettings                      | Recuperar configuração para emissão de notas fiscais                            |
| _AssinaturasApi_                   | [**recuperar_uma_unica_assinatura**](docs/AssinaturasApi.md#recuperar_uma_unica_assinatura)                                                                                                                 | **GET** /v3/subscriptions/{id}                                      | Recuperar uma única assinatura                                                  |
| _AssinaturasApi_                   | [**remover_assinatura**](docs/AssinaturasApi.md#remover_assinatura)                                                                                                                                         | **DELETE** /v3/subscriptions/{id}                                   | Remover assinatura                                                              |
| _AssinaturasApi_                   | [**remover_configuracao_para_emissao_de_notas_fiscais**](docs/AssinaturasApi.md#remover_configuracao_para_emissao_de_notas_fiscais)                                                                         | **DELETE** /v3/subscriptions/{id}/invoiceSettings                   | Remover configuração para emissão de Notas Fiscais                              |
| _CartoDeCrditoApi_                 | [**recuperar_configuracao_de_pre_autorizacao**](docs/CartoDeCrditoApi.md#recuperar_configuracao_de_pre_autorizacao)                                                                                         | **GET** /v3/creditCard/preAuthorization/config                      | Recuperar configuração da pré-autorização                                       |
| _CartoDeCrditoApi_                 | [**salvar_ou_atualizar_configuracao_de_pre_autorizacao**](docs/CartoDeCrditoApi.md#salvar_ou_atualizar_configuracao_de_pre_autorizacao)                                                                     | **POST** /v3/creditCard/preAuthorization/config                     | Salvar ou atualizar configuração da pré-autorização                             |
| _CartoDeCrditoApi_                 | [**tokenizacao_de_cartao_de_credito**](docs/CartoDeCrditoApi.md#tokenizacao_de_cartao_de_credito)                                                                                                           | **POST** /v3/creditCard/tokenizeCreditCard                          | Tokenização de cartão de crédito                                                |
| _ChargebackApi_                    | [**criar_disputa_de_chargeback**](docs/ChargebackApi.md#criar_disputa_de_chargeback)                                                                                                                        | **POST** /v3/chargebacks/{id}/dispute                               | Criar disputa de chargeback                                                     |
| _ChargebackApi_                    | [**listar_chargebacks**](docs/ChargebackApi.md#listar_chargebacks)                                                                                                                                          | **GET** /v3/chargebacks/                                            | Listar chargebacks                                                              |
| _ChargebackApi_                    | [**recuperar_um_unico_chargeback**](docs/ChargebackApi.md#recuperar_um_unico_chargeback)                                                                                                                    | **GET** /v3/payments/{id}/chargeback                                | Recuperar um único chargeback                                                   |
| _CheckoutApi_                      | [**cancelar_um_checkout**](docs/CheckoutApi.md#cancelar_um_checkout)                                                                                                                                        | **POST** /v3/checkouts/{id}/cancel                                  | Cancelar um checkout                                                            |
| _CheckoutApi_                      | [**criar_novo_checkout**](docs/CheckoutApi.md#criar_novo_checkout)                                                                                                                                          | **POST** /v3/checkouts                                              | Criar novo checkout                                                             |
| _ClientesApi_                      | [**atualizar_cliente_existente**](docs/ClientesApi.md#atualizar_cliente_existente)                                                                                                                          | **PUT** /v3/customers/{id}                                          | Atualizar cliente existente                                                     |
| _ClientesApi_                      | [**criar_novo_cliente**](docs/ClientesApi.md#criar_novo_cliente)                                                                                                                                            | **POST** /v3/customers                                              | Criar novo cliente                                                              |
| _ClientesApi_                      | [**listar_clientes**](docs/ClientesApi.md#listar_clientes)                                                                                                                                                  | **GET** /v3/customers                                               | Listar clientes                                                                 |
| _ClientesApi_                      | [**recuperar_notificacoes_de_um_cliente**](docs/ClientesApi.md#recuperar_notificacoes_de_um_cliente)                                                                                                        | **GET** /v3/customers/{id}/notifications                            | Recuperar notificações de um cliente                                            |
| _ClientesApi_                      | [**recuperar_um_unico_cliente**](docs/ClientesApi.md#recuperar_um_unico_cliente)                                                                                                                            | **GET** /v3/customers/{id}                                          | Recuperar um único cliente                                                      |
| _ClientesApi_                      | [**remover_cliente**](docs/ClientesApi.md#remover_cliente)                                                                                                                                                  | **DELETE** /v3/customers/{id}                                       | Remover cliente                                                                 |
| _ClientesApi_                      | [**restaurar_cliente_removido**](docs/ClientesApi.md#restaurar_cliente_removido)                                                                                                                            | **POST** /v3/customers/{id}/restore                                 | Restaurar cliente removido                                                      |
| _CobranasApi_                      | [**atualizar_cobranca_existente**](docs/CobranasApi.md#atualizar_cobranca_existente)                                                                                                                        | **PUT** /v3/payments/{id}                                           | Atualizar cobrança existente                                                    |
| _CobranasApi_                      | [**capturar_cobranca_com_pre_autorizacao**](docs/CobranasApi.md#capturar_cobranca_com_pre_autorizacao)                                                                                                      | **POST** /v3/payments/{id}/captureAuthorizedPayment                 | Capturar cobrança com Pré-Autorização                                           |
| _CobranasApi_                      | [**confirmar_recebimento_em_dinheiro**](docs/CobranasApi.md#confirmar_recebimento_em_dinheiro)                                                                                                              | **POST** /v3/payments/{id}/receiveInCash                            | Confirmar recebimento em dinheiro                                               |
| _CobranasApi_                      | [**criar_cobranca_com_cartao_de_credito**](docs/CobranasApi.md#criar_cobranca_com_cartao_de_credito)                                                                                                        | **POST** /v3/payments/                                              | Criar cobrança com cartão de crédito                                            |
| _CobranasApi_                      | [**criar_nova_cobranca**](docs/CobranasApi.md#criar_nova_cobranca)                                                                                                                                          | **POST** /v3/payments                                               | Criar nova cobrança                                                             |
| _CobranasApi_                      | [**desfazer_confirmacao_de_recebimento_em_dinheiro**](docs/CobranasApi.md#desfazer_confirmacao_de_recebimento_em_dinheiro)                                                                                  | **POST** /v3/payments/{id}/undoReceivedInCash                       | Desfazer confirmação de recebimento em dinheiro                                 |
| _CobranasApi_                      | [**estornar_cobranca**](docs/CobranasApi.md#estornar_cobranca)                                                                                                                                              | **POST** /v3/payments/{id}/refund                                   | Estornar cobrança                                                               |
| _CobranasApi_                      | [**excluir_cobranca**](docs/CobranasApi.md#excluir_cobranca)                                                                                                                                                | **DELETE** /v3/payments/{id}                                        | Excluir cobrança                                                                |
| _CobranasApi_                      | [**informacoes_sobre_visualizacao_da_cobranca**](docs/CobranasApi.md#informacoes_sobre_visualizacao_da_cobranca)                                                                                            | **GET** /v3/payments/{id}/viewingInfo                               | Informações sobre visualização da cobrança                                      |
| _CobranasApi_                      | [**listar_cobrancas**](docs/CobranasApi.md#listar_cobrancas)                                                                                                                                                | **GET** /v3/payments                                                | Listar cobranças                                                                |
| _CobranasApi_                      | [**obter_linha_digitavel_do_boleto**](docs/CobranasApi.md#obter_linha_digitavel_do_boleto)                                                                                                                  | **GET** /v3/payments/{id}/identificationField                       | Obter linha digitável do boleto                                                 |
| _CobranasApi_                      | [**obter_qr_code_para_pagamentos_via_pix**](docs/CobranasApi.md#obter_qr_code_para_pagamentos_via_pix)                                                                                                      | **GET** /v3/payments/{id}/pixQrCode                                 | Obter QR Code para pagamentos via Pix                                           |
| _CobranasApi_                      | [**pagar_uma_cobranca_com_cartao_de_credito**](docs/CobranasApi.md#pagar_uma_cobranca_com_cartao_de_credito)                                                                                                | **POST** /v3/payments/{id}/payWithCreditCard                        | Pagar uma cobrança com cartão de crédito                                        |
| _CobranasApi_                      | [**recuperando_limites_de_cobrancas**](docs/CobranasApi.md#recuperando_limites_de_cobrancas)                                                                                                                | **GET** /v3/payments/limits                                         | Recuperando limites de cobranças                                                |
| _CobranasApi_                      | [**recuperar_informacoes_de_pagamento_de_uma_cobranca**](docs/CobranasApi.md#recuperar_informacoes_de_pagamento_de_uma_cobranca)                                                                            | **GET** /v3/payments/{id}/billingInfo                               | Recuperar informações de pagamento de uma cobrança                              |
| _CobranasApi_                      | [**recuperar_status_de_uma_cobranca**](docs/CobranasApi.md#recuperar_status_de_uma_cobranca)                                                                                                                | **GET** /v3/payments/{id}/status                                    | Recuperar status de uma cobrança                                                |
| _CobranasApi_                      | [**recuperar_uma_unica_cobranca**](docs/CobranasApi.md#recuperar_uma_unica_cobranca)                                                                                                                        | **GET** /v3/payments/{id}                                           | Recuperar uma única cobrança                                                    |
| _CobranasApi_                      | [**restaurar_cobranca_removida**](docs/CobranasApi.md#restaurar_cobranca_removida)                                                                                                                          | **POST** /v3/payments/{id}/restore                                  | Restaurar cobrança removida                                                     |
| _CobranasApi_                      | [**simulador_de_vendas**](docs/CobranasApi.md#simulador_de_vendas)                                                                                                                                          | **POST** /v3/payments/simulate                                      | Simulador de vendas                                                             |
| _CobranasComDadosResumidosApi_     | [**atualizar_cobranca_existente_com_dados_resumidos_na_resposta**](docs/CobranasComDadosResumidosApi.md#atualizar_cobranca_existente_com_dados_resumidos_na_resposta)                                       | **PUT** /v3/lean/payments/{id}                                      | Atualizar cobrança existente com dados resumidos na resposta                    |
| _CobranasComDadosResumidosApi_     | [**capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta**](docs/CobranasComDadosResumidosApi.md#capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta)                     | **POST** /v3/lean/payments/{id}/captureAuthorizedPayment            | Capturar cobrança com Pré-Autorização com dados resumidos na resposta           |
| _CobranasComDadosResumidosApi_     | [**confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta**](docs/CobranasComDadosResumidosApi.md#confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta)                             | **POST** /v3/lean/payments/{id}/receiveInCash                       | Confirmar recebimento em dinheiro com dados resumidos na resposta               |
| _CobranasComDadosResumidosApi_     | [**criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta**](docs/CobranasComDadosResumidosApi.md#criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta)                       | **POST** /v3/lean/payments/                                         | Criar cobrança com cartão de crédito com dados resumidos na resposta            |
| _CobranasComDadosResumidosApi_     | [**criar_nova_cobranca_com_dados_resumidos_na_resposta**](docs/CobranasComDadosResumidosApi.md#criar_nova_cobranca_com_dados_resumidos_na_resposta)                                                         | **POST** /v3/lean/payments                                          | Criar nova cobrança com dados resumidos na resposta                             |
| _CobranasComDadosResumidosApi_     | [**desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta**](docs/CobranasComDadosResumidosApi.md#desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta) | **POST** /v3/lean/payments/{id}/undoReceivedInCash                  | Desfazer confirmação de recebimento em dinheiro com dados resumidos na resposta |
| _CobranasComDadosResumidosApi_     | [**estornar_cobranca_com_dados_resumidos_na_resposta**](docs/CobranasComDadosResumidosApi.md#estornar_cobranca_com_dados_resumidos_na_resposta)                                                             | **POST** /v3/lean/payments/{id}/refund                              | Estornar cobrança com dados resumidos na resposta                               |
| _CobranasComDadosResumidosApi_     | [**excluir_cobranca_com_dados_resumidos**](docs/CobranasComDadosResumidosApi.md#excluir_cobranca_com_dados_resumidos)                                                                                       | **DELETE** /v3/lean/payments/{id}                                   | Excluir cobrança com dados resumidos                                            |
| _CobranasComDadosResumidosApi_     | [**listar_cobrancas_com_dados_resumidos**](docs/CobranasComDadosResumidosApi.md#listar_cobrancas_com_dados_resumidos)                                                                                       | **GET** /v3/lean/payments                                           | Listar cobranças com dados resumidos                                            |
| _CobranasComDadosResumidosApi_     | [**recuperar_uma_unica_cobranca_com_dados_resumidos**](docs/CobranasComDadosResumidosApi.md#recuperar_uma_unica_cobranca_com_dados_resumidos)                                                               | **GET** /v3/lean/payments/{id}                                      | Recuperar uma única cobrança com dados resumidos                                |
| _CobranasComDadosResumidosApi_     | [**restaurar_cobranca_removida_com_dados_resumidos_na_resposta**](docs/CobranasComDadosResumidosApi.md#restaurar_cobranca_removida_com_dados_resumidos_na_resposta)                                         | **POST** /v3/lean/payments/{id}/restore                             | Restaurar cobrança removida com dados resumidos na resposta                     |
| _ConfiguraesDeWebhooksApi_         | [**atualizar_webhook_existente**](docs/ConfiguraesDeWebhooksApi.md#atualizar_webhook_existente)                                                                                                             | **PUT** /v3/webhooks/{id}                                           | Atualizar webhook existente                                                     |
| _ConfiguraesDeWebhooksApi_         | [**criar_novo_webhook**](docs/ConfiguraesDeWebhooksApi.md#criar_novo_webhook)                                                                                                                               | **POST** /v3/webhooks                                               | Criar novo webhook                                                              |
| _ConfiguraesDeWebhooksApi_         | [**listar_webhooks**](docs/ConfiguraesDeWebhooksApi.md#listar_webhooks)                                                                                                                                     | **GET** /v3/webhooks                                                | Listar webhooks                                                                 |
| _ConfiguraesDeWebhooksApi_         | [**recuperar_um_unico_webhook**](docs/ConfiguraesDeWebhooksApi.md#recuperar_um_unico_webhook)                                                                                                               | **GET** /v3/webhooks/{id}                                           | Recuperar um único webhook                                                      |
| _ConfiguraesDeWebhooksApi_         | [**remover_penalizacao_webhook**](docs/ConfiguraesDeWebhooksApi.md#remover_penalizacao_webhook)                                                                                                             | **POST** /v3/webhooks/{id}/removeBackoff                            | Remover penalização de webhook                                                  |
| _ConfiguraesDeWebhooksApi_         | [**remover_webhook**](docs/ConfiguraesDeWebhooksApi.md#remover_webhook)                                                                                                                                     | **DELETE** /v3/webhooks/{id}                                        | Remover um webhook                                                              |
| _ConsultaSerasaApi_                | [**listar_consultas**](docs/ConsultaSerasaApi.md#listar_consultas)                                                                                                                                          | **GET** /v3/creditBureauReport                                      | Listar consultas                                                                |
| _ConsultaSerasaApi_                | [**realizar_consulta**](docs/ConsultaSerasaApi.md#realizar_consulta)                                                                                                                                        | **POST** /v3/creditBureauReport                                     | Realizar consulta                                                               |
| _ConsultaSerasaApi_                | [**recuperar_uma_consulta**](docs/ConsultaSerasaApi.md#recuperar_uma_consulta)                                                                                                                              | **GET** /v3/creditBureauReport/{id}                                 | Recuperar uma consulta                                                          |
| _ContaEscrowApi_                   | [**criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas**](docs/ContaEscrowApi.md#criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas)                                           | **POST** /v3/accounts/escrow                                        | Criar configuração padrão da Conta Escrow para todas as subcontas               |
| _ContaEscrowApi_                   | [**encerrar_garantia_da_cobranca_na_conta_escrow**](docs/ContaEscrowApi.md#encerrar_garantia_da_cobranca_na_conta_escrow)                                                                                   | **POST** /v3/escrow/{id}/finish                                     | Encerrar garantia da cobrança na Conta Escrow                                   |
| _ContaEscrowApi_                   | [**recuperar_configuracao_da_conta_escrow_para_a_subconta**](docs/ContaEscrowApi.md#recuperar_configuracao_da_conta_escrow_para_a_subconta)                                                                 | **GET** /v3/accounts/{id}/escrow                                    | Recuperar configuração da Conta Escrow para a subconta                          |
| _ContaEscrowApi_                   | [**recuperar_configuracao_padrao_da_conta_escrow**](docs/ContaEscrowApi.md#recuperar_configuracao_padrao_da_conta_escrow)                                                                                   | **GET** /v3/accounts/escrow                                         | Recuperar configuração padrão da Conta Escrow                                   |
| _ContaEscrowApi_                   | [**recuperar_garantia_da_cobranca_na_conta_escrow**](docs/ContaEscrowApi.md#recuperar_garantia_da_cobranca_na_conta_escrow)                                                                                 | **GET** /v3/payments/{id}/escrow                                    | Recuperar garantia da cobrança na Conta Escrow                                  |
| _ContaEscrowApi_                   | [**salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta**](docs/ContaEscrowApi.md#salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta)                                             | **POST** /v3/accounts/{id}/escrow                                   | Salvar ou atualizar configuração da Conta Escrow para a subconta                |
| _DocumentosDeCobranasApi_          | [**atualizar_definicoes_de_um_documento_da_cobranca**](docs/DocumentosDeCobranasApi.md#atualizar_definicoes_de_um_documento_da_cobranca)                                                                    | **PUT** /v3/payments/{id}/documents/{documentId}                    | Atualizar definições de um documento da cobrança                                |
| _DocumentosDeCobranasApi_          | [**excluir_documento_de_uma_cobranca**](docs/DocumentosDeCobranasApi.md#excluir_documento_de_uma_cobranca)                                                                                                  | **DELETE** /v3/payments/{id}/documents/{documentId}                 | Excluir documento de uma cobrança                                               |
| _DocumentosDeCobranasApi_          | [**fazer_upload_de_documentos_da_cobranca**](docs/DocumentosDeCobranasApi.md#fazer_upload_de_documentos_da_cobranca)                                                                                        | **POST** /v3/payments/{id}/documents                                | Fazer upload de documentos da cobrança                                          |
| _DocumentosDeCobranasApi_          | [**listar_documentos_de_uma_cobranca**](docs/DocumentosDeCobranasApi.md#listar_documentos_de_uma_cobranca)                                                                                                  | **GET** /v3/payments/{id}/documents                                 | Listar documentos de uma cobrança                                               |
| _DocumentosDeCobranasApi_          | [**recuperar_um_unico_documento_da_cobranca**](docs/DocumentosDeCobranasApi.md#recuperar_um_unico_documento_da_cobranca)                                                                                    | **GET** /v3/payments/{id}/documents/{documentId}                    | Recuperar um único documento da cobrança                                        |
| _EnvioDeDocumentosWhiteLabelApi_   | [**atualizar_documento_enviado**](docs/EnvioDeDocumentosWhiteLabelApi.md#atualizar_documento_enviado)                                                                                                       | **POST** /v3/myAccount/documents/files/{id}                         | Atualizar documento enviado                                                     |
| _EnvioDeDocumentosWhiteLabelApi_   | [**enviar_documentos**](docs/EnvioDeDocumentosWhiteLabelApi.md#enviar_documentos)                                                                                                                           | **POST** /v3/myAccount/documents/{id}                               | Enviar documentos                                                               |
| _EnvioDeDocumentosWhiteLabelApi_   | [**remover_documento_enviado**](docs/EnvioDeDocumentosWhiteLabelApi.md#remover_documento_enviado)                                                                                                           | **DELETE** /v3/myAccount/documents/files/{id}                       | Remover documento enviado                                                       |
| _EnvioDeDocumentosWhiteLabelApi_   | [**verificar_documentos_pendentes**](docs/EnvioDeDocumentosWhiteLabelApi.md#verificar_documentos_pendentes)                                                                                                 | **GET** /v3/myAccount/documents                                     | Verificar documentos pendentes                                                  |
| _EnvioDeDocumentosWhiteLabelApi_   | [**visualizar_documento_enviado**](docs/EnvioDeDocumentosWhiteLabelApi.md#visualizar_documento_enviado)                                                                                                     | **GET** /v3/myAccount/documents/files/{id}                          | Visualizar documento enviado                                                    |
| _EstornosApi_                      | [**estornar_boleto**](docs/EstornosApi.md#estornar_boleto)                                                                                                                                                  | **POST** /v3/payments/{id}/bankSlip/refund                          | Estornar boleto                                                                 |
| _EstornosApi_                      | [**listar_estornos_de_uma_cobranca**](docs/EstornosApi.md#listar_estornos_de_uma_cobranca)                                                                                                                  | **GET** /v3/payments/{id}/refunds                                   | Listar estornos de uma cobrança                                                 |
| _ExtratoApi_                       | [**recuperar_extrato**](docs/ExtratoApi.md#recuperar_extrato)                                                                                                                                               | **GET** /v3/financialTransactions                                   | Recuperar extrato                                                               |
| _InformaesEPersonalizaoDaContaApi_ | [**aprovar_conta**](docs/InformaesEPersonalizaoDaContaApi.md#aprovar_conta)                                                                                                                                 | **POST** /v3/sandbox/myAccount/approve                              | (Apenas Sandbox) Aprovar conta                                                  |
| _InformaesEPersonalizaoDaContaApi_ | [**atualizar_dados_comerciais**](docs/InformaesEPersonalizaoDaContaApi.md#atualizar_dados_comerciais)                                                                                                       | **POST** /v3/myAccount/commercialInfo/                              | Atualizar dados comerciais                                                      |
| _InformaesEPersonalizaoDaContaApi_ | [**consultar_situacao_cadastral_da_conta**](docs/InformaesEPersonalizaoDaContaApi.md#consultar_situacao_cadastral_da_conta)                                                                                 | **GET** /v3/myAccount/status/                                       | Consultar situação cadastral da conta                                           |
| _InformaesEPersonalizaoDaContaApi_ | [**excluir_subconta_white_label**](docs/InformaesEPersonalizaoDaContaApi.md#excluir_subconta_white_label)                                                                                                   | **DELETE** /v3/myAccount/                                           | Excluir subconta White Label                                                    |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_configuracoes_de_personalizacao**](docs/InformaesEPersonalizaoDaContaApi.md#recuperar_configuracoes_de_personalizacao)                                                                         | **GET** /v3/myAccount/paymentCheckoutConfig/                        | Recuperar configurações de personalização                                       |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_dados_comerciais**](docs/InformaesEPersonalizaoDaContaApi.md#recuperar_dados_comerciais)                                                                                                       | **GET** /v3/myAccount/commercialInfo/                               | Recuperar dados comerciais                                                      |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_numero_de_conta_no_asaas**](docs/InformaesEPersonalizaoDaContaApi.md#recuperar_numero_de_conta_no_asaas)                                                                                       | **GET** /v3/myAccount/accountNumber                                 | Recuperar número de conta no Asaas                                              |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_taxas_da_conta**](docs/InformaesEPersonalizaoDaContaApi.md#recuperar_taxas_da_conta)                                                                                                           | **GET** /v3/myAccount/fees/                                         | Recuperar taxas da conta                                                        |
| _InformaesEPersonalizaoDaContaApi_ | [**recuperar_walletid**](docs/InformaesEPersonalizaoDaContaApi.md#recuperar_walletid)                                                                                                                       | **GET** /v3/wallets/                                                | Recuperar WalletId                                                              |
| _InformaesEPersonalizaoDaContaApi_ | [**salvar_personalizacao_da_fatura**](docs/InformaesEPersonalizaoDaContaApi.md#salvar_personalizacao_da_fatura)                                                                                             | **POST** /v3/myAccount/paymentCheckoutConfig/                       | Salvar personalização da fatura                                                 |
| _InformaesFinanceirasApi_          | [**estatisticas_de_cobrancas**](docs/InformaesFinanceirasApi.md#estatisticas_de_cobrancas)                                                                                                                  | **GET** /v3/finance/payment/statistics                              | Estatísticas de cobranças                                                       |
| _InformaesFinanceirasApi_          | [**recuperar_saldo_da_conta**](docs/InformaesFinanceirasApi.md#recuperar_saldo_da_conta)                                                                                                                    | **GET** /v3/finance/balance                                         | Recuperar saldo da conta                                                        |
| _InformaesFinanceirasApi_          | [**recuperar_valores_de_split**](docs/InformaesFinanceirasApi.md#recuperar_valores_de_split)                                                                                                                | **GET** /v3/finance/split/statistics                                | Recuperar valores de split                                                      |
| _InformaesFiscaisApi_              | [**configurar_portal_emissor_de_notas_fiscais**](docs/InformaesFiscaisApi.md#configurar_portal_emissor_de_notas_fiscais)                                                                                    | **POST** /v3/fiscalInfo/nationalPortal                              | Configurar portal emissor de notas fiscais                                      |
| _InformaesFiscaisApi_              | [**criar_e_atualizar_informacoes_fiscais**](docs/InformaesFiscaisApi.md#criar_e_atualizar_informacoes_fiscais)                                                                                              | **POST** /v3/fiscalInfo/                                            | Criar e atualizar informações fiscais                                           |
| _InformaesFiscaisApi_              | [**listar_codigos_de_classificacoes_tributarias**](docs/InformaesFiscaisApi.md#listar_codigos_de_classificacoes_tributarias)                                                                                | **GET** /v3/fiscalInfo/taxClassificationCodes                       | Listar códigos de classificações tributárias                                    |
| _InformaesFiscaisApi_              | [**listar_codigos_de_operadores_de_indicacoes**](docs/InformaesFiscaisApi.md#listar_codigos_de_operadores_de_indicacoes)                                                                                    | **GET** /v3/fiscalInfo/operationIndicatorCodes                      | Listar códigos de indicadores de operações                                      |
| _InformaesFiscaisApi_              | [**listar_codigos_de_situacoes_tributarias**](docs/InformaesFiscaisApi.md#listar_codigos_de_situacoes_tributarias)                                                                                          | **GET** /v3/fiscalInfo/taxSituationCodes                            | Listar códigos de situações tributárias                                         |
| _InformaesFiscaisApi_              | [**listar_codigos_nbs**](docs/InformaesFiscaisApi.md#listar_codigos_nbs)                                                                                                                                    | **GET** /v3/fiscalInfo/nbsCodes                                     | Listar códigos NBS                                                              |
| _InformaesFiscaisApi_              | [**listar_codigos_servicos_federais**](docs/InformaesFiscaisApi.md#listar_codigos_servicos_federais)                                                                                                        | **GET** /v3/fiscalInfo/federalServiceCodes                          | Listar códigos de serviços federais                                             |
| _InformaesFiscaisApi_              | [**listar_configuracoes_municipais**](docs/InformaesFiscaisApi.md#listar_configuracoes_municipais)                                                                                                          | **GET** /v3/fiscalInfo/municipalOptions                             | Listar configurações municipais                                                 |
| _InformaesFiscaisApi_              | [**listar_servicos_municipais**](docs/InformaesFiscaisApi.md#listar_servicos_municipais)                                                                                                                    | **GET** /v3/fiscalInfo/services                                     | Listar serviços municipais                                                      |
| _InformaesFiscaisApi_              | [**recuperar_informacoes_fiscais**](docs/InformaesFiscaisApi.md#recuperar_informacoes_fiscais)                                                                                                              | **GET** /v3/fiscalInfo/                                             | Recuperar informações fiscais                                                   |
| _LinkDePagamentosApi_              | [**adicionar_uma_imagem_aum_link_de_pagamentos**](docs/LinkDePagamentosApi.md#adicionar_uma_imagem_aum_link_de_pagamentos)                                                                                  | **POST** /v3/paymentLinks/{id}/images                               | Adicionar uma imagem a um link de pagamentos                                    |
| _LinkDePagamentosApi_              | [**atualizar_um_link_de_pagamentos**](docs/LinkDePagamentosApi.md#atualizar_um_link_de_pagamentos)                                                                                                          | **PUT** /v3/paymentLinks/{id}                                       | Atualizar um link de pagamentos                                                 |
| _LinkDePagamentosApi_              | [**criar_um_link_de_pagamentos**](docs/LinkDePagamentosApi.md#criar_um_link_de_pagamentos)                                                                                                                  | **POST** /v3/paymentLinks                                           | Criar um link de pagamentos                                                     |
| _LinkDePagamentosApi_              | [**definir_imagem_principal_do_link_de_pagamentos**](docs/LinkDePagamentosApi.md#definir_imagem_principal_do_link_de_pagamentos)                                                                            | **PUT** /v3/paymentLinks/{paymentLinkId}/images/{imageId}/setAsMain | Definir imagem principal do link de pagamentos                                  |
| _LinkDePagamentosApi_              | [**listar_imagens_de_um_link_de_pagamentos**](docs/LinkDePagamentosApi.md#listar_imagens_de_um_link_de_pagamentos)                                                                                          | **GET** /v3/paymentLinks/{id}/images                                | Listar imagens de um link de pagamentos                                         |
| _LinkDePagamentosApi_              | [**listar_links_de_pagamentos**](docs/LinkDePagamentosApi.md#listar_links_de_pagamentos)                                                                                                                    | **GET** /v3/paymentLinks                                            | Listar links de pagamentos                                                      |
| _LinkDePagamentosApi_              | [**recuperar_um_unico_link_de_pagamentos**](docs/LinkDePagamentosApi.md#recuperar_um_unico_link_de_pagamentos)                                                                                              | **GET** /v3/paymentLinks/{id}                                       | Recuperar um único link de pagamentos                                           |
| _LinkDePagamentosApi_              | [**recuperar_uma_unica_imagem_do_link_de_pagamentos**](docs/LinkDePagamentosApi.md#recuperar_uma_unica_imagem_do_link_de_pagamentos)                                                                        | **GET** /v3/paymentLinks/{paymentLinkId}/images/{imageId}           | Recuperar uma única imagem do link de pagamentos                                |
| _LinkDePagamentosApi_              | [**remover_um_link_de_pagamentos**](docs/LinkDePagamentosApi.md#remover_um_link_de_pagamentos)                                                                                                              | **DELETE** /v3/paymentLinks/{id}                                    | Remover um link de pagamentos                                                   |
| _LinkDePagamentosApi_              | [**remover_uma_imagem_do_link_de_pagamentos**](docs/LinkDePagamentosApi.md#remover_uma_imagem_do_link_de_pagamentos)                                                                                        | **DELETE** /v3/paymentLinks/{paymentLinkId}/images/{imageId}        | Remover uma imagem do link de pagamentos                                        |
| _LinkDePagamentosApi_              | [**restaurar_um_link_de_pagamentos**](docs/LinkDePagamentosApi.md#restaurar_um_link_de_pagamentos)                                                                                                          | **POST** /v3/paymentLinks/{id}/restore                              | Restaurar um link de pagamentos                                                 |
| _NegativaesApi_                    | [**cancelar_negativacao**](docs/NegativaesApi.md#cancelar_negativacao)                                                                                                                                      | **POST** /v3/paymentDunnings/{id}/cancel                            | Cancelar negativação                                                            |
| _NegativaesApi_                    | [**criar_uma_negativacao**](docs/NegativaesApi.md#criar_uma_negativacao)                                                                                                                                    | **POST** /v3/paymentDunnings                                        | Criar uma negativação                                                           |
| _NegativaesApi_                    | [**listar_cobrancas_disponiveis_para_negativacao**](docs/NegativaesApi.md#listar_cobrancas_disponiveis_para_negativacao)                                                                                    | **GET** /v3/paymentDunnings/paymentsAvailableForDunning             | Listar cobranças disponíveis para negativação                                   |
| _NegativaesApi_                    | [**listar_historico_de_eventos**](docs/NegativaesApi.md#listar_historico_de_eventos)                                                                                                                        | **GET** /v3/paymentDunnings/{id}/history                            | Listar histórico de eventos                                                     |
| _NegativaesApi_                    | [**listar_negativacoes**](docs/NegativaesApi.md#listar_negativacoes)                                                                                                                                        | **GET** /v3/paymentDunnings                                         | Listar negativações                                                             |
| _NegativaesApi_                    | [**listar_pagamentos_recebidos**](docs/NegativaesApi.md#listar_pagamentos_recebidos)                                                                                                                        | **GET** /v3/paymentDunnings/{id}/partialPayments                    | Listar pagamentos recebidos                                                     |
| _NegativaesApi_                    | [**recuperar_uma_unica_negativacao**](docs/NegativaesApi.md#recuperar_uma_unica_negativacao)                                                                                                                | **GET** /v3/paymentDunnings/{id}                                    | Recuperar uma única negativação                                                 |
| _NegativaesApi_                    | [**reenviar_documentos**](docs/NegativaesApi.md#reenviar_documentos)                                                                                                                                        | **POST** /v3/paymentDunnings/{id}/documents                         | Reenviar documentos                                                             |
| _NegativaesApi_                    | [**simular_uma_negativacao**](docs/NegativaesApi.md#simular_uma_negativacao)                                                                                                                                | **POST** /v3/paymentDunnings/simulate                               | Simular uma negativação                                                         |
| _NotasFiscaisApi_                  | [**agendar_nota_fiscal**](docs/NotasFiscaisApi.md#agendar_nota_fiscal)                                                                                                                                      | **POST** /v3/invoices                                               | Agendar nota fiscal                                                             |
| _NotasFiscaisApi_                  | [**atualizar_nota_fiscal**](docs/NotasFiscaisApi.md#atualizar_nota_fiscal)                                                                                                                                  | **PUT** /v3/invoices/{id}                                           | Atualizar nota fiscal                                                           |
| _NotasFiscaisApi_                  | [**cancelar_uma_nota_fiscal**](docs/NotasFiscaisApi.md#cancelar_uma_nota_fiscal)                                                                                                                            | **POST** /v3/invoices/{id}/cancel                                   | Cancelar uma nota fiscal                                                        |
| _NotasFiscaisApi_                  | [**emitir_uma_nota_fiscal**](docs/NotasFiscaisApi.md#emitir_uma_nota_fiscal)                                                                                                                                | **POST** /v3/invoices/{id}/authorize                                | Emitir uma nota fiscal                                                          |
| _NotasFiscaisApi_                  | [**listar_notas_fiscais**](docs/NotasFiscaisApi.md#listar_notas_fiscais)                                                                                                                                    | **GET** /v3/invoices                                                | Listar notas fiscais                                                            |
| _NotasFiscaisApi_                  | [**recuperar_uma_nota_fiscal**](docs/NotasFiscaisApi.md#recuperar_uma_nota_fiscal)                                                                                                                          | **GET** /v3/invoices/{id}                                           | Recuperar uma única nota fiscal                                                 |
| _NotificaesApi_                    | [**atualizar_notificacao_existente**](docs/NotificaesApi.md#atualizar_notificacao_existente)                                                                                                                | **PUT** /v3/notifications/{id}                                      | Atualizar notificação existente                                                 |
| _NotificaesApi_                    | [**atualizar_notificacoes_existentes_em_lote**](docs/NotificaesApi.md#atualizar_notificacoes_existentes_em_lote)                                                                                            | **PUT** /v3/notifications/batch                                     | Atualizar notificações existentes em lote                                       |
| _PagamentoDeContasApi_             | [**cancelar_pagamento_de_contas**](docs/PagamentoDeContasApi.md#cancelar_pagamento_de_contas)                                                                                                               | **POST** /v3/bill/{id}/cancel                                       | Cancelar pagamento de contas                                                    |
| _PagamentoDeContasApi_             | [**criar_um_pagamento_de_conta**](docs/PagamentoDeContasApi.md#criar_um_pagamento_de_conta)                                                                                                                 | **POST** /v3/bill                                                   | Criar um pagamento de conta                                                     |
| _PagamentoDeContasApi_             | [**listar_pagamento_de_contas**](docs/PagamentoDeContasApi.md#listar_pagamento_de_contas)                                                                                                                   | **GET** /v3/bill                                                    | Listar pagamento de contas                                                      |
| _PagamentoDeContasApi_             | [**recuperar_um_unico_pagamento_de_conta**](docs/PagamentoDeContasApi.md#recuperar_um_unico_pagamento_de_conta)                                                                                             | **GET** /v3/bill/{id}                                               | Recuperar um único pagamento de conta                                           |
| _PagamentoDeContasApi_             | [**simular_um_pagamento_de_conta**](docs/PagamentoDeContasApi.md#simular_um_pagamento_de_conta)                                                                                                             | **POST** /v3/bill/simulate                                          | Simular um pagamento de conta                                                   |
| _ParcelamentosApi_                 | [**atualizar_splits_do_parcelamento**](docs/ParcelamentosApi.md#atualizar_splits_do_parcelamento)                                                                                                           | **PUT** /v3/installments/{id}/splits                                | Atualizar splits do parcelamento                                                |
| _ParcelamentosApi_                 | [**cancelar_cobrancas_de_um_parcelamento**](docs/ParcelamentosApi.md#cancelar_cobrancas_de_um_parcelamento)                                                                                                 | **DELETE** /v3/installments/{id}/payments                           | Cancelar cobranças de um parcelamento (pendentes e vencidas)                    |
| _ParcelamentosApi_                 | [**criar_parcelamento**](docs/ParcelamentosApi.md#criar_parcelamento)                                                                                                                                       | **POST** /v3/installments                                           | Criar parcelamento                                                              |
| _ParcelamentosApi_                 | [**criar_parcelamento_com_carto_de_crdito**](docs/ParcelamentosApi.md#criar_parcelamento_com_carto_de_crdito)                                                                                               | **POST** /v3/installments/                                          | Criar parcelamento com cartão de crédito                                        |
| _ParcelamentosApi_                 | [**estornar_parcelamento**](docs/ParcelamentosApi.md#estornar_parcelamento)                                                                                                                                 | **POST** /v3/installments/{id}/refund                               | Estornar parcelamento                                                           |
| _ParcelamentosApi_                 | [**gerar_carne_de_parcelamento**](docs/ParcelamentosApi.md#gerar_carne_de_parcelamento)                                                                                                                     | **GET** /v3/installments/{id}/paymentBook                           | Gerar carnê de parcelamento                                                     |
| _ParcelamentosApi_                 | [**listar_cobranas_de_um_parcelamento**](docs/ParcelamentosApi.md#listar_cobranas_de_um_parcelamento)                                                                                                       | **GET** /v3/installments/{id}/payments                              | Listar cobranças de um parcelamento                                             |
| _ParcelamentosApi_                 | [**listar_parcelamentos**](docs/ParcelamentosApi.md#listar_parcelamentos)                                                                                                                                   | **GET** /v3/installments                                            | Listar parcelamentos                                                            |
| _ParcelamentosApi_                 | [**recuperar_um_unico_parcelamento**](docs/ParcelamentosApi.md#recuperar_um_unico_parcelamento)                                                                                                             | **GET** /v3/installments/{id}                                       | Recuperar um único parcelamento                                                 |
| _ParcelamentosApi_                 | [**remover_parcelamento**](docs/ParcelamentosApi.md#remover_parcelamento)                                                                                                                                   | **DELETE** /v3/installments/{id}                                    | Remover parcelamento                                                            |
| _PixApi_                           | [**consulta_de_fichas_disponiveis_no_balde**](docs/PixApi.md#consulta_de_fichas_disponiveis_no_balde)                                                                                                       | **GET** /v3/pix/tokenBucket/addressKey                              | Consulta de fichas disponíveis no balde                                         |
| _PixApi_                           | [**criar_qrcode_estatico**](docs/PixApi.md#criar_qrcode_estatico)                                                                                                                                           | **POST** /v3/pix/qrCodes/static                                     | Criar QR Code estático                                                          |
| _PixApi_                           | [**criar_uma_chave**](docs/PixApi.md#criar_uma_chave)                                                                                                                                                       | **POST** /v3/pix/addressKeys                                        | Criar uma chave                                                                 |
| _PixApi_                           | [**deletar_qrcode_estatico**](docs/PixApi.md#deletar_qrcode_estatico)                                                                                                                                       | **DELETE** /v3/pix/qrCodes/static/{id}                              | Deletar QR Code estático                                                        |
| _PixApi_                           | [**listar_chaves**](docs/PixApi.md#listar_chaves)                                                                                                                                                           | **GET** /v3/pix/addressKeys                                         | Listar chaves                                                                   |
| _PixApi_                           | [**recuperar_uma_unica_chave**](docs/PixApi.md#recuperar_uma_unica_chave)                                                                                                                                   | **GET** /v3/pix/addressKeys/{id}                                    | Recuperar uma única chave                                                       |
| _PixApi_                           | [**remover_chave**](docs/PixApi.md#remover_chave)                                                                                                                                                           | **DELETE** /v3/pix/addressKeys/{id}                                 | Remover chave                                                                   |
| _PixAutomticoApi_                  | [**cancelar_uma_autorizacao_pix_automatico**](docs/PixAutomticoApi.md#cancelar_uma_autorizacao_pix_automatico)                                                                                              | **DELETE** /v3/pix/automatic/authorizations/{id}                    | Cancelar uma autorização                                                        |
| _PixAutomticoApi_                  | [**criar_uma_autorizacao_pix_automatico**](docs/PixAutomticoApi.md#criar_uma_autorizacao_pix_automatico)                                                                                                    | **POST** /v3/pix/automatic/authorizations                           | Criar uma autorização                                                           |
| _PixAutomticoApi_                  | [**listar_autorizacoes_pix_automatico**](docs/PixAutomticoApi.md#listar_autorizacoes_pix_automatico)                                                                                                        | **GET** /v3/pix/automatic/authorizations                            | Listar autorizações                                                             |
| _PixAutomticoApi_                  | [**listar_instrucoes_de_pagamento_pix_automatico**](docs/PixAutomticoApi.md#listar_instrucoes_de_pagamento_pix_automatico)                                                                                  | **GET** /v3/pix/automatic/paymentInstructions                       | Listar instruções de pagamento                                                  |
| _PixAutomticoApi_                  | [**recuperar_uma_unica_autorizacao_pix_automatico**](docs/PixAutomticoApi.md#recuperar_uma_unica_autorizacao_pix_automatico)                                                                                | **GET** /v3/pix/automatic/authorizations/{id}                       | Recuperar uma única autorização                                                 |
| _PixAutomticoApi_                  | [**recuperar_uma_unica_instrucao_de_pagamento_pix_automatico**](docs/PixAutomticoApi.md#recuperar_uma_unica_instrucao_de_pagamento_pix_automatico)                                                          | **GET** /v3/pix/automatic/paymentInstructions/{id}                  | Recuperar uma única instrução de pagamento                                      |
| _PixRecorrenteApi_                 | [**cancelar_item_de_uma_recorrencia**](docs/PixRecorrenteApi.md#cancelar_item_de_uma_recorrencia)                                                                                                           | **POST** /v3/pix/transactions/recurrings/items/{id}/cancel          | Cancelar item de uma recorrência                                                |
| _PixRecorrenteApi_                 | [**cancelar_uma_recorrencia**](docs/PixRecorrenteApi.md#cancelar_uma_recorrencia)                                                                                                                           | **POST** /v3/pix/transactions/recurrings/{id}/cancel                | Cancelar uma recorrência                                                        |
| _PixRecorrenteApi_                 | [**listar_itens_de_uma_recorrencia**](docs/PixRecorrenteApi.md#listar_itens_de_uma_recorrencia)                                                                                                             | **GET** /v3/pix/transactions/recurrings/{id}/items                  | Listar itens de uma recorrência                                                 |
| _PixRecorrenteApi_                 | [**listar_recorrencias**](docs/PixRecorrenteApi.md#listar_recorrencias)                                                                                                                                     | **GET** /v3/pix/transactions/recurrings                             | Listar recorrências                                                             |
| _PixRecorrenteApi_                 | [**recuperar_uma_unica_recorrencia**](docs/PixRecorrenteApi.md#recuperar_uma_unica_recorrencia)                                                                                                             | **GET** /v3/pix/transactions/recurrings/{id}                        | Recuperar uma única recorrência                                                 |
| _RecargasDeCelularApi_             | [**buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga**](docs/RecargasDeCelularApi.md#buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga)                 | **GET** /v3/mobilePhoneRecharges/{phoneNumber}/provider             | Buscar qual provedor o número pertence e os valores disponíveis para recarga    |
| _RecargasDeCelularApi_             | [**cancelar_uma_recarga_de_celular**](docs/RecargasDeCelularApi.md#cancelar_uma_recarga_de_celular)                                                                                                         | **POST** /v3/mobilePhoneRecharges/{id}/cancel                       | Cancelar uma recarga de celular                                                 |
| _RecargasDeCelularApi_             | [**listar_recargas_de_celular**](docs/RecargasDeCelularApi.md#listar_recargas_de_celular)                                                                                                                   | **GET** /v3/mobilePhoneRecharges                                    | Listar recargas de celular                                                      |
| _RecargasDeCelularApi_             | [**recuperar_uma_unica_recarga_de_celular**](docs/RecargasDeCelularApi.md#recuperar_uma_unica_recarga_de_celular)                                                                                           | **GET** /v3/mobilePhoneRecharges/{id}                               | Recuperar uma única recarga de celular                                          |
| _RecargasDeCelularApi_             | [**solicitar_recarga**](docs/RecargasDeCelularApi.md#solicitar_recarga)                                                                                                                                     | **POST** /v3/mobilePhoneRecharges                                   | Solicitar recarga                                                               |
| _SplitsApi_                        | [**listar_splits_pagos**](docs/SplitsApi.md#listar_splits_pagos)                                                                                                                                            | **GET** /v3/payments/splits/paid                                    | Listar splits pagos                                                             |
| _SplitsApi_                        | [**listar_splits_recebidos**](docs/SplitsApi.md#listar_splits_recebidos)                                                                                                                                    | **GET** /v3/payments/splits/received                                | Listar splits recebidos                                                         |
| _SplitsApi_                        | [**recuperar_um_unico_split_pago**](docs/SplitsApi.md#recuperar_um_unico_split_pago)                                                                                                                        | **GET** /v3/payments/splits/paid/{id}                               | Recuperar um único split pago                                                   |
| _SplitsApi_                        | [**recuperar_um_unico_split_recebido**](docs/SplitsApi.md#recuperar_um_unico_split_recebido)                                                                                                                | **GET** /v3/payments/splits/received/{id}                           | Recuperar um único split recebido                                               |
| _SubcontasAsaasApi_                | [**atualizar_chave_de_api_de_uma_subconta**](docs/SubcontasAsaasApi.md#atualizar_chave_de_api_de_uma_subconta)                                                                                              | **PUT** /v3/accounts/{id}/accessTokens/{accessTokenId}              | Atualizar chave de API de uma subconta                                          |
| _SubcontasAsaasApi_                | [**criar_chave_de_api_para_uma_subconta**](docs/SubcontasAsaasApi.md#criar_chave_de_api_para_uma_subconta)                                                                                                  | **POST** /v3/accounts/{id}/accessTokens                             | Criar chave de API para uma subconta                                            |
| _SubcontasAsaasApi_                | [**criar_subconta**](docs/SubcontasAsaasApi.md#criar_subconta)                                                                                                                                              | **POST** /v3/accounts                                               | Criar subconta                                                                  |
| _SubcontasAsaasApi_                | [**excluir_chave_de_api_de_uma_subconta**](docs/SubcontasAsaasApi.md#excluir_chave_de_api_de_uma_subconta)                                                                                                  | **DELETE** /v3/accounts/{id}/accessTokens/{accessTokenId}           | Excluir chave de API de uma subconta                                            |
| _SubcontasAsaasApi_                | [**listar_chaves_de_api_de_uma_subconta**](docs/SubcontasAsaasApi.md#listar_chaves_de_api_de_uma_subconta)                                                                                                  | **GET** /v3/accounts/{id}/accessTokens                              | Listar chaves de API de uma subconta                                            |
| _SubcontasAsaasApi_                | [**listar_subcontas**](docs/SubcontasAsaasApi.md#listar_subcontas)                                                                                                                                          | **GET** /v3/accounts                                                | Listar subcontas                                                                |
| _SubcontasAsaasApi_                | [**recuperar_uma_unica_subconta**](docs/SubcontasAsaasApi.md#recuperar_uma_unica_subconta)                                                                                                                  | **GET** /v3/accounts/{id}                                           | Recuperar uma única subconta                                                    |
| _TransaesPixApi_                   | [**cancelar_uma_transacao_agendada**](docs/TransaesPixApi.md#cancelar_uma_transacao_agendada)                                                                                                               | **POST** /v3/pix/transactions/{id}/cancel                           | Cancelar uma transação agendada                                                 |
| _TransaesPixApi_                   | [**decodificar_um_qrcode_para_pagamento**](docs/TransaesPixApi.md#decodificar_um_qrcode_para_pagamento)                                                                                                     | **POST** /v3/pix/qrCodes/decode                                     | Decodificar um QRCode para pagamento                                            |
| _TransaesPixApi_                   | [**listar_transacoes**](docs/TransaesPixApi.md#listar_transacoes)                                                                                                                                           | **GET** /v3/pix/transactions                                        | Listar transações                                                               |
| _TransaesPixApi_                   | [**pagar_um_qrcode**](docs/TransaesPixApi.md#pagar_um_qrcode)                                                                                                                                               | **POST** /v3/pix/qrCodes/pay                                        | Pagar um QRCode                                                                 |
| _TransaesPixApi_                   | [**recuperar_uma_unica_transacao**](docs/TransaesPixApi.md#recuperar_uma_unica_transacao)                                                                                                                   | **GET** /v3/pix/transactions/{id}                                   | Recuperar uma única transação                                                   |
| _TransfernciasApi_                 | [**cancelar_uma_transferncia**](docs/TransfernciasApi.md#cancelar_uma_transferncia)                                                                                                                         | **DELETE** /v3/transfers/{id}/cancel                                | Cancelar uma transferência                                                      |
| _TransfernciasApi_                 | [**listar_transferencias**](docs/TransfernciasApi.md#listar_transferencias)                                                                                                                                 | **GET** /v3/transfers                                               | Listar transferências                                                           |
| _TransfernciasApi_                 | [**recuperar_uma_unica_transferencia**](docs/TransfernciasApi.md#recuperar_uma_unica_transferencia)                                                                                                         | **GET** /v3/transfers/{id}                                          | Recuperar uma única transferência                                               |
| _TransfernciasApi_                 | [**transferir_para_conta_asaas**](docs/TransfernciasApi.md#transferir_para_conta_asaas)                                                                                                                     | **POST** /v3/transfers/                                             | Transferir para conta Asaas                                                     |
| _TransfernciasApi_                 | [**transferir_para_conta_de_outra_instituicao_ou_chave_pix**](docs/TransfernciasApi.md#transferir_para_conta_de_outra_instituicao_ou_chave_pix)                                                             | **POST** /v3/transfers                                              | Transferir para conta de outra Instituição ou chave Pix                         |

## Documentation For Models

- [AccountDocumentDeleteResponseDTO](docs/AccountDocumentDeleteResponseDTO.md)
- [AccountDocumentGetResponseAccountDocumentStatus](docs/AccountDocumentGetResponseAccountDocumentStatus.md)
- [AccountDocumentGetResponseDTO](docs/AccountDocumentGetResponseDTO.md)
- [AccountDocumentGroupResponseAccountDocumentStatus](docs/AccountDocumentGroupResponseAccountDocumentStatus.md)
- [AccountDocumentGroupResponseAccountDocumentType](docs/AccountDocumentGroupResponseAccountDocumentType.md)
- [AccountDocumentGroupResponseDTO](docs/AccountDocumentGroupResponseDTO.md)
- [AccountDocumentResponsibleResponseAccountDocumentResponsibleType](docs/AccountDocumentResponsibleResponseAccountDocumentResponsibleType.md)
- [AccountDocumentResponsibleResponseDTO](docs/AccountDocumentResponsibleResponseDTO.md)
- [AccountDocumentSaveRequestAccountDocumentType](docs/AccountDocumentSaveRequestAccountDocumentType.md)
- [AccountDocumentShowResponseDTO](docs/AccountDocumentShowResponseDTO.md)
- [AccountGetResponseCompanyType](docs/AccountGetResponseCompanyType.md)
- [AccountGetResponseDTO](docs/AccountGetResponseDTO.md)
- [AccountGetResponsePersonType](docs/AccountGetResponsePersonType.md)
- [AccountInfoCityDTO](docs/AccountInfoCityDTO.md)
- [AccountInfoCityState](docs/AccountInfoCityState.md)
- [AccountInfoCommercialInfoExpirationResponseDTO](docs/AccountInfoCommercialInfoExpirationResponseDTO.md)
- [AccountInfoGetResponseCompanyType](docs/AccountInfoGetResponseCompanyType.md)
- [AccountInfoGetResponseDTO](docs/AccountInfoGetResponseDTO.md)
- [AccountInfoGetResponsePersonType](docs/AccountInfoGetResponsePersonType.md)
- [AccountInfoGetResponseStatus](docs/AccountInfoGetResponseStatus.md)
- [AccountInfoSaveRequestCompanyType](docs/AccountInfoSaveRequestCompanyType.md)
- [AccountInfoSaveRequestDTO](docs/AccountInfoSaveRequestDTO.md)
- [AccountInfoSaveRequestPersonType](docs/AccountInfoSaveRequestPersonType.md)
- [AccountListResponseDTO](docs/AccountListResponseDTO.md)
- [AccountNumberDTO](docs/AccountNumberDTO.md)
- [AccountPaymentEscrowConfigDTO](docs/AccountPaymentEscrowConfigDTO.md)
- [AccountSaveOrUpdatePaymentEscrowConfigRequestDTO](docs/AccountSaveOrUpdatePaymentEscrowConfigRequestDTO.md)
- [AccountSaveRequestCompanyType](docs/AccountSaveRequestCompanyType.md)
- [AccountSaveRequestDTO](docs/AccountSaveRequestDTO.md)
- [AccountSaveResponseCompanyType](docs/AccountSaveResponseCompanyType.md)
- [AccountSaveResponseDTO](docs/AccountSaveResponseDTO.md)
- [AccountSaveResponsePersonType](docs/AccountSaveResponsePersonType.md)
- [AnticipationConfigurationGetResponseDTO](docs/AnticipationConfigurationGetResponseDTO.md)
- [AnticipationConfigurationUpdateRequestDTO](docs/AnticipationConfigurationUpdateRequestDTO.md)
- [AnticipationGetResponseAnticipationStatus](docs/AnticipationGetResponseAnticipationStatus.md)
- [AnticipationGetResponseDTO](docs/AnticipationGetResponseDTO.md)
- [AnticipationLimitsInfoResponseDTO](docs/AnticipationLimitsInfoResponseDTO.md)
- [AnticipationLimitsResponseDTO](docs/AnticipationLimitsResponseDTO.md)
- [AnticipationListRequestAnticipationStatus](docs/AnticipationListRequestAnticipationStatus.md)
- [AnticipationListResponseDTO](docs/AnticipationListResponseDTO.md)
- [AnticipationSimulateRequestDTO](docs/AnticipationSimulateRequestDTO.md)
- [AnticipationSimulateResponseDTO](docs/AnticipationSimulateResponseDTO.md)
- [BankSlipBillingInfoResponseDTO](docs/BankSlipBillingInfoResponseDTO.md)
- [BillGetResponseBillStatus](docs/BillGetResponseBillStatus.md)
- [BillGetResponseDTO](docs/BillGetResponseDTO.md)
- [BillListResponseDTO](docs/BillListResponseDTO.md)
- [BillSaveRequestDTO](docs/BillSaveRequestDTO.md)
- [BillSimulateBankSlipInfoResponseDTO](docs/BillSimulateBankSlipInfoResponseDTO.md)
- [BillSimulateRequestDTO](docs/BillSimulateRequestDTO.md)
- [BillSimulateResponseDTO](docs/BillSimulateResponseDTO.md)
- [ChargebackCreditCardResponseCreditCardBrand](docs/ChargebackCreditCardResponseCreditCardBrand.md)
- [ChargebackCreditCardResponseDTO](docs/ChargebackCreditCardResponseDTO.md)
- [ChargebackListRequestChargebackStatus](docs/ChargebackListRequestChargebackStatus.md)
- [ChargebackListRequestCreditCardBrand](docs/ChargebackListRequestCreditCardBrand.md)
- [ChargebackListResponseDTO](docs/ChargebackListResponseDTO.md)
- [ChargebackSaveDisputeResponseChargebackDisputeStatus](docs/ChargebackSaveDisputeResponseChargebackDisputeStatus.md)
- [ChargebackSaveDisputeResponseDTO](docs/ChargebackSaveDisputeResponseDTO.md)
- [CheckoutSessionCallbackDTO](docs/CheckoutSessionCallbackDTO.md)
- [CheckoutSessionCustomerDataDTO](docs/CheckoutSessionCustomerDataDTO.md)
- [CheckoutSessionInstallmentDTO](docs/CheckoutSessionInstallmentDTO.md)
- [CheckoutSessionItemsDTO](docs/CheckoutSessionItemsDTO.md)
- [CheckoutSessionResponseBillingType](docs/CheckoutSessionResponseBillingType.md)
- [CheckoutSessionResponseChargeType](docs/CheckoutSessionResponseChargeType.md)
- [CheckoutSessionResponseDTO](docs/CheckoutSessionResponseDTO.md)
- [CheckoutSessionSaveRequestBillingType](docs/CheckoutSessionSaveRequestBillingType.md)
- [CheckoutSessionSaveRequestChargeType](docs/CheckoutSessionSaveRequestChargeType.md)
- [CheckoutSessionSaveRequestDTO](docs/CheckoutSessionSaveRequestDTO.md)
- [CheckoutSessionSplitDTO](docs/CheckoutSessionSplitDTO.md)
- [CheckoutSessionSubscriptionCycle](docs/CheckoutSessionSubscriptionCycle.md)
- [CheckoutSessionSubscriptionDTO](docs/CheckoutSessionSubscriptionDTO.md)
- [CreditBureauReportGetResponseDTO](docs/CreditBureauReportGetResponseDTO.md)
- [CreditBureauReportListResponseDTO](docs/CreditBureauReportListResponseDTO.md)
- [CreditBureauReportSaveRequestDTO](docs/CreditBureauReportSaveRequestDTO.md)
- [CreditCardHolderInfoRequestDTO](docs/CreditCardHolderInfoRequestDTO.md)
- [CreditCardPreAuthorizationConfigRequestDTO](docs/CreditCardPreAuthorizationConfigRequestDTO.md)
- [CreditCardPreAuthorizationConfigResponseDTO](docs/CreditCardPreAuthorizationConfigResponseDTO.md)
- [CreditCardRequestDTO](docs/CreditCardRequestDTO.md)
- [CreditCardTokenizeRequestDTO](docs/CreditCardTokenizeRequestDTO.md)
- [CreditCardTokenizeResponseCreditCardBrand](docs/CreditCardTokenizeResponseCreditCardBrand.md)
- [CreditCardTokenizeResponseDTO](docs/CreditCardTokenizeResponseDTO.md)
- [CustomerApiAccessTokenBaseResponseDTO](docs/CustomerApiAccessTokenBaseResponseDTO.md)
- [CustomerApiAccessTokenListResponseDTO](docs/CustomerApiAccessTokenListResponseDTO.md)
- [CustomerApiAccessTokenSaveRequestDTO](docs/CustomerApiAccessTokenSaveRequestDTO.md)
- [CustomerApiAccessTokenSaveResponseDTO](docs/CustomerApiAccessTokenSaveResponseDTO.md)
- [CustomerApiAccessTokenUpdateRequestDTO](docs/CustomerApiAccessTokenUpdateRequestDTO.md)
- [CustomerDeleteResponseDTO](docs/CustomerDeleteResponseDTO.md)
- [CustomerGetResponseDTO](docs/CustomerGetResponseDTO.md)
- [CustomerGetResponsePersonType](docs/CustomerGetResponsePersonType.md)
- [CustomerListResponseDTO](docs/CustomerListResponseDTO.md)
- [CustomerSaveRequestDTO](docs/CustomerSaveRequestDTO.md)
- [CustomerUpdateRequestDTO](docs/CustomerUpdateRequestDTO.md)
- [ErrorResponseDTO](docs/ErrorResponseDTO.md)
- [ErrorResponseItemDTO](docs/ErrorResponseItemDTO.md)
- [FinanceBalanceResponseDTO](docs/FinanceBalanceResponseDTO.md)
- [FinanceGetPaymentStatisticsRequestBillingType](docs/FinanceGetPaymentStatisticsRequestBillingType.md)
- [FinanceGetPaymentStatisticsRequestPaymentStatus](docs/FinanceGetPaymentStatisticsRequestPaymentStatus.md)
- [FinanceGetPaymentStatisticsResponseDTO](docs/FinanceGetPaymentStatisticsResponseDTO.md)
- [FinanceGetSplitStatisticsResponseDTO](docs/FinanceGetSplitStatisticsResponseDTO.md)
- [FinancialTransactionGetResponseDTO](docs/FinancialTransactionGetResponseDTO.md)
- [FinancialTransactionGetResponseFinancialTransactionType](docs/FinancialTransactionGetResponseFinancialTransactionType.md)
- [FinancialTransactionListResponseDTO](docs/FinancialTransactionListResponseDTO.md)
- [FiscalInfoFederalServiceCodeListResponseDTO](docs/FiscalInfoFederalServiceCodeListResponseDTO.md)
- [FiscalInfoFederalServiceCodeResponseDTO](docs/FiscalInfoFederalServiceCodeResponseDTO.md)
- [FiscalInfoGetResponseDTO](docs/FiscalInfoGetResponseDTO.md)
- [FiscalInfoListInvoiceNbsCodesResponseDTO](docs/FiscalInfoListInvoiceNbsCodesResponseDTO.md)
- [FiscalInfoListInvoiceNbsCodesResponseDataDTO](docs/FiscalInfoListInvoiceNbsCodesResponseDataDTO.md)
- [FiscalInfoListMunicipalServicesResponseDTO](docs/FiscalInfoListMunicipalServicesResponseDTO.md)
- [FiscalInfoListMunicipalServicesResponseDataDTO](docs/FiscalInfoListMunicipalServicesResponseDataDTO.md)
- [FiscalInfoMunicipalOptionsGetResponseDTO](docs/FiscalInfoMunicipalOptionsGetResponseDTO.md)
- [FiscalInfoMunicipalOptionsGetResponseEnotasTipoAutenticacao](docs/FiscalInfoMunicipalOptionsGetResponseEnotasTipoAutenticacao.md)
- [FiscalInfoMunicipalOptionsNationalPortalTaxCalculationRegimeDTO](docs/FiscalInfoMunicipalOptionsNationalPortalTaxCalculationRegimeDTO.md)
- [FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO](docs/FiscalInfoMunicipalOptionsSpecialTaxRegimesDTO.md)
- [FiscalInfoOperationIndicatorCodeListResponseDTO](docs/FiscalInfoOperationIndicatorCodeListResponseDTO.md)
- [FiscalInfoOperationIndicatorCodeResponseDTO](docs/FiscalInfoOperationIndicatorCodeResponseDTO.md)
- [FiscalInfoTaxClassificationCodeListResponseDTO](docs/FiscalInfoTaxClassificationCodeListResponseDTO.md)
- [FiscalInfoTaxClassificationCodeResponseDTO](docs/FiscalInfoTaxClassificationCodeResponseDTO.md)
- [FiscalInfoTaxSituationCodeListResponseDTO](docs/FiscalInfoTaxSituationCodeListResponseDTO.md)
- [FiscalInfoTaxSituationCodeResponseDTO](docs/FiscalInfoTaxSituationCodeResponseDTO.md)
- [FiscalInfoUpdateUseNationalPortalRequestDTO](docs/FiscalInfoUpdateUseNationalPortalRequestDTO.md)
- [FiscalInfoUpdateUseNationalPortalResponseDTO](docs/FiscalInfoUpdateUseNationalPortalResponseDTO.md)
- [InstallmentDeletePaymentsResponseDTO](docs/InstallmentDeletePaymentsResponseDTO.md)
- [InstallmentDeleteResponseDTO](docs/InstallmentDeleteResponseDTO.md)
- [InstallmentGetResponseBillingType](docs/InstallmentGetResponseBillingType.md)
- [InstallmentGetResponseDTO](docs/InstallmentGetResponseDTO.md)
- [InstallmentListPaymentsRequestPaymentStatus](docs/InstallmentListPaymentsRequestPaymentStatus.md)
- [InstallmentListResponseDTO](docs/InstallmentListResponseDTO.md)
- [InstallmentPaymentDeletedDTO](docs/InstallmentPaymentDeletedDTO.md)
- [InstallmentRefundRequestDTO](docs/InstallmentRefundRequestDTO.md)
- [InstallmentRefundResponseDTO](docs/InstallmentRefundResponseDTO.md)
- [InstallmentRefundResponsePaymentRefundStatus](docs/InstallmentRefundResponsePaymentRefundStatus.md)
- [InstallmentSaveRequestBillingType](docs/InstallmentSaveRequestBillingType.md)
- [InstallmentSaveRequestDTO](docs/InstallmentSaveRequestDTO.md)
- [InstallmentSaveWithCreditCardRequestBillingType](docs/InstallmentSaveWithCreditCardRequestBillingType.md)
- [InstallmentSaveWithCreditCardRequestDTO](docs/InstallmentSaveWithCreditCardRequestDTO.md)
- [InstallmentSplitGetResponseDTO](docs/InstallmentSplitGetResponseDTO.md)
- [InstallmentSplitGetResponsePaymentSplitCancellationReason](docs/InstallmentSplitGetResponsePaymentSplitCancellationReason.md)
- [InstallmentSplitGetResponsePaymentSplitStatus](docs/InstallmentSplitGetResponsePaymentSplitStatus.md)
- [InstallmentSplitRequestDTO](docs/InstallmentSplitRequestDTO.md)
- [InstallmentUpdateSplitRequestDTO](docs/InstallmentUpdateSplitRequestDTO.md)
- [InstallmentUpdateSplitResponseDTO](docs/InstallmentUpdateSplitResponseDTO.md)
- [InvoiceCancelRequestDTO](docs/InvoiceCancelRequestDTO.md)
- [InvoiceGetResponseDTO](docs/InvoiceGetResponseDTO.md)
- [InvoiceGetResponseInvoiceStatus](docs/InvoiceGetResponseInvoiceStatus.md)
- [InvoiceListRequestInvoiceStatus](docs/InvoiceListRequestInvoiceStatus.md)
- [InvoiceListResponseDTO](docs/InvoiceListResponseDTO.md)
- [InvoiceSaveRequestDTO](docs/InvoiceSaveRequestDTO.md)
- [InvoiceTaxesDTO](docs/InvoiceTaxesDTO.md)
- [InvoiceTaxesRequestDTO](docs/InvoiceTaxesRequestDTO.md)
- [InvoiceTaxesResponseDTO](docs/InvoiceTaxesResponseDTO.md)
- [InvoiceUpdateRequestDTO](docs/InvoiceUpdateRequestDTO.md)
- [MobilePhoneRechargeFindProviderResponseDTO](docs/MobilePhoneRechargeFindProviderResponseDTO.md)
- [MobilePhoneRechargeFindProviderResponseValuesDTO](docs/MobilePhoneRechargeFindProviderResponseValuesDTO.md)
- [MobilePhoneRechargeGetResponseDTO](docs/MobilePhoneRechargeGetResponseDTO.md)
- [MobilePhoneRechargeGetResponseMobilePhoneRechargeStatus](docs/MobilePhoneRechargeGetResponseMobilePhoneRechargeStatus.md)
- [MobilePhoneRechargeListResponseDTO](docs/MobilePhoneRechargeListResponseDTO.md)
- [MobilePhoneRechargeSaveRequestDTO](docs/MobilePhoneRechargeSaveRequestDTO.md)
- [MyAccountDisableAccountResponseDTO](docs/MyAccountDisableAccountResponseDTO.md)
- [MyAccountGetAccountFeesAnticipationBankSlipDTO](docs/MyAccountGetAccountFeesAnticipationBankSlipDTO.md)
- [MyAccountGetAccountFeesAnticipationCreditCardDTO](docs/MyAccountGetAccountFeesAnticipationCreditCardDTO.md)
- [MyAccountGetAccountFeesAnticipationDTO](docs/MyAccountGetAccountFeesAnticipationDTO.md)
- [MyAccountGetAccountFeesCreditBureauReportDTO](docs/MyAccountGetAccountFeesCreditBureauReportDTO.md)
- [MyAccountGetAccountFeesInvoiceDTO](docs/MyAccountGetAccountFeesInvoiceDTO.md)
- [MyAccountGetAccountFeesNotificationDTO](docs/MyAccountGetAccountFeesNotificationDTO.md)
- [MyAccountGetAccountFeesPaymentBankSlipDTO](docs/MyAccountGetAccountFeesPaymentBankSlipDTO.md)
- [MyAccountGetAccountFeesPaymentCreditCardDTO](docs/MyAccountGetAccountFeesPaymentCreditCardDTO.md)
- [MyAccountGetAccountFeesPaymentDTO](docs/MyAccountGetAccountFeesPaymentDTO.md)
- [MyAccountGetAccountFeesPaymentDebitCardDTO](docs/MyAccountGetAccountFeesPaymentDebitCardDTO.md)
- [MyAccountGetAccountFeesPaymentDunningDTO](docs/MyAccountGetAccountFeesPaymentDunningDTO.md)
- [MyAccountGetAccountFeesPaymentPixDTO](docs/MyAccountGetAccountFeesPaymentPixDTO.md)
- [MyAccountGetAccountFeesResponseDTO](docs/MyAccountGetAccountFeesResponseDTO.md)
- [MyAccountGetAccountFeesTransferDTO](docs/MyAccountGetAccountFeesTransferDTO.md)
- [MyAccountGetAccountFeesTransferPixDTO](docs/MyAccountGetAccountFeesTransferPixDTO.md)
- [MyAccountGetAccountFeesTransferTedDTO](docs/MyAccountGetAccountFeesTransferTedDTO.md)
- [MyAccountGetAccountNumberResponseDTO](docs/MyAccountGetAccountNumberResponseDTO.md)
- [MyAccountGetStatusResponseDTO](docs/MyAccountGetStatusResponseDTO.md)
- [MyAccountGetStatusResponseStatus](docs/MyAccountGetStatusResponseStatus.md)
- [NotificationBatchUpdateItemRequestDTO](docs/NotificationBatchUpdateItemRequestDTO.md)
- [NotificationBatchUpdateRequestDTO](docs/NotificationBatchUpdateRequestDTO.md)
- [NotificationBatchUpdateResponseDTO](docs/NotificationBatchUpdateResponseDTO.md)
- [NotificationGetResponseDTO](docs/NotificationGetResponseDTO.md)
- [NotificationGetResponseNotificationEvent](docs/NotificationGetResponseNotificationEvent.md)
- [NotificationListResponseDTO](docs/NotificationListResponseDTO.md)
- [NotificationUpdateRequestDTO](docs/NotificationUpdateRequestDTO.md)
- [PaymentBankSlipRefundResponseDTO](docs/PaymentBankSlipRefundResponseDTO.md)
- [PaymentBillingInfoResponseDTO](docs/PaymentBillingInfoResponseDTO.md)
- [PaymentCallbackRequestDTO](docs/PaymentCallbackRequestDTO.md)
- [PaymentChargebackResponseChargebackDisputeStatus](docs/PaymentChargebackResponseChargebackDisputeStatus.md)
- [PaymentChargebackResponseChargebackReason](docs/PaymentChargebackResponseChargebackReason.md)
- [PaymentChargebackResponseChargebackStatus](docs/PaymentChargebackResponseChargebackStatus.md)
- [PaymentChargebackResponseDTO](docs/PaymentChargebackResponseDTO.md)
- [PaymentCheckoutConfigGetResponseDTO](docs/PaymentCheckoutConfigGetResponseDTO.md)
- [PaymentCheckoutConfigGetResponseInvoiceConfigStatus](docs/PaymentCheckoutConfigGetResponseInvoiceConfigStatus.md)
- [PaymentDeleteResponseDTO](docs/PaymentDeleteResponseDTO.md)
- [PaymentDiscountDTO](docs/PaymentDiscountDTO.md)
- [PaymentDiscountDiscountType](docs/PaymentDiscountDiscountType.md)
- [PaymentDocumentDeleteResponseDTO](docs/PaymentDocumentDeleteResponseDTO.md)
- [PaymentDocumentFileResponseDTO](docs/PaymentDocumentFileResponseDTO.md)
- [PaymentDocumentGetResponseDTO](docs/PaymentDocumentGetResponseDTO.md)
- [PaymentDocumentGetResponsePaymentDocumentType](docs/PaymentDocumentGetResponsePaymentDocumentType.md)
- [PaymentDocumentListResponseDTO](docs/PaymentDocumentListResponseDTO.md)
- [PaymentDocumentSaveRequestPaymentDocumentType](docs/PaymentDocumentSaveRequestPaymentDocumentType.md)
- [PaymentDocumentUpdateRequestDTO](docs/PaymentDocumentUpdateRequestDTO.md)
- [PaymentDocumentUpdateRequestPaymentDocumentType](docs/PaymentDocumentUpdateRequestPaymentDocumentType.md)
- [PaymentDunningCancelResponseDTO](docs/PaymentDunningCancelResponseDTO.md)
- [PaymentDunningCancelResponsePaymentDunningStatus](docs/PaymentDunningCancelResponsePaymentDunningStatus.md)
- [PaymentDunningCancelResponsePaymentDunningType](docs/PaymentDunningCancelResponsePaymentDunningType.md)
- [PaymentDunningListHistoryResponseDTO](docs/PaymentDunningListHistoryResponseDTO.md)
- [PaymentDunningListHistoryResponseDataDTO](docs/PaymentDunningListHistoryResponseDataDTO.md)
- [PaymentDunningListHistoryResponseDataPaymentDunningHistoryStatus](docs/PaymentDunningListHistoryResponseDataPaymentDunningHistoryStatus.md)
- [PaymentDunningListPartialPaymentsResponseDTO](docs/PaymentDunningListPartialPaymentsResponseDTO.md)
- [PaymentDunningListPartialPaymentsResponseDataDTO](docs/PaymentDunningListPartialPaymentsResponseDataDTO.md)
- [PaymentDunningListRequestPaymentDunningStatus](docs/PaymentDunningListRequestPaymentDunningStatus.md)
- [PaymentDunningListRequestPaymentDunningType](docs/PaymentDunningListRequestPaymentDunningType.md)
- [PaymentDunningListResponseDTO](docs/PaymentDunningListResponseDTO.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDTO](docs/PaymentDunningPaymentsAvailableForDunningResponseDTO.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataBillingType](docs/PaymentDunningPaymentsAvailableForDunningResponseDataBillingType.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataDTO](docs/PaymentDunningPaymentsAvailableForDunningResponseDataDTO.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataPaymentStatus](docs/PaymentDunningPaymentsAvailableForDunningResponseDataPaymentStatus.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO](docs/PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO.md)
- [PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemPaymentDunningType](docs/PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemPaymentDunningType.md)
- [PaymentDunningSaveDocumentsResponseDTO](docs/PaymentDunningSaveDocumentsResponseDTO.md)
- [PaymentDunningSaveDocumentsResponsePaymentDunningStatus](docs/PaymentDunningSaveDocumentsResponsePaymentDunningStatus.md)
- [PaymentDunningSaveDocumentsResponsePaymentDunningType](docs/PaymentDunningSaveDocumentsResponsePaymentDunningType.md)
- [PaymentDunningSaveRequestPaymentDunningType](docs/PaymentDunningSaveRequestPaymentDunningType.md)
- [PaymentDunningShowResponseDTO](docs/PaymentDunningShowResponseDTO.md)
- [PaymentDunningShowResponsePaymentDunningStatus](docs/PaymentDunningShowResponsePaymentDunningStatus.md)
- [PaymentDunningShowResponsePaymentDunningType](docs/PaymentDunningShowResponsePaymentDunningType.md)
- [PaymentDunningSimulateResponseDTO](docs/PaymentDunningSimulateResponseDTO.md)
- [PaymentDunningSimulateResponseTypeSimulationItemDTO](docs/PaymentDunningSimulateResponseTypeSimulationItemDTO.md)
- [PaymentDunningSimulateResponseTypeSimulationItemPaymentDunningType](docs/PaymentDunningSimulateResponseTypeSimulationItemPaymentDunningType.md)
- [PaymentEscrowGetResponseDTO](docs/PaymentEscrowGetResponseDTO.md)
- [PaymentEscrowGetResponsePaymentEscrowFinishReason](docs/PaymentEscrowGetResponsePaymentEscrowFinishReason.md)
- [PaymentEscrowGetResponsePaymentEscrowStatus](docs/PaymentEscrowGetResponsePaymentEscrowStatus.md)
- [PaymentFineRequestDTO](docs/PaymentFineRequestDTO.md)
- [PaymentFineRequestFineType](docs/PaymentFineRequestFineType.md)
- [PaymentFineResponseDTO](docs/PaymentFineResponseDTO.md)
- [PaymentGetResponseBillingType](docs/PaymentGetResponseBillingType.md)
- [PaymentGetResponseDTO](docs/PaymentGetResponseDTO.md)
- [PaymentGetResponsePaymentStatus](docs/PaymentGetResponsePaymentStatus.md)
- [PaymentIdentificationFieldResponseDTO](docs/PaymentIdentificationFieldResponseDTO.md)
- [PaymentInterestRequestDTO](docs/PaymentInterestRequestDTO.md)
- [PaymentInterestResponseDTO](docs/PaymentInterestResponseDTO.md)
- [PaymentLeanGetResponseBillingType](docs/PaymentLeanGetResponseBillingType.md)
- [PaymentLeanGetResponseDTO](docs/PaymentLeanGetResponseDTO.md)
- [PaymentLeanGetResponsePaymentStatus](docs/PaymentLeanGetResponsePaymentStatus.md)
- [PaymentLeanListResponseDTO](docs/PaymentLeanListResponseDTO.md)
- [PaymentLeanSaveWithCreditCardResponseBillingType](docs/PaymentLeanSaveWithCreditCardResponseBillingType.md)
- [PaymentLeanSaveWithCreditCardResponseDTO](docs/PaymentLeanSaveWithCreditCardResponseDTO.md)
- [PaymentLeanSaveWithCreditCardResponsePaymentStatus](docs/PaymentLeanSaveWithCreditCardResponsePaymentStatus.md)
- [PaymentLimitsResponseCreationDTO](docs/PaymentLimitsResponseCreationDTO.md)
- [PaymentLimitsResponseCreationDailyDTO](docs/PaymentLimitsResponseCreationDailyDTO.md)
- [PaymentLimitsResponseDTO](docs/PaymentLimitsResponseDTO.md)
- [PaymentLinkDeleteResponseDTO](docs/PaymentLinkDeleteResponseDTO.md)
- [PaymentLinkFileDeleteResponseDTO](docs/PaymentLinkFileDeleteResponseDTO.md)
- [PaymentLinkFileGetResponseDTO](docs/PaymentLinkFileGetResponseDTO.md)
- [PaymentLinkFileImageResponseDTO](docs/PaymentLinkFileImageResponseDTO.md)
- [PaymentLinkFileListResponseDTO](docs/PaymentLinkFileListResponseDTO.md)
- [PaymentLinkGetResponseBillingType](docs/PaymentLinkGetResponseBillingType.md)
- [PaymentLinkGetResponseChargeType](docs/PaymentLinkGetResponseChargeType.md)
- [PaymentLinkGetResponseCycle](docs/PaymentLinkGetResponseCycle.md)
- [PaymentLinkGetResponseDTO](docs/PaymentLinkGetResponseDTO.md)
- [PaymentLinkListResponseDTO](docs/PaymentLinkListResponseDTO.md)
- [PaymentLinkSaveRequestBillingType](docs/PaymentLinkSaveRequestBillingType.md)
- [PaymentLinkSaveRequestChargeType](docs/PaymentLinkSaveRequestChargeType.md)
- [PaymentLinkSaveRequestCycle](docs/PaymentLinkSaveRequestCycle.md)
- [PaymentLinkSaveRequestDTO](docs/PaymentLinkSaveRequestDTO.md)
- [PaymentLinkUpdateRequestBillingType](docs/PaymentLinkUpdateRequestBillingType.md)
- [PaymentLinkUpdateRequestChargeType](docs/PaymentLinkUpdateRequestChargeType.md)
- [PaymentLinkUpdateRequestCycle](docs/PaymentLinkUpdateRequestCycle.md)
- [PaymentLinkUpdateRequestDTO](docs/PaymentLinkUpdateRequestDTO.md)
- [PaymentListRequestBillingType](docs/PaymentListRequestBillingType.md)
- [PaymentListRequestInvoiceStatus](docs/PaymentListRequestInvoiceStatus.md)
- [PaymentListRequestPaymentStatus](docs/PaymentListRequestPaymentStatus.md)
- [PaymentListResponseDTO](docs/PaymentListResponseDTO.md)
- [PaymentPayWithCreditCardRequestDTO](docs/PaymentPayWithCreditCardRequestDTO.md)
- [PaymentPixQrCodeResponseDTO](docs/PaymentPixQrCodeResponseDTO.md)
- [PaymentReceiveInCashRequestDTO](docs/PaymentReceiveInCashRequestDTO.md)
- [PaymentRefundGetResponseDTO](docs/PaymentRefundGetResponseDTO.md)
- [PaymentRefundGetResponsePaymentRefundStatus](docs/PaymentRefundGetResponsePaymentRefundStatus.md)
- [PaymentRefundListResponseDTO](docs/PaymentRefundListResponseDTO.md)
- [PaymentRefundRequestDTO](docs/PaymentRefundRequestDTO.md)
- [PaymentRefundSplitRequestDTO](docs/PaymentRefundSplitRequestDTO.md)
- [PaymentRefundedSplitResponseDTO](docs/PaymentRefundedSplitResponseDTO.md)
- [PaymentSaveRequestBillingType](docs/PaymentSaveRequestBillingType.md)
- [PaymentSaveRequestDTO](docs/PaymentSaveRequestDTO.md)
- [PaymentSaveWithCreditCardCreditCardCreditCardBrand](docs/PaymentSaveWithCreditCardCreditCardCreditCardBrand.md)
- [PaymentSaveWithCreditCardCreditCardDTO](docs/PaymentSaveWithCreditCardCreditCardDTO.md)
- [PaymentSaveWithCreditCardRequestBillingType](docs/PaymentSaveWithCreditCardRequestBillingType.md)
- [PaymentSaveWithCreditCardRequestDTO](docs/PaymentSaveWithCreditCardRequestDTO.md)
- [PaymentSimulateBankSlipResponseDTO](docs/PaymentSimulateBankSlipResponseDTO.md)
- [PaymentSimulateCreditCardResponseDTO](docs/PaymentSimulateCreditCardResponseDTO.md)
- [PaymentSimulateInstallmentResponseDTO](docs/PaymentSimulateInstallmentResponseDTO.md)
- [PaymentSimulatePixResponseDTO](docs/PaymentSimulatePixResponseDTO.md)
- [PaymentSimulateRequestBillingType](docs/PaymentSimulateRequestBillingType.md)
- [PaymentSimulateRequestDTO](docs/PaymentSimulateRequestDTO.md)
- [PaymentSimulateResponseDTO](docs/PaymentSimulateResponseDTO.md)
- [PaymentSplitGetFullResponseDTO](docs/PaymentSplitGetFullResponseDTO.md)
- [PaymentSplitGetFullResponsePaymentSplitCancellationReason](docs/PaymentSplitGetFullResponsePaymentSplitCancellationReason.md)
- [PaymentSplitGetFullResponsePaymentSplitStatus](docs/PaymentSplitGetFullResponsePaymentSplitStatus.md)
- [PaymentSplitGetResponseDTO](docs/PaymentSplitGetResponseDTO.md)
- [PaymentSplitGetResponsePaymentSplitCancellationReason](docs/PaymentSplitGetResponsePaymentSplitCancellationReason.md)
- [PaymentSplitGetResponsePaymentSplitStatus](docs/PaymentSplitGetResponsePaymentSplitStatus.md)
- [PaymentSplitListPaidRequestPaymentSplitStatus](docs/PaymentSplitListPaidRequestPaymentSplitStatus.md)
- [PaymentSplitListReceivedRequestPaymentSplitStatus](docs/PaymentSplitListReceivedRequestPaymentSplitStatus.md)
- [PaymentSplitListResponseDTO](docs/PaymentSplitListResponseDTO.md)
- [PaymentSplitPaymentInfoResponseDTO](docs/PaymentSplitPaymentInfoResponseDTO.md)
- [PaymentSplitRequestDTO](docs/PaymentSplitRequestDTO.md)
- [PaymentStatusResponseDTO](docs/PaymentStatusResponseDTO.md)
- [PaymentStatusResponsePaymentStatus](docs/PaymentStatusResponsePaymentStatus.md)
- [PaymentUpdateRequestBillingType](docs/PaymentUpdateRequestBillingType.md)
- [PaymentUpdateRequestDTO](docs/PaymentUpdateRequestDTO.md)
- [PaymentViewingInfoResponseDTO](docs/PaymentViewingInfoResponseDTO.md)
- [PixAddressKeyGetResponseDTO](docs/PixAddressKeyGetResponseDTO.md)
- [PixAddressKeyGetResponsePixAddressKeyStatus](docs/PixAddressKeyGetResponsePixAddressKeyStatus.md)
- [PixAddressKeyGetResponsePixAddressKeyType](docs/PixAddressKeyGetResponsePixAddressKeyType.md)
- [PixAddressKeyListRequestPixAddressKeyStatus](docs/PixAddressKeyListRequestPixAddressKeyStatus.md)
- [PixAddressKeyListResponseDTO](docs/PixAddressKeyListResponseDTO.md)
- [PixAddressKeyQrCodeGetResponseDTO](docs/PixAddressKeyQrCodeGetResponseDTO.md)
- [PixAddressKeySaveRequestDTO](docs/PixAddressKeySaveRequestDTO.md)
- [PixAddressKeySaveRequestPixAddressKeyType](docs/PixAddressKeySaveRequestPixAddressKeyType.md)
- [PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO](docs/PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO.md)
- [PixAutomaticRecurringPaymentInstructionGetResponseDTO](docs/PixAutomaticRecurringPaymentInstructionGetResponseDTO.md)
- [PixAutomaticRecurringPaymentInstructionListRequestPixAutomaticRecurringPaymentInstructionStatus](docs/PixAutomaticRecurringPaymentInstructionListRequestPixAutomaticRecurringPaymentInstructionStatus.md)
- [PixAutomaticRecurringPaymentInstructionListResponseDTO](docs/PixAutomaticRecurringPaymentInstructionListResponseDTO.md)
- [PixOriginalTransactionResponseDTO](docs/PixOriginalTransactionResponseDTO.md)
- [PixQrCodeDecodeReceiverDTO](docs/PixQrCodeDecodeReceiverDTO.md)
- [PixQrCodeDecodeReceiverPersonType](docs/PixQrCodeDecodeReceiverPersonType.md)
- [PixQrCodeDecodeReceiverPixAccountType](docs/PixQrCodeDecodeReceiverPixAccountType.md)
- [PixQrCodeDecodeRequestDTO](docs/PixQrCodeDecodeRequestDTO.md)
- [PixQrCodeDecodeResponseDTO](docs/PixQrCodeDecodeResponseDTO.md)
- [PixQrCodeDecodeResponsePixQrCodeType](docs/PixQrCodeDecodeResponsePixQrCodeType.md)
- [PixQrCodeDecodeResponsePixTransactionCashValueFinality](docs/PixQrCodeDecodeResponsePixTransactionCashValueFinality.md)
- [PixQrCodeDecodeResponsePixTransactionOriginType](docs/PixQrCodeDecodeResponsePixTransactionOriginType.md)
- [PixQrCodeDeleteResponseDTO](docs/PixQrCodeDeleteResponseDTO.md)
- [PixQrCodeSaveRequestDTO](docs/PixQrCodeSaveRequestDTO.md)
- [PixQrCodeSaveResponseDTO](docs/PixQrCodeSaveResponseDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationGetResponseDTO](docs/PixReceiverAutomaticRecurringAuthorizationGetResponseDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringFrequency](docs/PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringFrequency.md)
- [PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringOriginType](docs/PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringOriginType.md)
- [PixReceiverAutomaticRecurringAuthorizationGetResponsePixReceiverAutomaticRecurringAuthorizationStatus](docs/PixReceiverAutomaticRecurringAuthorizationGetResponsePixReceiverAutomaticRecurringAuthorizationStatus.md)
- [PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO](docs/PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO](docs/PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationListRequestPixReceiverAutomaticRecurringAuthorizationStatus](docs/PixReceiverAutomaticRecurringAuthorizationListRequestPixReceiverAutomaticRecurringAuthorizationStatus.md)
- [PixReceiverAutomaticRecurringAuthorizationListResponseDTO](docs/PixReceiverAutomaticRecurringAuthorizationListResponseDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO](docs/PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO.md)
- [PixReceiverAutomaticRecurringAuthorizationSaveRequestPixAutomaticRecurringFrequency](docs/PixReceiverAutomaticRecurringAuthorizationSaveRequestPixAutomaticRecurringFrequency.md)
- [PixRecurringTransactionExternalAccountDTO](docs/PixRecurringTransactionExternalAccountDTO.md)
- [PixRecurringTransactionGetItemResponseDTO](docs/PixRecurringTransactionGetItemResponseDTO.md)
- [PixRecurringTransactionGetItemResponsePixRecurringTransactionItemStatus](docs/PixRecurringTransactionGetItemResponsePixRecurringTransactionItemStatus.md)
- [PixRecurringTransactionGetResponseDTO](docs/PixRecurringTransactionGetResponseDTO.md)
- [PixRecurringTransactionGetResponsePixRecurringTransactionFrequency](docs/PixRecurringTransactionGetResponsePixRecurringTransactionFrequency.md)
- [PixRecurringTransactionGetResponsePixRecurringTransactionOrigin](docs/PixRecurringTransactionGetResponsePixRecurringTransactionOrigin.md)
- [PixRecurringTransactionGetResponsePixRecurringTransactionStatus](docs/PixRecurringTransactionGetResponsePixRecurringTransactionStatus.md)
- [PixRecurringTransactionListResponseDTO](docs/PixRecurringTransactionListResponseDTO.md)
- [PixTokenBucketGetAddressKeyResponseDTO](docs/PixTokenBucketGetAddressKeyResponseDTO.md)
- [PixTransactionExternalAccountResponseDTO](docs/PixTransactionExternalAccountResponseDTO.md)
- [PixTransactionExternalAccountResponsePixAddressKeyType](docs/PixTransactionExternalAccountResponsePixAddressKeyType.md)
- [PixTransactionGetResponseDTO](docs/PixTransactionGetResponseDTO.md)
- [PixTransactionGetResponsePixAddressKeyType](docs/PixTransactionGetResponsePixAddressKeyType.md)
- [PixTransactionGetResponsePixTransactionCashValueFinality](docs/PixTransactionGetResponsePixTransactionCashValueFinality.md)
- [PixTransactionGetResponsePixTransactionOriginType](docs/PixTransactionGetResponsePixTransactionOriginType.md)
- [PixTransactionGetResponsePixTransactionStatus](docs/PixTransactionGetResponsePixTransactionStatus.md)
- [PixTransactionGetResponsePixTransactionType](docs/PixTransactionGetResponsePixTransactionType.md)
- [PixTransactionListRequestPixTransactionStatus](docs/PixTransactionListRequestPixTransactionStatus.md)
- [PixTransactionListRequestPixTransactionType](docs/PixTransactionListRequestPixTransactionType.md)
- [PixTransactionListResponseDTO](docs/PixTransactionListResponseDTO.md)
- [PixTransactionQrCodePayerResponseDTO](docs/PixTransactionQrCodePayerResponseDTO.md)
- [PixTransactionQrCodeResponseDTO](docs/PixTransactionQrCodeResponseDTO.md)
- [PixTransactionQrCodeSaveRequestDTO](docs/PixTransactionQrCodeSaveRequestDTO.md)
- [PixTransactionSaveRequestDTO](docs/PixTransactionSaveRequestDTO.md)
- [RecurringPixTransactionListItemsResponseDTO](docs/RecurringPixTransactionListItemsResponseDTO.md)
- [RecurringPixTransactionListRequestPixRecurringTransactionStatus](docs/RecurringPixTransactionListRequestPixRecurringTransactionStatus.md)
- [SubscriptionConfigureInvoiceRequestDTO](docs/SubscriptionConfigureInvoiceRequestDTO.md)
- [SubscriptionDeleteInvoiceConfigResponseDTO](docs/SubscriptionDeleteInvoiceConfigResponseDTO.md)
- [SubscriptionDeleteResponseDTO](docs/SubscriptionDeleteResponseDTO.md)
- [SubscriptionGetInvoicesRequestInvoiceStatus](docs/SubscriptionGetInvoicesRequestInvoiceStatus.md)
- [SubscriptionGetResponseBillingType](docs/SubscriptionGetResponseBillingType.md)
- [SubscriptionGetResponseCycle](docs/SubscriptionGetResponseCycle.md)
- [SubscriptionGetResponseDTO](docs/SubscriptionGetResponseDTO.md)
- [SubscriptionGetResponseSubscriptionStatus](docs/SubscriptionGetResponseSubscriptionStatus.md)
- [SubscriptionInvoiceConfigGetResponseDTO](docs/SubscriptionInvoiceConfigGetResponseDTO.md)
- [SubscriptionInvoiceConfigUpdateRequestDTO](docs/SubscriptionInvoiceConfigUpdateRequestDTO.md)
- [SubscriptionListPaymentsRequestPaymentStatus](docs/SubscriptionListPaymentsRequestPaymentStatus.md)
- [SubscriptionListRequestBillingType](docs/SubscriptionListRequestBillingType.md)
- [SubscriptionListRequestSubscriptionStatus](docs/SubscriptionListRequestSubscriptionStatus.md)
- [SubscriptionListResponseDTO](docs/SubscriptionListResponseDTO.md)
- [SubscriptionSaveRequestBillingType](docs/SubscriptionSaveRequestBillingType.md)
- [SubscriptionSaveRequestCycle](docs/SubscriptionSaveRequestCycle.md)
- [SubscriptionSaveRequestDTO](docs/SubscriptionSaveRequestDTO.md)
- [SubscriptionSaveWithCreditCardRequestBillingType](docs/SubscriptionSaveWithCreditCardRequestBillingType.md)
- [SubscriptionSaveWithCreditCardRequestCycle](docs/SubscriptionSaveWithCreditCardRequestCycle.md)
- [SubscriptionSaveWithCreditCardRequestDTO](docs/SubscriptionSaveWithCreditCardRequestDTO.md)
- [SubscriptionSaveWithCreditCardResponseBillingType](docs/SubscriptionSaveWithCreditCardResponseBillingType.md)
- [SubscriptionSaveWithCreditCardResponseCycle](docs/SubscriptionSaveWithCreditCardResponseCycle.md)
- [SubscriptionSaveWithCreditCardResponseDTO](docs/SubscriptionSaveWithCreditCardResponseDTO.md)
- [SubscriptionSaveWithCreditCardResponseSubscriptionStatus](docs/SubscriptionSaveWithCreditCardResponseSubscriptionStatus.md)
- [SubscriptionSplitRequestDTO](docs/SubscriptionSplitRequestDTO.md)
- [SubscriptionSplitResponseDTO](docs/SubscriptionSplitResponseDTO.md)
- [SubscriptionSplitResponseSubscriptionSplitDisabledReason](docs/SubscriptionSplitResponseSubscriptionSplitDisabledReason.md)
- [SubscriptionSplitResponseSubscriptionSplitStatus](docs/SubscriptionSplitResponseSubscriptionSplitStatus.md)
- [SubscriptionUpdateCreditCardRequestDTO](docs/SubscriptionUpdateCreditCardRequestDTO.md)
- [SubscriptionUpdateRequestBillingType](docs/SubscriptionUpdateRequestBillingType.md)
- [SubscriptionUpdateRequestCycle](docs/SubscriptionUpdateRequestCycle.md)
- [SubscriptionUpdateRequestDTO](docs/SubscriptionUpdateRequestDTO.md)
- [SubscriptionUpdateRequestSubscriptionStatus](docs/SubscriptionUpdateRequestSubscriptionStatus.md)
- [TransferBankAccountGetResponseDTO](docs/TransferBankAccountGetResponseDTO.md)
- [TransferBankAccountSaveRequestBankAccountType](docs/TransferBankAccountSaveRequestBankAccountType.md)
- [TransferBankAccountSaveRequestDTO](docs/TransferBankAccountSaveRequestDTO.md)
- [TransferBankGetResponseDTO](docs/TransferBankGetResponseDTO.md)
- [TransferBankSaveRequestDTO](docs/TransferBankSaveRequestDTO.md)
- [TransferGetResponseDTO](docs/TransferGetResponseDTO.md)
- [TransferGetResponseTransferStatus](docs/TransferGetResponseTransferStatus.md)
- [TransferGetResponseTransferType](docs/TransferGetResponseTransferType.md)
- [TransferListResponseDTO](docs/TransferListResponseDTO.md)
- [TransferRecurringSaveRequestDTO](docs/TransferRecurringSaveRequestDTO.md)
- [TransferRecurringSaveRequestRecurringCheckoutScheduleFrequency](docs/TransferRecurringSaveRequestRecurringCheckoutScheduleFrequency.md)
- [TransferSaveInternalTransferAccountDTO](docs/TransferSaveInternalTransferAccountDTO.md)
- [TransferSaveInternalTransferRequestDTO](docs/TransferSaveInternalTransferRequestDTO.md)
- [TransferSaveInternalTransferResponseDTO](docs/TransferSaveInternalTransferResponseDTO.md)
- [TransferSaveInternalTransferResponseTransferStatus](docs/TransferSaveInternalTransferResponseTransferStatus.md)
- [TransferSaveInternalTransferResponseTransferType](docs/TransferSaveInternalTransferResponseTransferType.md)
- [TransferSaveRequestDTO](docs/TransferSaveRequestDTO.md)
- [TransferSaveRequestPixAddressKeyType](docs/TransferSaveRequestPixAddressKeyType.md)
- [TransferSaveRequestTransferType](docs/TransferSaveRequestTransferType.md)
- [WalletGetResponseDTO](docs/WalletGetResponseDTO.md)
- [WalletShowResponseDTO](docs/WalletShowResponseDTO.md)
- [WebhookConfigDeleteResponseDTO](docs/WebhookConfigDeleteResponseDTO.md)
- [WebhookConfigGetResponseDTO](docs/WebhookConfigGetResponseDTO.md)
- [WebhookConfigGetResponseWebhookEvent](docs/WebhookConfigGetResponseWebhookEvent.md)
- [WebhookConfigGetResponseWebhookSendType](docs/WebhookConfigGetResponseWebhookSendType.md)
- [WebhookConfigListResponseDTO](docs/WebhookConfigListResponseDTO.md)
- [WebhookConfigSaveRequestDTO](docs/WebhookConfigSaveRequestDTO.md)
- [WebhookConfigSaveRequestWebhookEvent](docs/WebhookConfigSaveRequestWebhookEvent.md)
- [WebhookConfigSaveRequestWebhookSendType](docs/WebhookConfigSaveRequestWebhookSendType.md)
- [WebhookConfigUpdateRequestDTO](docs/WebhookConfigUpdateRequestDTO.md)
- [WebhookConfigUpdateRequestWebhookEvent](docs/WebhookConfigUpdateRequestWebhookEvent.md)
- [WebhookConfigUpdateRequestWebhookSendType](docs/WebhookConfigUpdateRequestWebhookSendType.md)

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
