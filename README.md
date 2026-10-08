# LinkedIn Otimização

Plugin para otimizar o LinkedIn com um objetivo prático: conseguir entrevistas o mais rápido possível. Ele começa lendo o seu CV, faz só as perguntas que o CV não responde e monta um diagnóstico com um plano de ação de 90 dias.

Baseado no curso LinkedIn em Ação e no ebook Carreira sem Fronteiras (Isabela Schnorr), adaptado aos dados reais de uma operação de LinkedIn em andamento.

## Status

Versão 0.2.0. As 15 skills estão escritas. Falta testar cada uma em uso real e ajustar com o que aparecer.

| Fase | Skill | O que faz |
|---|---|---|
| Entrada | `linkedin-entrevista` | Lê o CV, entrevista só o que falta e grava perfil, diagnóstico e plano de 90 dias |
| 1. Perfil | `linkedin-auditar-perfil` | Audita cada seção e prioriza as correções |
| 1. Perfil | `linkedin-palavras-chave` | Lista priorizada a partir de vagas reais |
| 1. Perfil | `linkedin-titulo` | Cargo desejado e de 3 a 5 palavras-chave |
| 1. Perfil | `linkedin-sobre` | Sobre em 6 blocos, 3 versões |
| 1. Perfil | `linkedin-experiencias` | Responsabilidades e resultados com número |
| 1. Perfil | `linkedin-secoes-adicionais` | Competências, idiomas, recomendações, Open to Work, URL, versão em outro idioma |
| 1. Perfil | `linkedin-cv-ats` | CV adaptado à vaga, compatível com ATS, e carta |
| 2. Operação | `linkedin-algoritmo-2026` | Regras de distribuição do curso, cruzadas com dados próprios |
| 2. Operação | `linkedin-metricas` | Leitura e interpretação das métricas |
| 2. Operação | `linkedin-gancho` | Gancho com dualidade, vilão externo, sem molde |
| 2. Operação | `linkedin-conteudo-semanal` | 6 ganchos, escolha de 3, escrita e agendamento com aprovação |
| 2. Operação | `linkedin-engajamento` | Comentários com insight e modo caça opcional |
| 3. Internacional | `linkedin-networking-global` | Mapeamento, abordagem e follow-up, com modelos |
| 3. Internacional | `linkedin-entrevista-star` | Respostas STAR, simulação, inglês e fit cultural |

## Ordem de uso recomendada

1. `linkedin-entrevista`: sempre primeiro. Grava o contexto que todas as outras leem.
2. `linkedin-auditar-perfil` e `linkedin-palavras-chave`: mostram o que corrigir e com quais termos.
3. `linkedin-titulo`, `linkedin-secoes-adicionais` (Open to Work e competências), `linkedin-sobre`, `linkedin-experiencias`.
4. `linkedin-cv-ats`: junto com cada candidatura.
5. `linkedin-networking-global` e, se a pessoa quiser, `linkedin-engajamento`.
6. `linkedin-metricas` todo mês, junto com o check-in da entrevista.
7. `linkedin-conteudo-semanal` e `linkedin-gancho` só para quem optou por produzir conteúdo.
8. `linkedin-entrevista-star` ao receber um convite para entrevista.

## Arquivos de contexto que o plugin cria na pasta de trabalho

`perfil.md`, `banco-de-casos.md`, `diagnostico.md`, `plano-90-dias.md`, `palavras-chave.md`, `auditoria-perfil.md`, `metricas.md`, `candidaturas.md`, `mapa-networking.md`, `log-engajamento.md`, `aprendizados-publico.md`, `entrevistas.md` e a pasta `posts/`.

## Princípios

- Uma pergunta por vez, com opções clicáveis quando couber.
- Nenhum dado inventado. O que falta fica marcado como lacuna.
- Nada é enviado ou publicado sem aprovação explícita.
- Conexão com perfis frios (modo caça) vem desligada e só liga com resposta explícita.
- Privacidade: o plugin não grava telefone, endereço, documentos nem data de nascimento.
- Alegações do curso (números de impacto) aparecem como alegações, não como fatos verificados.
- Os dados da própria pessoa valem mais que qualquer regra geral.

## Aviso sobre conteúdo de terceiros

Este repositório é para uso pessoal e deve ficar privado. Ele contém templates e estruturas derivados de material pago de terceiros (curso LinkedIn em Ação e ebook Carreira sem Fronteiras).
