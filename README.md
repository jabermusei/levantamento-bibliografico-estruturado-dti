# Levantamento bibliográfico estruturado para construção e delimitação do corpus teórico e documental

- **Início prospectivo:** 14 de outubro de 2026
- **Localização oficial:** `04_METODOLOGIA_E_CORPUS/levantamento_bibliografico_estruturado_dti_2026`
- **Protocolo vigente:** `00_protocolo/PROTOCOLO_v1.0.md`
- **Estado:** protocolo v1.0 publicado e arquivado; `M1-SCO-001` e `M1-WOS-001` executadas e exportadas em 14/10/2026, respectivamente com 111 e 78 registros; integridade verificada.
- **OSF Registration:** <https://osf.io/xhkgt/overview>
- **DOI:** <https://doi.org/10.17605/OSF.IO/XHKGT>
- **Repositório GitHub:** <https://github.com/jabermusei/levantamento-bibliografico-estruturado-dti>
- **Release GitHub v1.0:** <https://github.com/jabermusei/levantamento-bibliografico-estruturado-dti/releases/tag/v1.0>
- **DOI Zenodo v1.0:** <https://doi.org/10.5281/zenodo.23376580>
- **DOI Zenodo de todas as versões:** <https://doi.org/10.5281/zenodo.23376579>

## Regra de identidade

Este trabalho é um **levantamento bibliográfico estruturado para construção e delimitação do corpus teórico e documental** da tese. Ele não deve ser denominado revisão sistemática e não constitui, por si, um resultado autônomo de revisão de literatura.

Materiais, strings, matrizes, chats e resultados anteriores a 14/10/2026 podem ser consultados apenas como insumos para formular ou testar o protocolo. Eles não podem preencher retroativamente datas, buscas, contagens, exportações, decisões ou evidências deste registro. Os materiais anteriores permanecem em suas localizações originais e não são sobrescritos.

## Estrutura

| Pasta | Função |
|---|---|
| `00_protocolo` | Protocolo vigente, convenção de nomes e histórico de versões. |
| `01_controle` | Diário de buscas, registro de decisões, inventário de exportações e controle de integridade. |
| `02_modulo_1_revisoes_e_sinteses` | Revisões e estudos de síntese sobre DTI. |
| `03_modulo_2_china` | Literatura acadêmica e documentação pertinente ao caso China. |
| `04_modulo_3_estados_unidos` | Literatura acadêmica e documentação pertinente ao caso Estados Unidos. |

Cada módulo separa: planejamento/strings; exportações brutas; triagem instrumental; fontes selecionadas; análise documental.

## Ordem de consulta

1. `00_protocolo/PROTOCOLO_v1.0.md`.
2. `01_controle/REGISTRO_DECISOES.md`.
3. `01_controle/DIARIO_BUSCAS.csv`.
4. `01_controle/INVENTARIO_EXPORTACOES.csv` e `01_controle/CONTROLE_INTEGRIDADE.md`.
5. A pasta do módulo em andamento.

## Regra de avanço

Executar uma busca por vez. A próxima string só deve ser liberada depois que os metadados e, quando houver exportação, o arquivo e seu hash SHA-256 da busca anterior tiverem sido registrados.
