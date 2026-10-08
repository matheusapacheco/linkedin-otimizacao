---
name: linkedin-conteudo-semanal
description: Roda a rotina semanal de conteúdo do LinkedIn: lê o desempenho da semana, sugere 6 ganchos prontos, a pessoa escolhe 3, escreve os escolhidos e agenda no agendador nativo do LinkedIn com aprovação. Acione quando a pessoa disser "planejamento da semana", "o que eu posto essa semana", "me dá ideias de post", "bora fazer o conteúdo", "agenda meus posts", ou quando uma tarefa semanal disparar. Só vale para quem optou por produzir conteúdo no perfil.md.
---

# Conteúdo semanal

Rotina de uma semana de conteúdo, do dado ao agendamento. Só roda se `perfil.md` disser que a pessoa quer postar. Quem não quer postar usa só as skills de perfil e rede.

## Gate humano, sem exceção

A skill **nunca agenda nem publica sem a pessoa aprovar o texto final**. Mesmo quando disparada por tarefa agendada, o resultado é um relatório com sugestões, e a execução acontece depois da revisão.

## Pré-requisitos

Ler `perfil.md` (cadência, dias, horário, temas, "Do que NÃO falar", discrição), `banco-de-casos.md` e `aprendizados-publico.md`. Se `perfil.md` não existir, acionar `linkedin-entrevista`.

## Passo 0: ler o desempenho (obrigatório)

Acionar `linkedin-metricas` para os posts da semana anterior, e **ler os comentários**. Eles entregam tema novo, objeção, vocabulário do público e, muitas vezes, o gancho do próximo post. Discordância densa de alguém sênior é sinal de território disputado.

Registrar em `aprendizados-publico.md`: números crus em tabela, leitura do que funcionou e do que não, e o que muda na escolha de assuntos. Cuidado: uma semana com mais de uma variável mudada não permite conclusão limpa, dizer isso.

Se faltou post na semana (cadência quebrada), registrar isso primeiro. Constância é prioridade antes de qualquer leitura de gancho ou formato.

## Passo 1: assuntos já usados

Checar `banco-de-casos.md` ("última vez usado") e `aprendizados-publico.md`. Reutilizar caso é permitido. O que não se aceita é gancho fraco. A fonte de assunto segue a ordem da skill `linkedin-gancho` (assunto que viralizou com ângulo novo, post fraco com gancho novo, caso inédito).

## Passo 2: 6 sugestões como ganchos prontos

Entregar 6 sugestões. Cada uma é **a frase do gancho de verdade**, mais uma linha com o ângulo e qual caso entra como prova. Nunca rótulo de método ("tipo, pilar, variável"), porque foi exatamente isso que fez uma rodada inteira de sugestões sair inútil.

Regras da curadoria:
- Variar o assunto. No máximo 1 em 3 posts da semana sobre o mesmo assunto da moda.
- Todo tema orbita o posicionamento do cargo-alvo. Tema fora da especialidade perde distribuição.
- Priorizar o que veio dos comentários, porque já tem demanda.
- Respeitar "Do que NÃO falar" e a discrição do `perfil.md`.
- Passar cada gancho pelo teste do vilão externo (ver `linkedin-gancho`).

**Entregar as 6 e parar.** A pessoa escolhe 3. Se ela rejeitar todas, entender o que não funcionou antes de gerar novas.

## Passo 3: escrever os 3 escolhidos

Acionar `linkedin-gancho` para cada um. Salvar em `posts/AAAA-MM-DD-slug/legenda.txt`.

## Passo 4: aprovação

Mostrar o texto final e esperar aprovação explícita de cada post. Se pedir ajuste de gancho, entender o que incomodou antes de reescrever.

## Passo 5: agendar

Com `~~navegador`, abrir o compositor do LinkedIn e usar o **agendador nativo** (ícone de relógio), um post por dia fixo da cadência do `perfil.md`.

Notas operacionais:
- O compositor roda em shadow DOM. Validar sempre por screenshot, nunca por inspeção de DOM.
- Texto com link gera um cartão de preview que **bloqueia upload de vídeo**. Remover o cartão antes de subir mídia. O link continua valendo no corpo.
- O campo de arquivo costuma estar oculto no shadow DOM. Se o upload por automação falhar, pedir que a pessoa suba a mídia manualmente em vez de insistir.
- Confirmar por screenshot a data e a hora antes de fechar.
- Documento (PDF) exige título.
- Fechar as abas que a rotina abriu.

## Passo 6: registrar

Atualizar `aprendizados-publico.md` com a leva agendada, os ganchos escolhidos e qualquer experimento em curso. Atualizar o "última vez usado" dos casos. Se houver experimento, registrar qual é a variável e o que se espera aprender, e **uma variável por semana**.

## O que esta skill não faz

- Não cria protocolo de testes, variáveis de redação nem checklist de escrita por conta própria. Se a pessoa pedir um experimento, registrar o que ela pediu.
- Não propõe táticas que a pessoa vetou (priming, DM para pares, conexão fria). Se `perfil.md` listar vetos, respeitar.
- Sem travessão, sem hashtag.
