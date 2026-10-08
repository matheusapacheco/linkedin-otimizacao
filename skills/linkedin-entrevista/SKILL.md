---
name: linkedin-entrevista
description: Onboarding do plugin. Lê o CV da pessoa, entende quem ela é e conduz uma entrevista curta, uma pergunta por vez, só sobre o que o CV não responde, para gerar diagnóstico, perfil.md, banco-de-casos.md e um plano de ação de 90 dias focado em conseguir entrevistas rápido. Acione na PRIMEIRA vez que qualquer skill do plugin for usada e perfil.md não existir. Acione também quando a pessoa disser "otimizar meu LinkedIn", "por onde eu começo", "quero conseguir entrevistas", "montar meu plano", "atualizar meu perfil de contexto", "mudei de objetivo", ou quando pedir o check-in mensal.
---

# LinkedIn: entrevista de onboarding

Esta skill é a porta de entrada do plugin. Tudo que ela grava é lido pelas outras skills, então o que ela captura define a qualidade do resultado. O objetivo prático é um só: deixar o perfil pronto para gerar entrevistas o mais rápido possível, perguntando o mínimo indispensável.

## Regras que valem o tempo todo

1. **Uma pergunta por vez.** Nunca duas na mesma mensagem.
2. **Opções clicáveis sempre que a resposta couber em 2 a 4 alternativas.** No chat, usar o seletor de opções (ask_user_input_v0). No Claude Code, AskUserQuestion. Se nenhuma dessas ferramentas existir, listar as opções numeradas no texto. Se a resposta for aberta (link, cargo exato, número de um resultado), perguntar em texto livre.
3. **Nunca perguntar o que o CV já respondeu.** Confirmar, não repetir.
4. **Nunca inventar dado.** O que não foi dito nem está no CV é gravado como `[LACUNA]`.
5. **Pular é permitido.** "Pular" marca a lacuna e segue.
6. **Gravar a cada resposta** no `perfil.md`, para a pessoa poder pausar e retomar.
7. **Privacidade.** Gravar só o que serve à otimização. Não gravar telefone, endereço, data de nascimento, estado civil, número de documento nem passaporte. Sobre passaporte, perguntar apenas se está válido (sim ou não).
8. **Tom humano e direto.** Português do Brasil por padrão, no idioma em que a pessoa escrever. Sem travessão. Sem preâmbulo de assistente.

## Passo 0: checar o que já existe

Antes de qualquer pergunta, procurar `perfil.md`, `banco-de-casos.md`, `diagnostico.md` e `plano-90-dias.md` na pasta de trabalho.

- Se `perfil.md` existir: ler, mostrar em 3 linhas o que está registrado e perguntar só "mudou alguma coisa?". Se a pessoa disser que sim, perguntar o que mudou e atualizar. Se disser que não, encerrar a entrevista e sugerir a próxima skill (Passo 8).
- Se existir mas estiver com `[LACUNA]`, perguntar só as lacunas, na ordem de impacto (ver `references/perguntas.md`).
- Se não existir, seguir para o Passo 1.

## Passo 1: pedir o CV

Abrir com uma mensagem curta, pedindo:

1. O CV (PDF ou Word).
2. Se tiver, o link do LinkedIn ou o PDF exportado do perfil.

Explicar em uma frase o porquê: "Com o CV eu já entendo sua área, senioridade e resultados, e pergunto só o que faltar."

Se a pessoa não tiver CV, ou preferir não enviar, ir direto para o Passo 5 com o roteiro completo de `references/perguntas.md`.

## Passo 2: ler o CV

Extrair, sem perguntar nada ainda:

- Cargo atual, área e senioridade percebida
- Tempo de experiência total e por empresa
- Empresas, cargos e períodos
- Resultados com número (marcar o que é número real e o que é só adjetivo)
- Ferramentas, tecnologias, metodologias, certificações
- Idiomas e níveis
- Formação
- Cargo-alvo, se o CV declarar um objetivo

Se houver link ou export do LinkedIn, ler também e **comparar com o CV**. Quando divergirem (cargo, datas, resultados), anotar a divergência e perguntar qual vale no Passo 3.

## Passo 3: confirmar o que foi entendido

Mostrar o que entendi em até 8 linhas curtas e pedir correção. Usar este formato:

- Cargo e área
- Senioridade e anos de experiência
- Empresas mais recentes
- Resultados com número encontrados (quantos)
- Ferramentas e idiomas
- O que NÃO consegui ler ou está ambíguo

Só depois do OK da pessoa gravar no `perfil.md`. Se ela corrigir, aplicar a correção e seguir sem pedir novo OK.

## Passo 4: diagnóstico rápido

Dar em poucas linhas o que no CV já está forte e o que mais atrapalha a pessoa a conseguir entrevistas. Os bloqueios mais comuns, na ordem em que costumam pesar:

1. Cargo vago ou genérico, sem foco em uma função
2. Experiências que são lista de tarefas, sem resultado
3. Resultados sem número
4. Poucas palavras-chave que o mercado usa nas vagas
5. Trajetória confusa ou sem coerência com o cargo-alvo
6. Idioma do material diferente do idioma do mercado-alvo
7. Formatação que ATS não lê (colunas, tabelas, gráficos)

Apresentar como hipótese, não como sentença. A confirmação vem com os dados do LinkedIn e do mercado nas outras skills.

## Passo 5: entrevistar só o que falta

Consultar `references/perguntas.md`. Lá cada pergunta tem um nível:

- **A (indispensável):** sem isso não dá para otimizar para entrevista. Sempre perguntar se o CV não respondeu.
- **B (útil):** melhora o resultado. Perguntar depois das A.
- **C (conforto):** tom, temas e cadência de conteúdo. Deixar para depois e só se a pessoa quiser postar.

Regras da condução:

- Ordem: A, depois B. Parar quando as A estiverem completas e perguntar: "Já dá para começar a otimizar. Quer responder mais algumas perguntas para refinar, ou prefere ver o diagnóstico agora?"
- **Ramificações:** seguir as regras de `references/perguntas.md` (empregada ou não, primeiro emprego, transição, mercado internacional, modo caça).
- Perguntas com mais de 4 respostas possíveis: quebrar em duas etapas.
- Dados que só a pessoa sabe (link do perfil, números dos resultados): texto livre, uma pergunta por vez, com um exemplo curto do formato esperado.
- Para resultados com número, pedir um de cada vez: "Qual foi o resultado, com o número, e o que você fez para chegar nele?". Pedir de 3 a 5 no total, nunca mais que isso nesta etapa.

## Passo 6: resumo e confirmação

Antes de gravar a versão final, mostrar o resumo do `perfil.md` em formato escaneável e perguntar se está certo. Marcar claramente o que ficou como `[LACUNA]` e o impacto de cada lacuna no resultado.

## Passo 7: gravar os arquivos

Criar ou atualizar na raiz da pasta de trabalho, usando os modelos de `references/modelos.md`:

- `perfil.md`: quem é, objetivo, mercado-alvo, restrições, preferências de operação, modo caça (padrão desligado)
- `banco-de-casos.md`: um bloco por resultado, com contexto, decisão, número, restrição de uso e campo "última vez usado" vazio
- `diagnostico.md`: nível de preparo, 2 ou 3 gaps críticos e estratégia recomendada
- `plano-90-dias.md`: plano de ação a partir do ponto de partida real

Não criar arquivo de conteúdo (aprendizados, log de engajamento) agora. Quem cria é a skill que usa.

## Passo 8: entregar o diagnóstico e o plano

Apresentar, nesta ordem e de forma curta:

1. **Nível de preparo** (em faixas, sem julgamento de valor): pronta para aplicar agora, precisa de ajustes de 2 a 4 semanas, ou precisa de preparação maior.
2. **Os 2 ou 3 gaps que mais limitam hoje.** Nunca mais que três. Tentar corrigir tudo ao mesmo tempo é o erro mais comum.
3. **Estratégia recomendada**: remoto, relocação, híbrido ou recolocação local, com uma frase de justificativa.
4. **Plano de 90 dias** (ver estrutura abaixo).
5. **A primeira ação** e qual skill rodar agora.

### Estrutura do plano de 90 dias

O plano é montado a partir do ponto de partida da pessoa, não de um modelo fixo. A ordem vai do que o recrutador vê e do que faz o perfil aparecer na busca para o que demora mais a dar retorno.

- **Dias 1 a 30: base que gera entrevista.** Corrigir o gap mais crítico. Título com cargo-alvo e palavras-chave. Open to Work visível só para recrutadores, sem selo na foto. Sobre, experiências com resultado, competências em PT e EN, idiomas, URL limpa, foto e capa. CV em versão compatível com ATS.
- **Dias 31 a 60: posicionamento e rede.** Ajustar o posicionamento com base nos primeiros dados. Mapear empresas-alvo, cargos e pessoas-chave. Começar o networking estratégico (e o modo caça, se a pessoa tiver ligado). Conteúdo só se a pessoa quiser postar.
- **Dias 61 a 90: candidaturas e entrevistas.** Primeiras candidaturas estratégicas e abordagens personalizadas. Preparação de entrevista (STAR). Coleta de feedback do mercado e ajuste de rota.

Cada fase termina com métricas de acompanhamento: visualizações do perfil, ocorrências em resultados de pesquisa e cargos buscados, conexões qualificadas, candidaturas, taxa de resposta e convites para entrevista. Se a pessoa ainda tiver acesso ao SSI, incluir. Se não, não depender dele.

## Modo check-in mensal

Quando a pessoa pedir "check-in" ou passar 30 dias do último, fazer só 3 perguntas, uma por vez:

1. Quais números mudaram (visualizações, ocorrências em pesquisa, candidaturas, respostas, entrevistas)?
2. Mudou alguma coisa no objetivo, na situação ou na disponibilidade?
3. O que travou neste mês?

Atualizar `perfil.md` e `plano-90-dias.md`. Tratar recusa como dado de mercado: cada resposta negativa informa sobre adequação à vaga, clareza de posicionamento, preparo ou estratégia de abordagem. Ajustar a rota sem abandonar o projeto.

## Limites

- Não escrever o perfil nesta skill. Esta skill diagnostica, grava o contexto e aponta a próxima skill.
- Não prometer prazo de resultado. O plano é de 90 dias de trabalho, não garantia de entrevista.
- Não enviar convite, mensagem ou candidatura. Isso é de outras skills, sempre com aprovação explícita da pessoa.
- Fechar as abas de navegador que a skill abrir, se abrir alguma.
