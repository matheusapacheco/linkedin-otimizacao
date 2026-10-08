---
name: linkedin-sobre
description: Escreve e revisa a seção Sobre do LinkedIn na estrutura de 6 blocos, com resultados em bullets, palavras-chave distribuídas e contato, em três versões (profissional com experiência, primeiro emprego, transição de carreira). Acione quando a pessoa disser "meu Sobre", "resumo do perfil", "escreve meu about", "revisa meu Sobre", "como escrever o Sobre", ou quando a auditoria apontar o Sobre como correção prioritária.
---

# Sobre

O título atrai, o Sobre convence o recrutador a entrar em contato. Ele chega aqui depois do título, lê de forma escaneável (cerca de 6 segundos por perfil, segundo o curso) e procura quatro coisas: clareza de quem você é, coerência com o título, nível de experiência e indício de resultado.

## Pré-requisitos

Ler `perfil.md`, `banco-de-casos.md` e `palavras-chave.md`. Faltando `perfil.md`, acionar `linkedin-entrevista`. Faltando `palavras-chave.md`, acionar `linkedin-palavras-chave`.

## Escolher a versão

Pelo `perfil.md`:

- Experiência na área-alvo: **versão padrão** (6 blocos).
- Primeiro emprego ou estágio: **versão primeiro emprego** (sem resultados, com formação e projetos).
- Mudança de área: **versão transição** (competências transferíveis e estudos na área nova).

Os textos-modelo e os prompts de cada versão estão em `references/prompts-sobre.md`.

## Versão padrão: os 6 blocos

1. **Identidade profissional.** Cargo ou área principal, senioridade, tempo de experiência (quando passar de 3 ou 4 anos), setores e contextos. Quem lê já entende quem é a pessoa.
2. **Contexto de atuação.** Principais atividades, projetos e o tipo de problema que resolve. Curto.
3. **Principais resultados e entregas.** De 3 a 4 bullets, saídos do `banco-de-casos.md`, com número. Respeitar a restrição de uso de cada caso.
4. **Competências e especialidades.** Onde mais entram palavras-chave: hard skills, ferramentas, diferenciais técnicos.
5. **Direcionamento de carreira (opcional).** Só para quem pode sinalizar busca. **Se a pessoa está empregada e não quer sinalizar, omitir este bloco.**
6. **Fechamento com convite.** Aberta(o) a conexões e trocas sobre temas profissionais, com e-mail. Telefone só se a pessoa quiser.

Formato: parágrafos curtos com respiro entre eles, resultados em bullets, nada de parágrafo colado em parágrafo.

## Competências em destaque

O Sobre permite destacar até 5 competências. Usar as mesmas 5 palavras-chave essenciais do título.

## Regras de escrita

- **Técnico antes de comportamental.** O recrutador usa o LinkedIn para avaliação técnica. Comportamento se avalia na entrevista. Nada de "sou apaixonado por pessoas", "proativo", "gosto de trabalhar em equipe".
- **Sem frase genérica ou motivacional.**
- **Número real ou nada.** Resultado sem número entra como qualitativo e marcado. Nunca estimar, nunca arredondar para cima.
- **Palavras-chave de forma orgânica**, distribuídas no texto, sem lista artificial no meio.
- **Linguagem de mercado**, não jargão interno da empresa.
- **Coerência com o título.** O Sobre confirma o que o título promete.
- Sem travessão, sem hashtag.

## Como executar

1. Ler os arquivos de contexto e escolher a versão.
2. Escrever o rascunho no idioma principal do perfil.
3. Checar: os 6 blocos (ou os da versão escolhida) estão presentes? Bloco 5 respeita a discrição? Cada número vem do `banco-de-casos.md`? As palavras-chave essenciais aparecem?
4. Mostrar o texto e perguntar o que ajustar, em uma pergunta. Entender o que incomodou antes de reescrever.
5. Gerar a versão no segundo idioma, se o `perfil.md` pedir os dois. Tradução com cuidado de termos técnicos, não literal.
6. Gravar o texto aprovado em `perfil.md` (seção "Textos aprovados") com a data.

## Limites

- Não publicar no LinkedIn sem aprovação explícita. Com navegador, aplicar só depois do OK e confirmar por screenshot.
- Não incluir telefone, endereço ou dado pessoal que a pessoa não tenha autorizado.
- Não inventar resultado, tempo de experiência, empresa ou ferramenta.
