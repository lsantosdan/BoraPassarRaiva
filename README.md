## Attribution
This project is a fork of [depuis1958](https://github.com/cljoly/depuis1958)
by Clément Joly, adapted for the 2026 Brazilian presidential election.
Licensed under AGPL-3.0.

# BoraPassarRaiva

Modelo estatístico do escrutínio uninominal majoritário em dois turnos da eleição presidencial brasileira, inspirado pelo FiveThirtyEight (e outros).

## Usar o modelo Python

O ponto de entrada é a classe `ElectionModel` (em `election.py`), que modela a probabilidade total de vitória.

## Gerar o site completo

O site é baseado em templates Jinja2. Tudo é automatizado. Para gerá-lo, crie um symlink para as pesquisas. As minhas estão aqui: https://github.com/BoraPassarRaiva/pesquisas:

    ln -s ../pesquisas/presidente/ data

Em seguida, o script `page.py` faz todo o trabalho:

    ./page.py

e gera um diretório "public" com o conteúdo HTML.
