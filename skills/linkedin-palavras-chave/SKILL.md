---
name: linkedin-palavras-chave
description: Monta a lista priorizada de palavras-chave que recrutadores e o algoritmo usam para encontrar o perfil, a partir de vagas reais, do CV e do cargo-alvo. Acione quando a pessoa disser "palavras-chave", "o que colocar no título", "como ser encontrada por recrutadores", "keywords", "meu perfil não aparece nas buscas", ou quando as skills de título, sobre, experiências ou CV precisarem da lista e palavras-chave.md não existir.
---

# Palavras-chave

Recrutadores buscam no LinkedIn como se busca no Google: por cargo, localização e termos técnicos. O perfil só aparece se tiver as palavras certas nos lugares certos. Esta skill produz a lista que as outras skills consomem.

A pergunta que guia tudo: **quais palavras um recrutador usaria para procurar um profissional como esta pessoa?** Recrutador não busca "proativo" nem "dedicado". Busca cargo, ferramenta, metodologia e especialidade.

## Pré-requisitos

Ler `perfil.md` (cargo-alvo, senioridade, mercado-alvo, idioma, ferramentas, certificações). Se não existir, acionar `linkedin-entrevista` primeiro.

## Passo 1: lista própria

Montar a partir do `perfil.md` e do CV, sem perguntar nada que já esteja lá:

- Cargo-alvo e variações de nomenclatura
- Senioridade
- Competências técnicas (hard skills)
- Ferramentas e tecnologias
- Metodologias e frameworks
- Especialidades, certificações e setores

## Passo 2: o que as vagas pedem (o passo mais importante)

Reunir cerca de 10 descrições de vagas reais do cargo-alvo, de empresas interessantes, em que a pessoa teria perfil.

- Com `~~navegador`: buscar as vagas no LinkedIn Jobs e ler as descrições.
- Sem navegador: pedir que a pessoa cole de 5 a 10 descrições.

De cada vaga, extrair cargo usado, requisitos, ferramentas e termos técnicos. Depois:

1. Contar a frequência de cada termo nas vagas.
2. Identificar a **nomenclatura de cargo mais usada**. O mercado varia (por exemplo, o mesmo papel aparece com nomes diferentes), e o termo que mais aparece é o que vai no título.
3. Separar termos em português e em inglês.

Nunca inventar frequência. Se só houver 3 vagas, dizer que a amostra é pequena.

## Passo 3: perfis de quem já ocupa o cargo

Olhar de 5 a 10 perfis de profissionais do cargo-alvo em empresas desejadas e anotar os termos que usam no título e nas competências. Este passo é complementar: perfis alheios podem estar mal preenchidos, então ele nunca sobrepõe o Passo 2.

## Passo 4: sugestão por modelo de linguagem

Usar o prompt de `references/prompt-palavras-chave.md` para gerar uma lista de apoio e cruzar com o resultado do Passo 2. O que o modelo sugerir e **não** aparecer nas vagas entra como hipótese de baixa prioridade, nunca como essencial.

## Passo 5: entregar `palavras-chave.md`

Gravar na raiz da pasta de trabalho:

```markdown
# Palavras-chave
Atualizado em: DD/MM/AAAA | Base: N vagas analisadas

## Cargo (nomenclatura que o mercado mais usa)
- Principal:
- Variação aceita (no máximo uma):
- Em inglês:

## Essenciais (3 a 5, vão no título)
termo | quantas vagas citam

## Importantes (vão no Sobre e nas experiências)
termo | quantas vagas citam

## Complementares (vão em Competências, em PT e EN)
termo PT | termo EN

## Hipóteses (apareceram só na sugestão do modelo, não nas vagas)
```

## Onde cada grupo entra

- **Título:** cargo-alvo + de 3 a 5 essenciais (skill `linkedin-titulo`).
- **Sobre:** essenciais e importantes distribuídos no texto, com os 5 principais também como competências em destaque (skill `linkedin-sobre`).
- **Experiências:** importantes que tenham conexão real com cada cargo (skill `linkedin-experiencias`).
- **Competências:** todos, em PT e EN, até 100. O mínimo recomendado pelo curso é 50 (skill `linkedin-secoes-adicionais`).
- **CV:** termos da vaga específica, sempre adaptados (skill `linkedin-cv-ats`).

## Regras

- Só entra palavra que a pessoa realmente domina. Palavra-chave sem lastro é mentira no perfil e cai na entrevista.
- Não encher de termos artificiais. Precisão técnica com naturalidade.
- Habilidade comportamental (proativo, trabalho em equipe) não entra. O LinkedIn é avaliação técnica, comportamento se avalia na entrevista.
- Nada é gravado no perfil do LinkedIn por esta skill. Ela só produz a lista.

## Validar depois de publicar

Duas ou mais semanas depois de aplicar, usar a skill `linkedin-metricas` para conferir, em ocorrências em resultados de pesquisa:

- Nos cargos usados nas buscas que acharam o perfil, **ao menos um deve ser o cargo-alvo**. Se nenhum for, as palavras escolhidas não estão acertando.
- Nos cargos de quem pesquisou, devem aparecer recrutadores ou pessoas de RH. Se não aparecem, rever as palavras.
- Perfil novo ou parado pode não mostrar esses dados ainda. Isso não é erro.

O curso sugere testar um foco de título por cerca de 15 dias e trocar se não render. Nada é definitivo.
