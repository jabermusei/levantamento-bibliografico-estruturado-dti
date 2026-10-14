# Relatório de deduplicação do Módulo 1 — v1.0

- **Data de processamento:** 14/10/2026.
- **Arquivo derivado:** `2026-10-14_M1_BASE_COMBINADA_DEDUPLICADA_v1.0.xlsx`.
- **Tamanho:** 266.492 bytes.
- **SHA-256:** `528CE6BBD88AD9E3EEBB31B73E2E185BE295337B32D8FCA6EF53C0FC01FDD7F3`.
- **Estado:** verificado e preservado localmente; não publicado no GitHub por conter metadados e resumos provenientes de bases sujeitas a contrato.

## Entradas

| Busca | Registros | SHA-256 da exportação bruta |
|---|---:|---|
| M1-SCO-001 | 111 | `7CE0AEBE6FECBD44B6C67DE0AFA374AB20354D767833CAB4A174EB34A6DE6A95` |
| M1-WOS-001 | 78 | `A044BB4EB62D3B76B232274D8D64924AFDC1B9F944C8D5F93012698ADD7FD840` |
| **Total combinado** | **189** | — |

## Regras

1. Normalizar DOI por caixa, prefixos de URL/`doi:` e espaços finais.
2. Confirmar duplicata quando o DOI normalizado coincidir entre Scopus e Web of Science.
3. Na ausência de DOI comum, confirmar duplicata quando coincidirem título normalizado, ano e sobrenome normalizado do primeiro autor, desde que não exista conflito de DOI.
4. Para pares confirmados, selecionar como representante o registro com maior completude de metadados; em empate, selecionar o maior resumo; persistindo empate, selecionar Scopus.
5. Preservar todas as linhas de origem na aba `Base combinada`; marcar uma linha como `DUPLICATA` e manter a outra como `REPRESENTANTE`.
6. Procurar, entre os registros restantes, candidatos com similaridade Jaccard de título igual ou superior a 0,90 e diferença de ano de no máximo um ano. Esses candidatos exigiriam revisão humana e não seriam removidos automaticamente.

## Resultado

| Classe | Quantidade |
|---|---:|
| Pares confirmados por DOI exato | 56 |
| Pares confirmados por título, ano e primeiro autor | 2 |
| Linhas marcadas como duplicata | 58 |
| Candidatos pendentes de revisão humana | 0 |
| **Registros únicos para o corpus de trabalho** | **131** |

Não foram encontradas duplicatas internas por identificador em cada exportação nem candidatos residuais acima do limiar conservador. A deduplicação é instrumental e não constitui triagem de pertinência, seleção de fontes ou constituição do corpus final da tese.

## Estrutura da planilha

- `Resumo`: contagens, regras e hashes das entradas.
- `Base combinada`: todas as 189 linhas com proveniência e estado de deduplicação.
- `Corpus único`: 131 representantes ou registros recuperados em uma única base.
- `Pares duplicados`: 58 pares, regra aplicada e representante escolhido.

## Verificações

- arquivo reaberto após a exportação;
- quatro abas presentes nas dimensões esperadas;
- contagens reconciliadas com as entradas;
- zero erros de fórmula detectados;
- inspeção visual das quatro abas concluída;
- hash SHA-256 calculado após a versão final.
