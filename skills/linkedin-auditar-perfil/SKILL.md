---
name: linkedin-auditar-perfil
description: Audita o perfil do LinkedIn seção por seção contra os critérios do curso e do mercado, e entrega uma lista priorizada pelo impacto em conseguir entrevistas. Acione quando a pessoa disser "audita meu perfil", "revisa meu LinkedIn", "o que está errado no meu perfil", "o que eu mudo primeiro", "meu perfil está bom?", ou logo depois da skill linkedin-entrevista quando o diagnóstico apontar o perfil como gap.
---

# Auditar perfil

Compara cada seção do perfil com o que o recrutador e o algoritmo valorizam e devolve o que corrigir primeiro. O recrutador passa em média cerca de 6 segundos em um perfil (segundo o curso), então a ordem das correções importa mais que a quantidade.

## Pré-requisitos

- `perfil.md` e, se existir, `palavras-chave.md`. Sem `perfil.md`, acionar `linkedin-entrevista`.
- O conteúdo do perfil por uma destas vias: `~~navegador` com a pessoa logada, PDF exportado do perfil, ou texto colado seção por seção. Se for pelo navegador, validar por screenshot e fechar as abas que a skill abrir.

Nunca avaliar de memória. Se uma seção não foi lida, ela entra como `[NÃO LIDA]`.

## Como avaliar

Para cada seção abaixo: dar nota **ok**, **ajustar** ou **refazer**, citar a evidência (o que está escrito hoje) e a correção. Os critérios abaixo vêm do curso LinkedIn em Ação.

| Seção | O que precisa estar certo |
|---|---|
| Foto | Rosto visível e centralizado, do peito para cima, boa iluminação, fundo neutro, roupa adequada à área, expressão acessível, foto atual, sem filtro. Selfie, óculos escuros, foto cortada ou de festa reprovam. |
| Capa | Limpa, neutra, pouco texto, em linguagem de mercado. Não influencia o algoritmo, mas influencia a impressão. Quem está empregado pode usar a capa da empresa. |
| Título | Cargo desejado + de 3 a 5 palavras-chave, separados por barra. No máximo 2 cargos. Sem "aberto a oportunidades", sem termos inflados. Ver `linkedin-titulo`. |
| Sobre | Estrutura em blocos, escaneável, com resultados em bullets, palavras-chave distribuídas e contato. Sem soft skills em excesso, sem frase motivacional. Ver `linkedin-sobre`. |
| Experiências | Responsabilidades separadas de resultados, em bullets, mais detalhe nas 2 ou 3 mais recentes, cargo na nomenclatura do mercado, empresa ligada à página, todos os cargos da mesma empresa listados. Ver `linkedin-experiencias`. |
| Competências | De 50 a 100, técnicas antes de comportamentais, em português e em inglês. |
| Idiomas | Português (nativo), inglês com nível, outros se houver. Recrutadores filtram por idioma. |
| Recomendações | Mais de 5, segundo o curso. |
| Certificações e cursos | Só relevantes e recentes, no formato "Nome do curso - Instituição (ano)". |
| Formação | Só formação formal, ano de início basta. |
| Versão em outro idioma | Título, Sobre e Experiências traduzidos. Competências não traduzem sozinhas. |
| URL | Curta e limpa, de preferência nome e sobrenome. |
| Open to Work | Ligado só para recrutadores, sem selo na foto. |
| Perfil completo | Quanto mais seções bem preenchidas, melhor para a marca profissional. |

Critérios adicionais para checar:

- **Coerência:** título, Sobre e experiências contam a mesma história e apontam para o cargo-alvo do `perfil.md`.
- **Datas:** comparar com o CV e, se houver, com o portfólio. Divergência entra como pergunta, não como correção silenciosa.
- **Discrição:** se a pessoa está empregada e não quer sinalizar busca, marcar qualquer trecho que sinalize.
- **Idioma:** o idioma principal do perfil bate com o mercado-alvo?

## Priorização (o que entrega entrevista mais rápido)

Ordenar as correções por impacto, nesta lógica:

1. **Título e palavras-chave:** é o que aparece na lista do recrutador e define se o perfil é achado.
2. **Open to Work só para recrutadores.**
3. **Sobre e experiências com resultado e número.**
4. **Competências em PT e EN, idiomas e URL.**
5. **Foto, capa, recomendações e certificações.**

No máximo 5 correções por rodada. Mais que isso paralisa.

## Entrega

Gravar `auditoria-perfil.md` na raiz:

```markdown
# Auditoria do perfil
Data: DD/MM/AAAA | Fonte lida: navegador | PDF | texto colado

| Seção | Nota | Evidência | Correção | Skill |
|---|---|---|---|---|

## As 5 primeiras correções, em ordem
1.
```

Mostrar na conversa só as 5 correções e o ponto mais forte do perfil. Perguntar qual seção atacar primeiro e acionar a skill correspondente.

## Limites

- Não alterar o perfil do LinkedIn por esta skill. Ela só audita.
- Números citados do curso (por exemplo, o impacto de foto ou de recomendações) são alegações do curso, não dados verificados. Apresentar como "segundo o curso".
- Não inventar o que está faltando. Dado ausente vira lacuna.
