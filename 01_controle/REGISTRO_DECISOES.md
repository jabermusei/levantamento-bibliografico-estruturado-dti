# Registro de decisões

As decisões são cumulativas. Não apagar entradas; se uma decisão for revista, criar nova entrada e apontar qual decisão ela substitui.

## DEC-20261014-001 — Abertura prospectiva

- **Data e hora:** 2026-10-14 14:30:25 -03:00.
- **Decisão:** considerar como evidência do novo levantamento apenas buscas, exportações, triagens e decisões produzidas a partir de 14/10/2026.
- **Justificativa:** impedir retrodatação e mistura com levantamentos anteriores.
- **Efeito:** materiais anteriores podem informar o desenho, mas não preencher registros do ciclo novo.

## DEC-20261014-002 — Denominação e estatuto

- **Data e hora:** 2026-10-14 14:30:25 -03:00.
- **Decisão:** adotar exclusivamente a denominação “levantamento bibliográfico estruturado para construção e delimitação do corpus teórico e documental”.
- **Justificativa:** o procedimento subsidia a tese e não será apresentado como revisão sistemática ou resultado autônomo de revisão.

## DEC-20261014-003 — Localização oficial e separação

- **Data e hora:** 2026-10-14 14:30:25 -03:00.
- **Decisão:** adotar `04_METODOLOGIA_E_CORPUS/levantamento_bibliografico_estruturado_dti_2026` como localização oficial.
- **Justificativa:** a função principal é metodológica e de delimitação de corpus; a pasta irmã evita confusão com `revisao_sistematica_dti` e com os casos anteriores.

## DEC-20261014-004 — Primeira busca

- **Data e hora:** 2026-10-14 14:30:25 -03:00.
- **Decisão:** iniciar pelo Módulo 1 na Scopus, busca `M1-SCO-001`, sem executar qualquer outra busca antes de registrar seu retorno.
- **Justificativa:** testar primeiro o bloco conceitual e os marcadores de síntese em uma base multidisciplinar antes da tradução para outras interfaces.
- **Estado:** executada em 14/10/2026, com 111 resultados; exportação pendente.

## DEC-20261014-005 — Aceite da contagem de M1-SCO-001

- **Data e hora:** 2026-10-14 16:43:32 -03:00.
- **Evidência:** captura da página de resultados da Scopus mostrando 111 documentos e a string executada.
- **Decisão:** aceitar a contagem de 111 registros para orientar a exportação da busca `M1-SCO-001`.
- **Condição:** completar a exportação, o inventário e o hash antes de formular ou liberar a busca seguinte.

## DEC-20261014-006 — Aceite da exportação de M1-SCO-001

- **Data e hora:** 2026-10-14 16:49:17 -03:00.
- **Decisão:** aceitar como exportação bruta oficial o arquivo `2026-10-14_M1-SCO-001_scopus_documents_csv_parte01.csv`.
- **Verificações:** 111 registros, 45 campos, 1.589.607 bytes e SHA-256 idêntico antes e depois da cópia para a pasta oficial.
- **Cautela:** o arquivo bruto permanece fora do GitHub por restrição de redistribuição; o inventário e o hash são públicos.

## DEC-20261014-007 — Tradução da estratégia e aceite da contagem de M1-WOS-001

- **Data e hora:** 2026-10-14 17:20:25 -03:00.
- **Decisão:** aceitar a tradução dos dois blocos conceituais para `TS` e do limite temporal para `PY=(1900-2026)` na Web of Science Core Collection.
- **Justificativa:** manter a lógica da busca `M1-SCO-001` com a sintaxe e os campos próprios da segunda base; `TS` inclui título, resumo, palavras-chave de autor e Keywords Plus, diferença que deve permanecer documentada.
- **Evidência:** captura da página de resultados mostrando a coleção, a estratégia executada e 78 documentos.
- **Efeito:** aceitar a contagem de 78 registros para `M1-WOS-001` e autorizar apenas sua exportação integral, sem filtros nem triagem nesta etapa.

## DEC-20261014-008 — Aceite da exportação de M1-WOS-001

- **Data e hora:** 2026-10-14 17:23:42 -03:00.
- **Decisão:** aceitar como exportação bruta oficial o arquivo `2026-10-14_M1-WOS-001_wos_core_collection_plaintext_full_record_cited_references_parte01.txt`.
- **Verificações:** 78 registros PT/ER, 78 identificadores UT únicos, 78 resumos, 74 DOI únicos, 719.912 bytes e SHA-256 idêntico antes e depois da cópia para a pasta oficial.
- **Cautela:** a ausência de quatro DOI não indica erro de exportação; os respectivos registros permanecem identificados por UT. O arquivo bruto permanece fora do GitHub por restrição de redistribuição.

## DEC-20261014-009 — Complementação do local de execução de M1-WOS-001

- **Data e hora do registro complementar:** 2026-10-14 17:28:36 -03:00.
- **Declaração do responsável:** a busca `M1-WOS-001` foi executada em Goiânia–GO.
- **Tratamento:** registrar o local como informação declarada posteriormente pelo responsável, sem atribuí-lo à captura da interface e sem alterar a data e hora técnica já documentada.
- **Escopo:** esta complementação se aplica somente a `M1-WOS-001`; não permite inferir automaticamente o local de outras buscas.

## DEC-20261014-010 — Deduplicação instrumental do Módulo 1

- **Data e hora de conclusão:** 2026-10-14 17:46:36 -03:00.
- **Entradas:** 111 registros de `M1-SCO-001` e 78 registros de `M1-WOS-001`, totalizando 189 linhas.
- **Decisão:** confirmar 56 pares por DOI exato e dois pares adicionais por título normalizado, ano e sobrenome normalizado do primeiro autor, sem conflito de DOI.
- **Resultado:** marcar 58 linhas como duplicatas e manter 131 registros no corpus único de trabalho.
- **Controle:** todas as 189 linhas permanecem preservadas na base combinada, com grupo, regra, estado e representante; nenhum candidato residual atingiu o limiar Jaccard de título ≥ 0,90 com diferença de ano ≤ 1.
- **Cautela:** esta operação não constitui triagem de pertinência nem seleção do corpus final.
- **Arquivo derivado:** `2026-10-14_M1_BASE_COMBINADA_DEDUPLICADA_v1.0.xlsx`, SHA-256 `528CE6BBD88AD9E3EEBB31B73E2E185BE295337B32D8FCA6EF53C0FC01FDD7F3`.

## DEC-20261015-011 — Preparação da triagem por título e resumo do Módulo 1

- **Data e hora de conclusão:** 2026-10-15 13:23:18 -03:00.
- **Entrada:** 131 registros únicos da base deduplicada v1.0.
- **Decisão:** fixar antes da avaliação os critérios operacionais, os estados de decisão e os códigos de justificativa para a triagem inicial por título e resumo.
- **Instrumento:** criar uma planilha separada da base deduplicada, preservando a fonte e inicializando todos os 131 registros como `PENDENTE`.
- **Controle:** nenhuma inclusão, exclusão, transferência de módulo ou nova duplicata foi pré-atribuída. Dúvidas devem permanecer `PENDENTE` e podem exigir obtenção do texto integral.
- **Arquivo derivado:** `2026-10-15_M1_TRIAGEM_TITULO_RESUMO_v1.0.xlsx`, 110.041 bytes, SHA-256 `DE5AC25C2A9C13FF213944C7738E9EECDC95061348044A53CF7C7EF3137D1CFE`.
- **Documento público:** `02_modulo_1_revisoes_e_sinteses/02_triagem_instrumental/CRITERIOS_TRIAGEM_M1_v1.0.md`.
- **Cautela:** esta etapa organiza a avaliação e não constitui seleção analítica definitiva nem revisão sistemática.

## DEC-20261016-012 — Abertura da seleção de fontes do Módulo 1

- **Data:** 16/10/2026.
- **Entrada:** 94 registros classificados como `INCLUIR` na triagem instrumental validada, sendo 52 `NÚCLEO` e 42 `COMPLEMENTAR`.
- **Decisão:** criar instrumento separado para obtenção, confirmação de identidade, definição da função na tese e decisão final de seleção.
- **Controle:** inicializar todos os 94 candidatos como `PENDENTE`; a inclusão instrumental não será convertida automaticamente em seleção definitiva.
- **Ordem operacional:** iniciar a obtenção e verificação pelos registros `NÚCLEO`; os registros `COMPLEMENTAR` permanecem candidatos e serão avaliados em ciclo posterior.
- **Regra de acesso:** indisponibilidade imediata do texto integral não autoriza exclusão automática; a tentativa e o estado de obtenção devem ser registrados.
- **Arquivo derivado:** `2026-10-16_M1_SELECAO_FONTES_v1.0.xlsx`, 87.156 bytes, SHA-256 `41A4B493AD4E64C4A51482701C764F844ABEB9EEA8382C69D2445E725CC8A35F`.
- **Documento público:** `02_modulo_1_revisoes_e_sinteses/03_fontes_selecionadas/CRITERIOS_SELECAO_M1_v1.0.md`.

## DEC-20261016-013 — Encerramento da triagem por título e resumo

- **Data:** 16/10/2026.
- **Entrada:** 131 registros únicos da base deduplicada.
- **Decisão:** encerrar a triagem instrumental com 94 registros `INCLUIR`, 37 registros `EXCLUIR` e nenhum `PENDENTE`.
- **Controle:** a decisão de triagem não equivale a seleção definitiva nem confirma acesso ao texto integral.
- **Efeito:** os 94 registros incluídos seguem para a etapa separada de seleção de fontes.

## DEC-20261018-014 — Encerramento da seleção inicial

- **Data:** 18/10/2026.
- **Entrada:** 94 candidatos provenientes da triagem.
- **Decisão:** encerrar a seleção inicial com 54 posições `SELECIONADO`, 16 `EXCLUIR` e 24 `PENDENTE` exclusivamente por ausência de acesso legal ao texto integral neste ciclo.
- **Controle:** os 24 registros sem acesso não são excluídos por indisponibilidade e permanecem como limite explícito do corpus acessível.
- **Efeito:** iniciar a conferência integral dos textos obtidos e preservar separadamente a fila sem acesso.

## DEC-20261019-015 — Encerramento da busca de acesso aos 24 pendentes

- **Data:** 19/10/2026.
- **Declaração do responsável:** toda a lista dos 24 registros pendentes foi pesquisada, sem obtenção legal dos textos integrais.
- **Decisão:** encerrar novas tentativas indefinidas de obtenção neste ciclo e manter os 24 registros documentados como limite de acesso.
- **Cautela:** o texto correto de `M1-WOS-001-060` permanece indisponível; uma cópia divergente foi isolada e não integra o corpus.

## DEC-20261021-016 — Delimitação do corpus acessível e plano de cinco lotes

- **Data:** 21/10/2026.
- **Decisão:** adotar a nota de delimitação do corpus acessível e organizar as posições selecionadas em cinco lotes funcionais: estado do campo e agenda; base conceitual; mapeamento do campo; métodos e instrumentos; contextos comparativos.
- **Campos:** preservar os campos de referência, método/corpus, definição ou tratamento de DTI, dimensões, achados, tensões, limites declarados e observados, sobreposição, uso proposto, localizadores e estado de validação.
- **Controle:** `PROPOSTA_EXTRAIDA` não equivale a `VALIDADO_PESQUISADOR`; nenhuma extração avança automaticamente para N3 ou N4.
- **Estatuto:** decisão operacional OA1 adotada pelo pesquisador.

## DEC-20261026-017 — Correção de identidade e congelamento do corpus único

- **Data:** 26/10/2026.
- **Evidência:** `M1-WOS-001-051` e `M1-SCO-001-096` correspondem ao mesmo documento de Femenia-Serra e Neuhofer (2018).
- **Decisão:** classificar `M1-WOS-001-051` como `DUPLICATA_DOCUMENTAL`, manter `M1-SCO-001-096` como representante e preservar a posição duplicada sem contagem adicional.
- **Resultado:** as 54 posições selecionadas correspondem a 53 documentos únicos e uma duplicata documental.
- **Controle:** a versão anterior do instrumento de seleção foi preservada no arquivo histórico da tese.

## DEC-20261030-018 — Encerramento das extrações do Módulo 1

- **Data:** 30/10/2026.
- **Decisão:** encerrar os cinco lotes após aprovação expressa das extrações pelo pesquisador.
- **Resultado:** 53 documentos únicos em `VALIDADO_PESQUISADOR` e uma posição em `DUPLICATA_DOCUMENTAL`; lotes encerrados com 10, 18, 14, 5 e 6 documentos únicos.
- **QA:** os cinco controles confirmam alinhamento de IDs, preenchimento dos campos vigentes, ausência de estados residuais e ausência de erros de fórmula.
- **Limite:** completude documental não implica homogeneidade metodológica, confirmação independente, causalidade, eficácia ou transferibilidade.
- **Próxima etapa:** consolidar o marco público pré-síntese e somente depois iniciar a síntese transversal.

## DEC-20261030-019 — Marco público pré-síntese do Módulo 1

- **Data:** 30/10/2026.
- **Decisão:** preparar a versão 1.1 do repositório como marco de execução anterior à síntese transversal, mantendo o protocolo metodológico na versão 1.0.
- **Conteúdo público:** protocolo, strings, decisões, critérios, planos, QAs, manifesto do corpus e hashes dos arquivos privados pertinentes.
- **Exclusões:** exportações brutas, PDFs, planilhas binárias, evidências de sessão, arquivos temporários e inspeções permanecem fora do repositório público.
- **Controle:** o manifesto registra 53 documentos únicos e uma posição duplicada, sem produzir síntese argumentativa ou proposição da tese.
- **Estatuto:** decisão operacional OA1; não altera problema, objetivos, teoria, método, corpus ou contribuição e não exige manifestação imediata do orientador formal.
