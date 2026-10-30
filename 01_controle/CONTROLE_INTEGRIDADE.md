# Controle de integridade

## Algoritmo

Usar SHA-256 para todas as exportações brutas e, quando pertinente, para arquivos derivados entregues como marcos do processo.

## Procedimento no PowerShell

Depois de salvar a exportação na pasta correta e antes de modificá-la:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath "CAMINHO_COMPLETO_DO_ARQUIVO"
```

Registrar o valor integral de `Hash`, o tamanho em bytes e a data/hora da exportação em `INVENTARIO_EXPORTACOES.csv`. Copiar o mesmo hash para a linha da busca em `DIARIO_BUSCAS.csv`.

## Estados de integridade

- `VERIFICADO`: hash recalculado e idêntico ao inventário.
- `REGISTRADO`: hash inicial registrado, ainda sem segunda conferência.
- `DIVERGENTE`: hash recalculado diferente; preservar os arquivos e abrir decisão.
- `PENDENTE`: arquivo existente sem hash; regularizar antes de avançar.

## Estado atual em 30/10/2026

### Exportações e instrumentos privados

| ID | Arquivo ou estado preservado | Bytes | SHA-256 | Estado |
|---|---|---:|---|---|
| EXP-M1-SCO-001-CSV-01 | `2026-10-14_M1-SCO-001_scopus_documents_csv_parte01.csv` | 1.589.607 | `7CE0AEBE6FECBD44B6C67DE0AFA374AB20354D767833CAB4A174EB34A6DE6A95` | VERIFICADO; privado |
| EXP-M1-WOS-001-TXT-01 | `2026-10-14_M1-WOS-001_wos_core_collection_plaintext_full_record_cited_references_parte01.txt` | 719.912 | `A044BB4EB62D3B76B232274D8D64924AFDC1B9F944C8D5F93012698ADD7FD840` | VERIFICADO; privado |
| DER-M1-DEDUP-001-XLSX | `2026-10-14_M1_BASE_COMBINADA_DEDUPLICADA_v1.0.xlsx` | 266.492 | `528CE6BBD88AD9E3EEBB31B73E2E185BE295337B32D8FCA6EF53C0FC01FDD7F3` | VERIFICADO; privado |
| DER-M1-TRIAGEM-001-XLSX | estado inicial criado em 15/10/2026 | 110.041 | `DE5AC25C2A9C13FF213944C7738E9EECDC95061348044A53CF7C7EF3137D1CFE` | HISTÓRICO; o binário inicial separado não foi preservado |
| DER-M1-TRIAGEM-002-XLSX | `2026-10-15_M1_TRIAGEM_TITULO_RESUMO_v1.0.xlsx`, estado final | 120.601 | `A8F39C891A8CD4BC1BB9E35FA55D29747872CAB1C4D0DFCCAEB3686D0415947C` | VERIFICADO; privado |
| DER-M1-SELECAO-001-XLSX | estado anterior à correção de duplicidade, preservado no arquivo histórico | 100.352 | `E8FDE6C5C304CFAB8C833448FD4E22073B421A64952C8AA47E0C9E5ABE0FC98C` | VERIFICADO; privado e superado |
| DER-M1-SELECAO-002-XLSX | `2026-10-16_M1_SELECAO_FONTES_v1.0.xlsx`, estado final | 100.733 | `4AF9F6F5E35C4CBE0F65A4DE82C29DD0DB228BCBEB1E2408EF709B16EB422C2E` | VERIFICADO; privado |
| DER-M1-LOTE1-XLSX | `2026-10-21_M1_EXTRACAO_LOTE1_v1.0.xlsx` | 33.146 | `656712DE53B916035927289FA1697121243CD2BCA23FCDEB14263F47AD6D5ADD` | VERIFICADO; privado |
| DER-M1-LOTE2-XLSX | `2026-10-23_M1_EXTRACAO_LOTE2_v1.0.xlsx` | 46.121 | `A6EFC7398F5715E796AA6C2B37B0CE08852215E5C9431FF704268EA43E8BE66B` | VERIFICADO; privado |
| DER-M1-LOTE3-XLSX | `2026-10-27_M1_EXTRACAO_LOTE3_v1.0.xlsx` | 39.879 | `958D7E9D9EB800E862C88D0E0E106D73FD7E1DAD3EB7535108F476D4FFE2B188` | VERIFICADO; privado |
| DER-M1-LOTE4-XLSX | `2026-10-28_M1_EXTRACAO_LOTE4_v1.0.xlsx` | 28.613 | `4E7A635EB0D13A5B589942A88F70FC4BD81A0798BE2297416254D3B7FCA57DE8` | VERIFICADO; privado |
| DER-M1-LOTE5-XLSX | `2026-10-29_M1_EXTRACAO_LOTE5_v1.0.xlsx` | 27.990 | `15EEE7D9B14CFE112EC184101F6AE5997DC0B1DCE2D31F6639CAB941A3F44DB2` | VERIFICADO; privado |

### Controles e manifesto públicos

| ID | Arquivo | Bytes | SHA-256 | Estado |
|---|---|---:|---|---|
| QA-M1-LOTE1-MD | `2026-10-23_M1_QA_ENCERRAMENTO_LOTE1_v1.0.md` | 4.104 | `19F36B42175A4D77D768D5895691829D0FFC99709942005D93D9FF67FBDF594B` | VERIFICADO; público |
| QA-M1-LOTE2-MD | `2026-10-26_M1_QA_ENCERRAMENTO_LOTE2_v1.0.md` | 5.088 | `C4801856064024880ABEC2BEC5CCEC0A6B2F503F24427482AD99B3514E28C877` | VERIFICADO; público |
| QA-M1-LOTE3-MD | `2026-10-28_M1_QA_ENCERRAMENTO_LOTE3_v1.0.md` | 5.401 | `B910CBC5E4EFEC986A2EA68EAC8ECE756C5B8FDF0198FBACA35FF627C1793174` | VERIFICADO; público |
| QA-M1-LOTE4-MD | `2026-10-29_M1_QA_ENCERRAMENTO_LOTE4_v1.0.md` | 6.350 | `5314D972D10BF2AA48BB2A4611771CC4D5119922EA9B185AB3DACD6C94AA7C9A` | VERIFICADO; público |
| QA-M1-LOTE5-MD | `2026-10-30_M1_QA_ENCERRAMENTO_LOTE5_v1.0.md` | 5.852 | `7DEA1682A274867C952DE5274C7F72119785ED7AE7E05D0C155D83845568EDE5` | VERIFICADO; público |
| MAN-M1-CORPUS-MD | `2026-10-30_M1_MANIFESTO_CORPUS_FINAL_v1.0.md` | 26.178 | `2F90EF4DE3EB78BCE08C21864F57CE47D6E9631A3A19F2DD784AF53C51B77DB8` | VERIFICADO; público |
| MAR-M1-PRE-SINTESE-MD | `2026-10-30_MARCO_PRE_SINTESE_M1_v1.1.md` | 3.961 | `09133C20204E029D72BF5AD7FB7E1F8F1C3F9BD948BF2A25C0D4579E7BFD47E3` | VERIFICADO; público |

Os hashes das exportações foram calculados nos arquivos de origem e recalculados após as cópias para a pasta oficial, com valores idênticos. A exportação Scopus contém 111 registros e 45 campos. A exportação Web of Science contém 78 registros PT/ER, 78 identificadores UT únicos, 78 resumos e 74 DOI únicos; inicia com `FN Clarivate Analytics Web of Science` e termina com `EF`.

A planilha de deduplicação preserva 189 linhas e 131 registros únicos. O estado inicial da planilha de triagem permanece documentado por tamanho e hash, mas não foi preservado como binário separado; essa limitação não deve ser ocultada nem confundida com o arquivo final de triagem. A versão anterior da seleção foi preservada no histórico antes da correção da duplicidade documental.

Os cinco instrumentos de extração foram reabertos e conferidos por seus respectivos QAs. Em conjunto, registram 53 documentos únicos em `VALIDADO_PESQUISADOR` e uma posição em `DUPLICATA_DOCUMENTAL`. Arquivos binários, exportações e textos integrais permanecem no acervo privado; os controles, o manifesto e seus hashes são públicos.
