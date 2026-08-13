# ADR-001 — Escolha do projeto-espinha

**Data:** 12/08/2026

## Contexto
Precisava de um projeto que crescesse tornando-se cada vez mais robusto ao longo
dos meses de estudo, em vez de vários projetos pequenos, pra ter profundidade nos
assuntos de SWE + AI Engineering.

## Alternativas consideradas

**Arquiteturas:**
- Multi-tenant com papéis — descartada por ser fraca em assíncrono
- Processamento assíncrono — descartada por ser estreita
- Agregação sobre APIs instáveis — descartada por ter pouca modelagem própria
- Histórico/versionamento — descartada por ser profunda em banco e rasa em produção
- Ingestão de fontes variadas + busca — escolhida

**Domínios:**
- Conteúdo técnico via RSS — descartado porque o dedupe seria fácil demais
- Editais — descartado por não ter dado suficiente pra índice e cache serem relevantes
- Vagas remotas internacionais — escolhido

## Escolha
Projeto de ingestão de fontes variadas + busca, no domínio de vagas remotas
internacionais.

## Motivo
A arquitetura força a prática de rate limiting, idempotência, fila, índice e cache,
além de permitir transformar o pipeline de ingestão em RAG quando eu começar a
aprender AI Engineering.

O domínio de vagas dá um dedupe desafiador entre três fontes diferentes e
normalização rica: moeda de salário, senioridade escrita de dez formas, "remote"
que às vezes é híbrido.

Por um momento cheguei a descartar vagas, porque achei que ia perder muito tempo
com scraping. Percebi que isso só aconteceria se eu usasse o LinkedIn como fonte,
e que eu poderia usar fontes com API pública ou feed.

## O que me faria mudar de ideia
Se alguma fonte fechar acesso, substituo por outra que entre nos critérios. Se
todas fecharem, o domínio deixa de sustentar o projeto e eu teria que pesquisar
novas opções.