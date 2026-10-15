# Critérios operacionais para triagem inicial do Módulo 1 — v1.0

- **Data:** 15/10/2026.
- **Fase:** triagem instrumental por título e resumo.
- **Unidade de análise:** registro bibliográfico único após deduplicação.
- **Universo:** 131 registros.
- **Finalidade:** verificar pertinência mínima, identificar a função de síntese e priorizar fontes para a etapa posterior de seleção.
- **Limite:** esta triagem não constitui revisão sistemática nem seleção analítica definitiva do corpus.

## Regra central

O registro deve apresentar relação substantiva com Destinos Turísticos Inteligentes, smart tourism destinations ou turismo inteligente territorializado e cumprir uma função de síntese pertinente ao Módulo 1. A simples presença da palavra `review`, de uma revisão bibliográfica rotineira ou de uma menção incidental a DTI não basta para inclusão.

Quando o título e o resumo não sustentarem uma decisão auditável, o estado deve permanecer `PENDENTE`, com indicação da necessidade de texto integral. A indisponibilidade imediata do texto completo não autoriza exclusão.

## Estados de decisão

| Estado | Uso |
|---|---|
| `PENDENTE` | Registro ainda não avaliado ou com informação insuficiente. |
| `INCLUIR` | Atende aos critérios e à função do Módulo 1. |
| `EXCLUIR` | Não atende aos critérios ou à função do Módulo 1. |
| `FORA_DO_MODULO` | Pode ser útil à tese, mas sua função pertence a outro módulo ou etapa. |
| `DUPLICATA` | Duplicação adicional confirmada após a deduplicação inicial. |

Toda decisão diferente de `PENDENTE` exige código, justificativa curta, revisor e data. Registros incluídos devem ser enquadrados como `NÚCLEO` ou `COMPLEMENTAR`.

## Códigos operacionais

| Código | Decisão | Definição operacional |
|---|---|---|
| `I1_SINTESE_DTI` | `INCLUIR` | O objeto principal ou uma seção substantiva sintetiza literatura sobre DTI ou smart tourism destinations. |
| `I2_SINTESE_ADJACENTE` | `INCLUIR` | Síntese de tema adjacente com contribuição verificável para turismo inteligente territorializado ou gestão de destinos. |
| `I3_MAPEAMENTO_CAMPO` | `INCLUIR` | Estudo bibliométrico, cientométrico, mapeamento do conhecimento ou estado da arte pertinente a DTI. |
| `I4_BASE_CONCEITUAL` | `INCLUIR` | Síntese útil para definições, terminologias, tradições, dimensões, métodos, lacunas ou referências recorrentes do campo. |
| `E1_SEM_RELACAO_SUBSTANTIVA_DTI` | `EXCLUIR` | A menção a DTI, smart tourism ou destino é incidental e não sustenta relação material com o objeto do módulo. |
| `E2_ESTUDO_PRIMARIO_SEM_SINTESE` | `EXCLUIR` | Estudo empírico ou aplicado primário sem função de síntese para o Módulo 1. |
| `E3_SECAO_ROTINEIRA_REVISAO` | `EXCLUIR` | Apenas contém revisão bibliográfica rotineira ou a palavra `review`, sem síntese substantiva como objeto ou contribuição. |
| `E4_TECNOLOGIA_SETORIAL_SEM_DESTINO` | `EXCLUIR` | Foco exclusivo em cidade inteligente, hotelaria, marketing, recomendação, mobilidade ou tecnologia sem relação substantiva com turismo territorializado ou destino. |
| `E5_TIPO_DOCUMENTAL_SEM_FUNCAO` | `EXCLUIR` | Editorial, notícia, apresentação, resumo isolado, errata ou item semelhante sem função documental justificada. |
| `E6_IDENTIDADE_NAO_VERIFICAVEL` | `EXCLUIR` | Identidade documental não verificável após tentativa registrada de confirmação. |
| `E7_RETRATADO_SEM_FUNCAO` | `EXCLUIR` | Item retratado sem função documental expressamente justificada. |
| `D1_DUPLICATA_ADICIONAL` | `DUPLICATA` | Duplicata adicional identificada após a etapa inicial. Deve apontar o registro representativo. |
| `F1_FORA_DO_MODULO` | `FORA_DO_MODULO` | Documento potencialmente útil à tese, mas com função pertencente a outro módulo ou etapa. |
| `P1_INFORMACAO_INSUFICIENTE` | `PENDENTE` | Título e resumo não bastam para uma decisão auditável. |
| `OUTRO` | qualquer | Situação não coberta pelos códigos anteriores; exige descrição específica. |

## Regras de não exclusão automática

- Não há filtro inicial de idioma.
- A indisponibilidade imediata do texto integral mantém o registro pendente.
- O rótulo do tipo documental fornecido pela base não substitui a avaliação da função efetiva do documento.
- A quantidade de citações, a base de origem e a duplicação de indexação entre bases não determinam pertinência.

## Sequência de preenchimento

1. Ler título e resumo preservados no instrumento.
2. Avaliar a relação substantiva com DTI e a função de síntese.
3. Preencher `decisao`.
4. Para `INCLUIR`, indicar `NÚCLEO` ou `COMPLEMENTAR`.
5. Preencher o código principal e uma justificativa curta baseada no conteúdo do registro.
6. Se a informação for insuficiente, manter `PENDENTE`, usar `P1_INFORMACAO_INSUFICIENTE` e marcar a necessidade de texto integral.
7. Identificar o revisor e registrar a data de toda decisão concluída.

## Instrumento

O arquivo local `2026-10-15_M1_TRIAGEM_TITULO_RESUMO_v1.0.xlsx` contém as abas `Resumo`, `Triagem` e `Critérios`. Todos os 131 registros foram inicializados como `PENDENTE`; nenhuma inclusão ou exclusão foi pré-atribuída.

- **SHA-256:** `DE5AC25C2A9C13FF213944C7738E9EECDC95061348044A53CF7C7EF3137D1CFE`.
- **Tamanho:** 110.041 bytes.
- **Fonte derivada:** `2026-10-14_M1_BASE_COMBINADA_DEDUPLICADA_v1.0.xlsx`.

O arquivo contém metadados licenciados das bases e permanece fora do repositório público. O documento de critérios, o hash e o registro da decisão são públicos.
