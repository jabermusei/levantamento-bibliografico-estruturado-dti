# Critérios operacionais para seleção de fontes do Módulo 1 — v1.0

- **Data:** 16/10/2026.
- **Fase:** seleção de fontes para o corpus teórico do Módulo 1.
- **Unidade de análise:** fonte bibliográfica candidata após triagem instrumental validada.
- **Universo:** 94 registros, sendo 52 classificados como `NÚCLEO` e 42 como `COMPLEMENTAR`.
- **Finalidade:** decidir, com justificativa auditável, quais fontes integrarão o corpus teórico e quais permanecerão excluídas ou pendentes de obtenção.
- **Limite:** a inclusão na triagem instrumental não equivale à seleção definitiva; esta etapa também não constitui revisão sistemática.

## Requisitos para decisão final

Uma fonte somente pode receber `SELECIONAR` quando apresentar:

1. identidade documental confirmada por DOI, identificador persistente, registro da base ou URL verificável;
2. função explícita na tese;
3. código de seleção e justificativa curta;
4. revisor e data da decisão.

A indisponibilidade imediata do texto integral não autoriza exclusão automática. A fonte permanece `PENDENTE`, com estado de obtenção e tentativa registrados.

## Estados de obtenção

| Estado | Uso |
|---|---|
| `NAO_INICIADA` | A busca pelo texto ou registro persistente ainda não começou. |
| `EM_BUSCA` | A obtenção está em andamento. |
| `OBTIDO` | Texto ou documento foi obtido e localizado de forma rastreável. |
| `ACESSO_RESTRITO` | A fonte foi localizada, mas o acesso integral depende de autorização ou assinatura. |
| `NAO_LOCALIZADO` | A tentativa registrada não localizou versão verificável; não implica exclusão automática. |

## Estados de seleção

| Estado | Uso |
|---|---|
| `PENDENTE` | A fonte ainda não recebeu decisão final. |
| `SELECIONAR` | A fonte tem identidade confirmada, função declarada e justificativa para integrar o corpus. |
| `EXCLUIR` | A fonte não integra o corpus após verificação documentada; exige código e justificativa. |

## Funções na tese

`BASE_CONCEITUAL`, `MAPEAMENTO_CAMPO`, `ESTADO_DO_CAMPO`, `METODO`, `AGENDA_DE_PESQUISA`, `CONTEXTO_COMPARATIVO` ou `OUTRA`. O uso de `OUTRA` exige descrição específica na justificativa.

## Códigos de seleção

| Código | Definição |
|---|---|
| `S1_SELECIONAR` | Selecionar para o corpus do Módulo 1. |
| `S2_EXCLUIR_SEM_FUNCAO` | Excluir porque a leitura não confirmou função substantiva para a tese. |
| `S3_EXCLUIR_IDENTIDADE` | Excluir após tentativa registrada de confirmação da identidade documental. |
| `S4_ADIAR_OBTENCAO` | Manter pendente enquanto se tenta obter ou verificar a fonte. |
| `OUTRO` | Situação não coberta; exige descrição específica. |

## Ordem operacional

1. Iniciar pelos 52 registros `NÚCLEO`.
2. Registrar o estado de obtenção e o local do arquivo ou URL persistente.
3. Confirmar a identidade documental.
4. Definir a função da fonte na tese.
5. Registrar código, decisão, justificativa, revisor e data.
6. Avaliar os 42 registros `COMPLEMENTAR` após o primeiro ciclo do núcleo, sem exclusão automática por prioridade.

## Instrumento

O arquivo `2026-10-16_M1_SELECAO_FONTES_v1.0.xlsx` contém as abas `Resumo`, `Seleção` e `Critérios`. Os 94 candidatos foram inicializados como `PENDENTE`; nenhuma seleção ou exclusão final foi pré-atribuída.

- **SHA-256:** `41A4B493AD4E64C4A51482701C764F844ABEB9EEA8382C69D2445E725CC8A35F`.
- **Tamanho:** 87.156 bytes.
- **Fonte derivada:** `2026-10-15_M1_TRIAGEM_TITULO_RESUMO_v1.0.xlsx`.

O instrumento contém metadados licenciados das bases e permanece fora do repositório público. Os critérios, o hash e o registro da decisão podem ser publicados.
