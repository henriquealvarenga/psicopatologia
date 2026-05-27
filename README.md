# Psicopatologia — Uma Breve Introdução

Livro-texto introdutório à psicopatologia descritiva, construído em [Quarto](https://quarto.org) (`type: book`) e publicado no GitHub Pages via GitHub Actions.

- **Site:** <https://henriquealvarenga.com/psicopatologia>
- **Autor:** Henrique Alvarenga da Silva — UFSJ, Curso de Medicina
- **Licença:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.pt_BR)

## Desenvolvimento local

```bash
# pré-requisito: Quarto ≥ 1.5  (https://quarto.org/docs/get-started/)

quarto preview   # servidor local com live reload
quarto render    # build estático em _book/
```

## Publicação

A publicação no GitHub Pages é automática via `.github/workflows/publish.yml`. **Não usa branch `gh-pages`** — usa o novo modelo de Pages (source = "GitHub Actions").

**Setup único, manual:** em `Settings → Pages → Build and deployment`, definir **Source: GitHub Actions**.

Depois disso, todo push em `main` que tocar em arquivos relevantes dispara o workflow. Para forçar um deploy manualmente, use `Actions → Publicar (Quarto → GitHub Pages) → Run workflow`.

## Estrutura

```
.
├── _quarto.yml                # config do livro
├── _language-pt.yml           # i18n pt-BR
├── index.qmd                  # capa
├── creditos.qmd               # autor, licença, citação
├── references.qmd             # bibliografia (stub para o div#refs)
├── theme-editorial.scss       # tema (paleta, tipografia, layout)
├── styles.css                 # @font-face + overrides finos
│
├── capitulos/
│   └── parte-1-fundamentos-epistemologicos/
│       ├── 01-problema-objeto.qmd
│       ├── 02-niveis-analise.qmd
│       ├── ...
│       └── 09-pratica-reflexiva.qmd
├── apendices/                 # apêndices A, B, C
├── images/                    # cover.png e demais
├── fonts/                     # Inter, Playfair Display, JetBrains Mono (woff2)
├── references/
│   ├── references.bib
│   ├── csl_styles/            # ABNT.csl, vancouver.csl
│   └── PDFs/                  # gitignored
└── code/                      # scripts auxiliares (vazia por ora)
```
