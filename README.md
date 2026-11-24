# MVP — Análise de Dados e Boas Práticas

**Título do projeto:** _a definir_

**Autor:** Samuel Leonel Lucas Ferreira

**Curso:** Pós-graduação PUC-Rio — Sprint: Análise de Dados e Boas Práticas

## Sobre o trabalho

_Resumo do problema e das perguntas H1 e H2 (a escrever)._

## Arquivos

| Arquivo | Conteúdo |
|---|---|
| `MVP_Exoplanetas.ipynb` | Notebook com a análise exploratória e o pré-processamento |
| `data/exoplanetas_pscomppars_2026-11-24.csv` | Dados utilizados, exatamente como obtidos da fonte |

## Dados

- **Fonte:** NASA Exoplanet Archive, tabela *Planetary Systems Composite Parameters* (`pscomppars`).
- **Página da tabela:** https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=PSCompPars
- **DOI da tabela:** 10.26133/NEA13
- **Data de obtenção:** 24/11/2026. A tabela é atualizada continuamente pela fonte; este repositório guarda a cópia obtida nessa data.
- **Dimensões:** 6.473 linhas (um planeta confirmado por linha) e 22 colunas.
- **Recorte:** 22 das colunas da tabela original, sem filtro de linhas.

### Como obter exatamente os mesmos dados

A cópia em `data/` é a versão usada no notebook. A consulta que a gerou, pelo serviço TAP da fonte, foi:

```
https://exoplanetarchive.ipac.caltech.edu/TAP/sync?query=select+pl_name,hostname,sy_snum,sy_pnum,discoverymethod,disc_year,disc_facility,pl_orbper,pl_orbsmax,pl_rade,pl_bmasse,pl_bmassprov,pl_orbeccen,pl_insol,pl_eqt,st_spectype,st_teff,st_rad,st_mass,st_met,sy_dist,sy_vmag+from+pscomppars&format=csv
```

Repetir a consulta em outra data pode retornar mais planetas ou valores revisados.

## Como executar

1. Abra o notebook no Google Colab: _link a incluir_.
2. Use "Ambiente de execução → Reiniciar sessão e executar tudo".

O notebook lê os dados diretamente deste repositório, pela URL *raw* do arquivo CSV. Não é preciso enviar arquivos nem usar credenciais.

### Dependências

Python 3 com `pandas`, `numpy`, `matplotlib` e `seaborn`, nas versões do ambiente padrão do Colab. As versões usadas são impressas na seção 3 do notebook.

## Referências

- NASA Exoplanet Archive. *Planetary Systems Composite Parameters*. DOI 10.26133/NEA13.
- Agradecimento solicitado pela fonte: "This research has made use of the NASA Exoplanet Archive, which is operated by the California Institute of Technology, under contract with the National Aeronautics and Space Administration under the Exoplanet Exploration Program."
