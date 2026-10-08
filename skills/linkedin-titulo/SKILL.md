---
name: linkedin-titulo
description: Escreve e revisa o título (headline) do LinkedIn com a fórmula cargo desejado + de 3 a 5 palavras-chave, para o perfil ser encontrado por recrutadores. Acione quando a pessoa disser "meu título", "headline", "o que colocar embaixo do meu nome", "revisa meu título", "melhorar meu título do LinkedIn", ou quando a auditoria apontar o título como correção prioritária.
---

# Título

O título é a primeira coisa que o recrutador vê, ao lado de foto e nome, na lista de resultados da busca. É com base nele que decide abrir o perfil ou passar. Por isso ele define quem você é e **o que você está buscando**, não só onde trabalha hoje.

## Pré-requisitos

Ler `perfil.md` (cargo-alvo, situação, mercado, idioma) e `palavras-chave.md`. Se `palavras-chave.md` não existir, acionar `linkedin-palavras-chave` antes. Escrever título sem essa lista é chutar.

## Fórmula

```
[Cargo desejado] | [palavra-chave 1] | [palavra-chave 2] | [palavra-chave 3] | ...
```

- **Sempre o cargo desejado**, não o atual. Se hoje é analista sênior e quer coordenar, o título leva "coordenador". Se o título tiver só o cargo atual, o perfil será encontrado para o cargo atual e nunca para o desejado.
- **De 3 a 5 palavras-chave**, separadas por barra reta. Cinco é o limite. Mais que isso vira um bloco ilegível que ninguém lê.
- As palavras-chave são as **essenciais** de `palavras-chave.md`, as que mais aparecem nas vagas da área.
- **Um cargo é o ideal.** Dois só quando o mercado usa as duas nomenclaturas para o mesmo papel. Mais de dois demonstra falta de foco.

## Casos especiais

- **Transição de carreira:** o título é obrigatoriamente da área desejada, com as tecnologias ou conhecimentos que a pessoa já estuda. Recrutador não adivinha.
- **Primeiro emprego:** escolher um cargo e uma área e estruturar tudo em volta. "Aberto a qualquer coisa" não funciona para a busca nem para o algoritmo.
- **Empregada(o) sem sinalizar busca:** o título pode usar o cargo-alvo se for da mesma função, e nunca usa "em busca de" ou "aberta(o) a".

## Idioma

Cada versão do perfil tem seu título. Perfil em inglês tem título em inglês, perfil em português tem título em português. Seguir o idioma principal definido no `perfil.md` e criar a segunda versão pela skill `linkedin-secoes-adicionais`.

## Os 4 erros a evitar

1. Só cargo e empresa, sem especialidade nem palavras-chave.
2. Genérico demais ("profissional em busca de oportunidades", "aberto a trabalho").
3. Inflado, com muitos termos e nada concreto.
4. Confuso, com várias áreas ou vários cargos ao mesmo tempo.

Extra, e que o curso não cobre: o título aceita uma prova de impacto curta, como um resultado com número, **só se couber sem inflar** e sem passar de 5 palavras-chave. Oferecer como opção, não como regra.

## Como executar

1. Ler `perfil.md` e `palavras-chave.md`.
2. Montar **3 opções** de título, cada uma com uma linha explicando a escolha (qual palavra-chave pesa mais, qual risco tem).
3. Recomendar uma e dizer por quê.
4. Rodar a revisão dos 4 erros e checar o limite de caracteres no editor do LinkedIn, que pode mudar.
5. Perguntar qual a pessoa prefere, em uma pergunta só, com as 3 opções como escolha.
6. Gravar a escolha em `perfil.md` (campo de título aprovado) com a data.

## Teste

O título não é definitivo. Manter um foco por cerca de 15 dias e conferir em `linkedin-metricas` se o cargo-alvo aparece nos cargos que acharam o perfil. Se não aparecer, trocar o conjunto de palavras e testar de novo, uma mudança por vez.

## Limites

- Não editar o título no LinkedIn sem aprovação explícita. Com navegador, só aplicar depois do OK, confirmar por screenshot e fechar a aba.
- Não usar palavra-chave que a pessoa não domina.
- Sem travessão, sem hashtag.
