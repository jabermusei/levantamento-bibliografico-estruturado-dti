# Plano de leitura e extração — corpus acessível v1 do Módulo 1

**Data:** 21 de outubro de 2026  
**Status:** adotado pelo pesquisador em 21 de outubro de 2026; decisão operacional OA1  
**Universo:** 53 documentos únicos selecionados e uma posição duplicada preservada no instrumento canônico  
**Regra:** a atribuição a lote organiza a leitura; não altera a função registrada nem cria hierarquia de qualidade não documentada.

## Sequência dos lotes

### Lote 1 — Estado do campo e agenda de pesquisa (10 fontes)

**Estado de execução:** concluído e validado pelo pesquisador em 23/10/2026. As dez extrações passaram pelo controle de qualidade final, sem pendências estruturais; ver `2026-10-23_M1_QA_ENCERRAMENTO_LOTE1_v1.0.md`.

**Finalidade:** construir a visão inicial de convergências, tensões, lacunas e questões ainda abertas. Serve de mapa para as leituras seguintes, sem substituir a conferência das fontes conceituais.

`M1-SCO-001-028`, `M1-SCO-001-036`, `M1-SCO-001-039`, `M1-SCO-001-082`, `M1-WOS-001-009`, `M1-WOS-001-011`, `M1-WOS-001-012`, `M1-WOS-001-035`, `M1-WOS-001-039`, `M1-WOS-001-058`.

**Ordem interna inicial:** `M1-WOS-001-009` e `M1-WOS-001-035` (P1), seguidas pelas demais em ordem de centralidade para o Capítulo 2 e atualidade.

### Lote 2 — Base conceitual (19 fontes)

**Finalidade:** extrair definições, dimensões e relações entre governança, tecnologia, conhecimento, experiência, sustentabilidade, acessibilidade, segurança, inovação, atratividade, preservação e desenvolvimento.

`M1-SCO-001-026`, `M1-SCO-001-029`, `M1-SCO-001-060`, `M1-SCO-001-065`, `M1-SCO-001-083`, `M1-SCO-001-084`, `M1-SCO-001-088`, `M1-SCO-001-094`, `M1-SCO-001-096`, `M1-WOS-001-001`, `M1-WOS-001-002`, `M1-WOS-001-016`, `M1-WOS-001-029`, `M1-WOS-001-031`, `M1-WOS-001-046`, `M1-WOS-001-050`, `M1-WOS-001-051`, `M1-WOS-001-068`, `M1-WOS-001-071`.

**Ordem interna inicial:** P1 — `M1-SCO-001-026`, `M1-SCO-001-088`, `M1-WOS-001-031`, `M1-WOS-001-050` e `M1-WOS-001-071`; P2 — `M1-SCO-001-094`; depois, as demais por eixo conceitual.

### Lote 3 — Mapeamento do campo (14 fontes)

**Finalidade:** situar evolução temporal, redes, agrupamentos, influências intelectuais e distribuição temática. Os resultados bibliométricos serão tratados como descrição do corpus de cada estudo, não como representação automática de toda a literatura.

`M1-SCO-001-022`, `M1-SCO-001-031`, `M1-SCO-001-034`, `M1-SCO-001-053`, `M1-WOS-001-014`, `M1-WOS-001-019`, `M1-WOS-001-023`, `M1-WOS-001-028`, `M1-WOS-001-032`, `M1-WOS-001-036`, `M1-WOS-001-054`, `M1-WOS-001-055`, `M1-WOS-001-056`, `M1-WOS-001-063`.

**Ordem interna inicial:** `M1-WOS-001-023` e `M1-WOS-001-056` (P2), seguidas pelos mapeamentos gerais e, depois, pelos recortes especializados.

### Lote 4 — Métodos e instrumentos (5 fontes)

**Finalidade:** identificar procedimentos úteis para leitura, codificação, acompanhamento, prontidão e organização de dados. O método empregado por uma fonte não se torna método da tese sem decisão específica.

`M1-SCO-001-002`, `M1-WOS-001-020`, `M1-WOS-001-048`, `M1-WOS-001-062`, `M1-WOS-001-066`.

### Lote 5 — Contextos comparativos (6 fontes)

**Finalidade:** apoiar contrastes delimitados sobre patrimônio, dados, recuperação, praias inteligentes e inovação regional, sem fundir esses casos aos módulos China e Estados Unidos.

`M1-SCO-001-061`, `M1-SCO-001-064`, `M1-SCO-001-072`, `M1-WOS-001-003`, `M1-WOS-001-013`, `M1-WOS-001-041`.

## Campos mínimos de extração

| Campo | Conteúdo obrigatório |
|---|---|
| `id_canonico` | Identificador estável do instrumento de seleção. |
| `referencia_verificada` | Autoria, ano, título, veículo e DOI/URL conferidos na publicação. |
| `lote_e_funcao` | Lote de leitura e função vigente na tese. |
| `tipo_e_escopo` | Tipo de documento, pergunta/objetivo, recorte geográfico e temporal. |
| `metodo_e_corpus` | Bases, string quando informada, critérios, quantidade de documentos/casos e técnica de análise. |
| `definicao_de_DTI` | Definição adotada, autores mobilizados e páginas. Registrar ausência quando não houver definição. |
| `dimensoes_e_categorias` | Dimensões, pilares, indicadores e relações propostas, com páginas. |
| `achados_relevantes` | Achados pertinentes aos eixos do Capítulo 2, sem extrapolar o desenho da fonte. |
| `tensoes_e_contraevidencias` | Divergências, efeitos adversos, ausências e resultados que limitem a narrativa principal. |
| `limites_da_fonte` | Limitações declaradas e limitações observadas, separadas. |
| `sobreposicao_documental` | Corpus ou referências compartilhadas com outras sínteses; risco de dupla contagem. |
| `uso_proposto_na_tese` | Ponto argumentativo específico, capítulo/seção e estatuto: fonte, síntese, inferência ou proposição. |
| `localizador` | Página, seção, tabela ou figura de cada evidência; citação literal somente quando indispensável. |
| `controle` | Responsável, data da extração, estado da conferência e pendências. |

## Regra de conclusão de cada fonte

Uma fonte somente sai do lote de leitura quando: (1) sua identidade e referência estiverem conferidas; (2) os campos aplicáveis tiverem sido preenchidos; (3) cada afirmação relevante possuir localizador; (4) os limites estiverem explícitos; e (5) o uso proposto não duplicar silenciosamente outra síntese. A leitura não autoriza integração direta no texto da tese: qualquer avanço para N3/N4 continua sujeito ao portão de prontidão e à conferência da fonte original.

## Ponto de controle após o Lote 1

Antes de iniciar o Lote 2, verificar se as categorias usadas no instrumento de extração cobrem as tensões e lacunas encontradas nas dez fontes iniciais. Ajustes de campos são permitidos e devem ser registrados; mudanças no corpus, nas funções ou nos critérios exigem decisão separada.

**Resultado do ponto de controle em 23/10/2026:** os campos vigentes cobrem as tensões e lacunas observadas e serão preservados no Lote 2. Não houve mudança de corpus, funções ou critérios. A suficiência é operacional e não equivale a validação das categorias propostas pelas fontes nem a autorização de avanço para N3/N4.

**Estado operacional em 30/10/2026:** os cinco lotes estão encerrados. O QA final do Lote 5 confirmou seis de seis fontes em `VALIDADO_PESQUISADOR`, preenchimento dos 16 campos analíticos, alinhamento entre controle e extração, ausência de estado residual e ausência de erro de fórmula. O total global é de 53 de 53 documentos únicos validados, além de uma posição duplicada preservada sem contagem adicional. Não houve mudança de corpus, funções, critérios ou campos de extração, fusão com China/EUA nem adoção automática de método, dimensão, escala, tecnologia, campo, instrumento, ontologia ou questionário.

