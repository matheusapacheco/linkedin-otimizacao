---
name: linkedin-engajamento
description: Monta a rotina de engajamento no LinkedIn: comentários com insight em posts de terceiros e, só se o modo caça estiver ligado, conexões estratégicas, sempre parando para aprovação antes de enviar. Acione quando a pessoa disser "engajamento do dia", "acha posts para eu comentar", "quem eu conecto hoje", "rotina diária do LinkedIn", "ligar o modo caça". Em perfis com o modo caça desligado, só faz a parte de comentários.
---

# Engajamento

Alimenta os pilares de conexão e interação. Complementa o perfil e os posts, não substitui. Esta skill tem duas partes com regras diferentes: comentários (padrão) e conexões com perfis frios (modo caça, **desligado por padrão**).

## Gate humano, sem exceção

**Nunca envia convite, mensagem ou comentário sozinha.** Pesquisa, monta lista, escreve rascunho e **para**, esperando aprovação explícita numa conversa. Isso vale mesmo quando disparada por tarefa agendada: o resultado é um relatório. "Rodar a rotina" não é autorização para enviar. Cada ação aprovada é executada exatamente como foi aprovada. Aceitar aprovação parcial.

## Pré-requisitos

Ler `perfil.md` (modo caça, teto de convites por semana, discrição, vetos, "Do que NÃO falar"), `log-engajamento.md` (quem já foi contactado e em quais posts já se comentou; não repetir nos últimos 14 dias) e `palavras-chave.md` (para achar o público certo).

## Parte 1: comentários com insight (sempre disponível)

Comentar em posts de pessoas da mesma área e de líderes do setor expõe o perfil à audiência deles, que costuma ser maior.

O padrão de comentário que funciona:
- **De 2 a 4 linhas com substância.** Algo concreto: uma construção pessoal (ferramenta nomeada, o que faz, resultado), um dado ou um caso que complementa o autor.
- Nunca elogio genérico ("ótimo post!", "parabéns"), nunca só emoji.
- Nunca discordar de forma seca sem oferecer nada em troca.
- Sem polêmica, política, religião, crítica a empresa ou a pessoa. Cada comentário diz quem você é como profissional.
- Sempre no idioma do post, a menos que a pessoa decida outro.

Passos:
1. Achar de 2 a 3 posts recentes e relevantes (de preferência com menos de 48 horas), com algo real a dizer. Descartar vaga de emprego, evento, post institucional e celebração, que só rendem elogio genérico.
2. Escrever um rascunho de comentário para cada um, usando apenas fatos do `banco-de-casos.md` e do `perfil.md`.
3. Apresentar e esperar aprovação.
4. Publicar só o aprovado.

Complemento do curso: compartilhar com comentário próprio de insight, algumas vezes por semana, em vez de só curtir.

## Parte 2: modo caça (só se `perfil.md` disser ligado)

Se o modo caça estiver desligado, **não propor conexão fria**, nem insistir. Se a pessoa quiser ligar, voltar à pergunta 5.2 da skill `linkedin-entrevista` e gravar o teto.

Contexto honesto para decidir: o curso recomenda conectar com muita gente da área, inclusive recrutadores. Já uma hipótese de um perfil real (não isolada nos dados) diz que conexão com gente que nunca viu o conteúdo faz o LinkedIn testar os posts nesses perfis, que não engajam, e isso derruba o desempenho. Por isso o teto semanal existe e quem posta conteúdo deve manter o teto baixo.

Ordem de prioridade dos alvos:
1. Quem já interagiu com o perfil ou com os posts (comentou, curtiu, visitou).
2. Quem comentou nos mesmos posts em que a pessoa comentou.
3. Segundo grau com conexões em comum, mesma área ou empresa-alvo.
4. Perfis frios, só dentro do teto.

Quem buscar:
- Recrutadores especializados na área e liderança da área (gestores do cargo, quem decide contratação). Pares de mesma senioridade só para completar a lista.
- Pessoas ativas na plataforma. Perfil parado não retribui.
- Profissionais que já ocupam o cargo-alvo e pessoas das empresas-alvo.

Como buscar (do curso):
- **Pela página da empresa:** página da empresa, aba Pessoas, busca por cargo ou "recruiter". Cerca de 5 pessoas por tipo de cargo é um bom número.
- **Busca booleana:** cargo entre aspas na busca geral, filtro Pessoas, depois localidade e empresa atual.

Apresentar a lista com nome, cargo, empresa, conexões em comum e **uma linha de por que faz sentido**. Respeitar o teto semanal do `perfil.md`.

Convite: sem nota em conexão fria, porque a nota reduz a taxa de aceite. Depois que a pessoa aceita, a abordagem usa os modelos da skill `linkedin-networking-global`. Toda conexão aceita deve receber uma mensagem personalizada. Conectar e não abordar não gera relação.

## Registro

Depois de qualquer envio aprovado, gravar em `log-engajamento.md`: data, status (ENVIADO ou PROPOSTO), pessoas e posts. Esse arquivo é a memória entre execuções, porque cada rodada começa sem o contexto da conversa anterior.

```markdown
## DD/MM/AAAA | ENVIADO ou PROPOSTO
### Conexões
1. Nome | cargo | empresa | origem (interagiu, 2º grau, fria)
### Comentários
1. Autor | assunto do post | resumo do comentário
```

## Limites

- Fechar as abas que a skill abrir.
- Não compilar dados pessoais de terceiros além de nome, cargo e empresa.
- Em perfis de pessoa empregada que não sinaliza busca: nenhum comentário ou mensagem fala de procurar vaga.
- Sem travessão.
