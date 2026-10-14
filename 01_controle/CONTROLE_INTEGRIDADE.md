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

Nenhuma exportação do novo levantamento existe ou foi registrada até a abertura do protocolo v1.0.
