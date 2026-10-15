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

## Estado atual

| ID | Arquivo | Bytes | SHA-256 | Estado |
|---|---|---:|---|---|
| EXP-M1-SCO-001-CSV-01 | `2026-10-14_M1-SCO-001_scopus_documents_csv_parte01.csv` | 1.589.607 | `7CE0AEBE6FECBD44B6C67DE0AFA374AB20354D767833CAB4A174EB34A6DE6A95` | VERIFICADO |
| EXP-M1-WOS-001-TXT-01 | `2026-10-14_M1-WOS-001_wos_core_collection_plaintext_full_record_cited_references_parte01.txt` | 719.912 | `A044BB4EB62D3B76B232274D8D64924AFDC1B9F944C8D5F93012698ADD7FD840` | VERIFICADO |
| DER-M1-DEDUP-001-XLSX | `2026-10-14_M1_BASE_COMBINADA_DEDUPLICADA_v1.0.xlsx` | 266.492 | `528CE6BBD88AD9E3EEBB31B73E2E185BE295337B32D8FCA6EF53C0FC01FDD7F3` | VERIFICADO |
| DER-M1-TRIAGEM-001-XLSX | `2026-10-15_M1_TRIAGEM_TITULO_RESUMO_v1.0.xlsx` | 110.041 | `DE5AC25C2A9C13FF213944C7738E9EECDC95061348044A53CF7C7EF3137D1CFE` | VERIFICADO |

Os hashes foram calculados nos arquivos de origem e recalculados após as cópias para a pasta oficial. Os valores foram idênticos. A exportação Scopus contém 111 registros e 45 campos. A exportação Web of Science contém 78 registros PT/ER, 78 identificadores UT únicos, 78 resumos e 74 DOI únicos; inicia com o cabeçalho `FN Clarivate Analytics Web of Science` e termina com `EF`.

A planilha derivada de deduplicação foi reaberta após a exportação e verificada quanto às dimensões, contagens, erros de fórmula e apresentação visual. Ela preserva 189 linhas na base combinada e contém 131 registros no corpus único.

A planilha de triagem por título e resumo foi criada como arquivo separado, reaberta após a exportação e verificada quanto às três abas, às 131 linhas, às fórmulas de resumo, às validações de entrada, aos erros de fórmula e à apresentação visual. Todos os registros permanecem inicialmente `PENDENTE`.
