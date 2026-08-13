# ADR-002 — Critério de escolha de fontes

**Data:** 12/08/2026

## Contexto
A primeira coisa que veio na cabeça foi usar o LinkedIn como fonte, já que é o
maior hub de vagas do mundo. Mas estudando um pouco sobre ele, percebi que a API
deles é privada — dessa forma, pra manter minha fonte de dados sempre atualizada
eu perderia muito tempo e teria muita dor de cabeça com scraping.

## Alternativas consideradas
- Usar o LinkedIn mesmo assim, e ter tempo desperdiçado com scraping que poderia
  estar destinado a estudos.
- Criar um critério de fontes que realmente me permitisse focar no que importa.

## Escolha
Só entra fonte com API pública, feed oficial ou HTML estável e permitido.

## Motivo
Mesmo abrindo mão do maior hub de vagas do mundo, ainda consigo aplicar a junção
de dados de três fontes diferentes e confiáveis, destinando meu tempo pra
aplicação dos conceitos estudados.

## O que me faria mudar de ideia
Se surgisse uma fonte muito valiosa pro projeto existindo apenas em HTML frágil,
eu gostaria de tentar explorá-la — porém apenas com o pipeline já bem estável.
Nesse início de projeto, minha preferência é destinar tempo à aplicação dos
conceitos que estou aprendendo.