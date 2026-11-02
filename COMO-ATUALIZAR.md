# Como atualizar o site

O site é um único `index.html` que lê os arquivos da pasta `data/`. Para mudar algo, edite só um desses arquivos direto no GitHub (botão do lápis) e faça commit. Não precisa de programa nenhum.

| Seção | Arquivo |
|---|---|
| Patentes | `data/patentes.json` |
| Artigos | `data/artigos.json` |
| Prêmios | `data/premios.json` |
| Formação | `data/formacao.json` |
| Certificações | `data/certificacoes.json` |
| Comunidade | `data/comunidade.json` |
| Entrevistas | `data/entrevistas.json` (dividido em seções: imprensa, TV, podcasts, palestras) |

## Adicionar um prêmio, artigo ou formação
Copie um bloco `{ ... }` existente, cole logo abaixo (com vírgula entre os blocos), e troque os textos.

## Adicionar uma patente
Copie um bloco de `data/patentes.json` e ajuste:

- `status`: `"concedida"` ou `"pedido"`
- `concedidas_us`: patentes concedidas nos EUA (`numero` e `data`)
- `publicacoes_us`: pedidos publicados nos EUA
- `fora_dos_eua`: outros países, com `status` `"concedida"` ou `"publicada"`

Quando um pedido virar patente concedida, mova o número para `concedidas_us` e mude `status` para `"concedida"`. Atualize também `atualizado_em` no topo do arquivo.

## Dica
Se der erro na página depois de editar, quase sempre é uma vírgula faltando ou sobrando. Cole o arquivo em jsonlint.com para achar a linha.
