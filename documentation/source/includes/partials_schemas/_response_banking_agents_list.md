## ResponseBankingAgentsList
<a id="schemaResponseBankingAgentsList"></a>

```json
{
  "data": {
    "brand": [
      {
        "name": "string",
        "companies": [
          {
            "name": "string",
            "cnpjNumber": "string",
            "contractors": [
              {
                "name": "string",
                "cnpjNumber": "string",
                "bankingAgents": [
                  {
                    "identification": {
                      "corporationName": "string",
                      "groupName": "string",
                      "cnpjNumber": "string"
                    },
                    "postalAddresses": [
                      {
                        "address": "string",
                        "districtName": "string",
                        "townName": "string",
                        "countrySubDivision": "string",
                        "postCode": "string"
                      }
                    ],
                    "services": {
                      "codes": [
                        "string"
                      ],
                      "additionalInfo": "string"
                    }
                  }
                ]
              }
            ]
          }
        ]
      }
    ]
  },
  "links": {
    "self": "string",
    "first": "string",
    "prev": "string",
    "next": "string",
    "last": "string"
  },
  "meta": {
    "totalRecords": "string",
    "totalPages": "string"
  }
}
```

|     Nome          |  Tipo                                                  | Obrigatório  |                            Definição                  |
|:------------      |:---------------------------------                      |:-----------  |:----------------------------------------------------  |
| data              | object                                                 | Sim          |                                                       |
| brand           | [[BankingAgentsBrand](#schemaBankingAgentsBrand)]      | Sim          | Lista das organizações titulares das dependência.      |
| links             | [[LinksPaginated](#schemaLinksPaginated)]              | Sim          |                                                       |
| meta              | [MetaPaginated](#schemaMetaPaginated)                | Sim          |                                                       |

## BankingAgentsBrand
<a id="schemaBankingAgentsBrand"></a>

```json
{
  "name": "string",
  "companies": [
    {
      "name": "string",
      "cnpjNumber": "string",
      "contractors": [
        {
          "name": "string",
          "cnpjNumber": "string",
          "bankingAgents": [
            {
              "identification": {
                "corporationName": "string",
                "groupName": "string",
                "cnpjNumber": "string"
              },
              "postalAddresses": [
                {
                  "address": "string",
                  "districtName": "string",
                  "townName": "string",
                  "countrySubDivision": "string",
                  "postCode": "string"
                }
              ],
              "services": {
                "codes": [
                  "string"
                ],
                "additionalInfo": "string"
              }
            }
          ]
        }
      ]
    }
  ]
}
```

|     Nome     |  Tipo                                                      | Obrigatório  |                            Definição                     |
|:------------ |:---------------------------------                          |:-----------  |:----------------------------------------------------     |
| name         | string                                                     | Sim          | Nome da Marca reportada pelo participante do Open Banking. O conceito a que se refere a 'marca' utilizada está em definição pelos participantes.  |
| companies    | [[BankingAgentsCompanies](#schemaBankingAgentsCompanies)]  | Sim          | Lista de instituições pertencentes à marca.               |

## BankingAgentsCompanies 
<a id="schemaBankingAgentsCompanies"></a>

```json
{
  "name": "string",
  "cnpjNumber": "string",
  "contractors": [
    {
      "name": "string",
      "cnpjNumber": "string",
      "bankingAgents": [
        {
          "identification": {
            "corporationName": "string",
            "groupName": "string",
            "cnpjNumber": "string"
          },
          "postalAddresses": [
            {
              "address": "string",
              "districtName": "string",
              "townName": "string",
              "countrySubDivision": "string",
              "postCode": "string"
            }
          ],
          "services": {
            "codes": [
              "string"
            ],
            "additionalInfo": "string"
          }
        }
      ]
    }
  ]
}
```

|     Nome    |  Tipo                                                       | Obrigatório |                            Definição                                                                                                  |
|:----------- |:---------------------------------                           |:----------- |:------------------------------------------------------------------------------------------------------------------------------------- |
| name        | string                                                      | Sim         | Nome da Instituição, pertencente à Marca, responsável pela Dependência. p. ex. 'Empresa da Organização A'                             |
| cnpjNumber  | string                                                      | Sim         | Número completo do CNPJ da instituição responsável pelo Correspondente Bancário no pais - o CNPJ corresponde ao número de inscrição no Cadastro de Pessoa Jurídica. Deve-se ter apenas os números do CNPJ, sem máscara |
| contractors | [[BankingAgentsContractor](#schemaBankingAgentsContractor)] | Sim         | Lista de contratantes.                                                                                                                |


## BankingAgentsContractor
<a id="schemaBankingAgentsContractor"></a>

```json
{
  "name": "string",
  "cnpjNumber": "string",
  "bankingAgents": [
    {
      "identification": {
        "corporationName": "string",
        "groupName": "string",
        "cnpjNumber": "string"
      },
      "postalAddresses": [
        {
          "address": "string",
          "districtName": "string",
          "townName": "string",
          "countrySubDivision": "string",
          "postCode": "string"
        }
      ],
      "services": {
        "codes": [
          "string"
        ],
        "additionalInfo": "string"
      }
    }
  ]
}
```

|     Nome              |  Tipo                                    |  Obrigatório    |                            Descrição                  |
|:------------          |:-----------------------------            | :-------------  |:----------------------------------------------------  |
| name                  | string                                   | Sim             | Nome do contratante do serviço do correspondente.      |
| cnpjNumber            | string                                   | Sim             | CNPJ do Contrante.                                     |
| bankingAgents         | [[BankingAgent](#schemaBankingAgents)]   | Sim             | Lista de correspondentes bancários.                    |

## BankingAgent
<a id="schemaBankingAgents"></a>

```json
{
  "identification": {
    "corporationName": "string",
    "groupName": "string",
    "cnpjNumber": "string"
  },
  "postalAddresses": [
    {
      "address": "string",
      "districtName": "string",
      "townName": "string",
      "countrySubDivision": "string",
      "postCode": "string"
    }
  ],
  "services": {
    "codes": [
      "string"
    ],
    "additionalInfo": "string"
  }
}
```

| Nome | Tipo|Obrigatório|Descrição|
|:---- |:---|:---|:---|:---|
| identification |[BankingAgentsIdentification](#schemaBankingAgentsIdentification)|Sim|Dados de identificação do correspondente.|
| postalAddresses |[BankingAgentsPostalAddress](#schemaBankingAgentsPostalAddress)|Sim|Endereço do correspondente.|
| services |[BankingAgentsServices](#schemaBankingAgentsServices)|Sim|Serviços fornecidos pelo correspondente.|

## BankingAgentsIdentification
<a id="schemaBankingAgentsIdentification"></a>

```json
{
  "corporationName": "string",
  "groupName": "string",
  "cnpjNumber": "string"
}
```

| Nome                   | Tipo   | Obrigatório | Descrição                                                 |
|:----------------       |:------ |:----------- |:-------------------------------                           |
| corporationName        | string | Sim         | Nome do Correspondente Bancário.                          |
| groupName              | string | Não         | Nome do conglomerado ao qual pertence o agente bancário.  |
| cnpjNumber             | string | Sim         | CNPJ do Correspondente.                                   |

## BankingAgentsPostalAddress
<a id="schemaBankingAgentsPostalAddress"></a>

```json
{
  "address": "string",
  "districtName": "string",
  "townName": "string",
  "countrySubDivision": "string",
  "postCode": "string",
  "additionalInfo": "string",
  "ibgeCode": "string",
  "country": "string",
  "countryCode": "string",
  "latitude": "string",
  "longitude": "string"
}
```

| Nome               | Tipo   | Obrigatório |Descrição|
|:---                |:---    |:---         |:---                                                           |
| address            | string | Sim         | informação referente ao endereço do Correspondente Bancário informado: Tipo de logradouro + Nome do logradouro + Número do Logradouro (se não existir usar ' s/n') + complemento (se houver)  |
| districtName       | string | Sim         | Bairro.                                                       |
| townName           | string | Sim         | Cidade.                                                       |
| countrySubDivision | string | Sim         | Estado.                                                       |
| postCode           | string | Sim         | CEP.                                                          |                                                       
| additionalInfo     | string | Não         | Alguns logradouros ainda necessitam ser especificados por meio de complemento, conforme o exemplo a seguir: 'Loja B', 'Fundos', 'Casa 2', 'Lote C'  |
| ibgeCode           | string | Não         | Código IBGE de Município. A Tabela de Códigos de Municípios do IBGE apresenta a lista dos municípios brasileiros associados a um código composto de 7 dígitos, sendo os dois primeiros referentes ao código da Unidade da Federação. p.ex.'3550308' |
| country            | string | Não         | Nome do país. p.ex. Brasil  |
| countryCode        | string | Não         | Código do pais de acordo com o código “alpha3” do ISO-3166.p.ex.'BRA' |
| latitude           | string | Não         | Informação da Latitude referente a geolocalização informada. Entre -90 e 90.p.ex. '-90.8365180' |
| longitude          | string | Não         | Informação da Longitude referente a geolocalização informada. Entre -180 e 180.p.ex. '-180.836519' |

## BankingAgentsServices
<a id="schemaBankingAgentsServices"></a>

```json
{
  "codes": [
    "string"
  ],
  "additionalInfo": "string"
}
```

|Nome|Tipo|Obrigatório|Descrição|
|:---|:---|:---|:---|:---|
|codes|[[Enum BankingAgentsServicesCodes](#schemaEnumBankingAgentsServicesCodes)]|Sim| Lista de serviços prestados. |
|additionalInfo|string|Não| Detalhes adicionais sobre os serviços prestados. |

### Enum BankingAgentsServicesCodes
<a id="schemaEnumBankingAgentsServicesCodes"></a>

| Propriedade  | Código                                               | Definição                                                                                   |
|:------------ |:---------------------------------------------------- |:------------------------------------------------------------------------------------------- |
| codes        | RECEPCAO_ENCAMINHAMENTO_PROPOSTAS_ABERTURA_CONTAS    | Recepção e encaminhamento de propostas de abertura de contas.                                |
| codes        | REALIZACAO_RECEBIMENTOS_PAGAMENTOS_TRANSFERENCIA_ELETRONICAS   | Realização de recebimentos, pagamentos e transferências eletrônicas.                         |
| codes        | RECEBIMENTOS_PAGAMENTOS_QUALQUER_NATUREZA   | Recebimentos e pagamentos de qualquer natureza.                                              |
| codes        | EXECUCAO_ATIVA_PASSIVA_ORDENS_PAGAMENTO      | Execução ativa e passiva de ordens de pagamento.                                             |
| codes        | RECEPCAO_ENCAMINHAMENTO_PROPOSTAS_CREDITO_ARRENDAMENTO_MERCANTIL  | Recepção e encaminhamento de propostas de operações de crédito e de arrendamento mercantil.  |
| codes        | RECEBIMENTO_PAGAMENTOS_RELACIONADOS_LETRAS_CAMBIO_ACEITE_INSTITUICAO | Recebimento e pagamentos relacionados a letras de câmbio de aceite da instituição.           |
| codes        | RECEPCAO_ENCAMINHAMENTO_PROPOSTAS_FORNECEIMENTO_CARTAO_CREDITO | Recepção e encaminhamento de propostas de fornecimento de cartões de crédito.                |
| codes        | REALIZACAO_OPERACOES_CAMBIO                 | Realização de operações de câmbio.                                                           |
