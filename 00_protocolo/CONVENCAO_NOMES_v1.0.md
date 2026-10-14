# Convenção de nomes v1.0

## Identificadores de busca

Formato: `M[modulo]-[base]-[sequencial]`.

- `M1`, `M2`, `M3`: módulo.
- Bases iniciais: `SCO` (Scopus), `WOS` (Web of Science), `INST` (fonte institucional), `ENC` (encadeamento de referências/citações).
- Sequencial com três dígitos: `001`, `002` etc.

Exemplo: `M1-SCO-001`.

## Arquivos de exportação

Formato:

`AAAA-MM-DD_Mx-BASE-NNN_base_colecao_formato_parteNN.ext`

Exemplos:

- `2026-10-14_M1-SCO-001_scopus_documents_csv_parte01.csv`
- `2026-10-14_M1-SCO-001_scopus_documents_ris_parte01.ris`

Regras:

- usar apenas letras minúsculas sem acentos nos componentes descritivos;
- manter o identificador da busca em maiúsculas;
- não incluir a contagem no nome, pois ela pode ser confundida com versão ou lote;
- não sobrescrever; nova exportação recebe nova parte ou novo identificador de busca;
- preservar a extensão original fornecida pela base.

## Arquivos derivados

Formato:

`AAAA-MM-DD_Mx-BASE-NNN_[etapa]_[descricao]_vNN.ext`

Etapas permitidas: `triagem`, `selecao`, `extracao`, `analise`.

## Versões documentais

- Protocolo: `PROTOCOLO_vMAJOR.MINOR.md`.
- Mudança metodológica substantiva incrementa `MAJOR` ou `MINOR` conforme a extensão.
- Arquivos de controle são cumulativos e não recebem cópias silenciosas.
- Versões superadas do protocolo devem ser preservadas e marcadas como substituídas no histórico.
