---
name: linkedin-metricas
description: Lê e interpreta as métricas reais do LinkedIn (visualizações do perfil, ocorrências em pesquisa, cargos buscados, desempenho por post, audiência) e transforma em decisão. Acione quando a pessoa disser "como está meu perfil", "quantas visualizações", "estou aparecendo nas buscas", "analisa meu desempenho", "como foi meu post", "check-in do mês", ou quando o planejamento semanal ou o plano de 90 dias precisar de dados.
---

# Métricas

Sem dado, o plano vira achismo. Esta skill coleta o número real, interpreta e grava em `metricas.md`. Nunca só reporta: sempre entrega o que o número significa e o que fazer.

## Onde buscar

Com `~~navegador` e a pessoa logada, ou com números colados por ela.

**Área de análise do perfil (Eu, Ver perfil, seção só visível ao dono):**
- **Visualizações do perfil:** sempre dos últimos 90 dias.
- **Ocorrências em resultados de pesquisa:** sempre dos últimos 7 dias, atualizada uma vez por semana. Dentro dela:
  - onde o perfil apareceu (publicação, comentário, pesquisa, recomendações da rede);
  - as principais empresas de quem pesquisou;
  - os principais cargos de quem pesquisou;
  - **os cargos usados na pesquisa que encontrou o perfil**.

**Análise de conteúdo (se a pessoa publica):** por post, impressões, reações, comentários, compartilhamentos, salvamentos, envios, visitas ao perfil geradas e seguidores ganhos. Agregado de 7, 28 ou 90 dias. Audiência: cargo, senioridade, setor, localidade, tamanho de empresa.

**Social selling index (SSI):** só se a pessoa ainda tiver acesso. Pode ter sido descontinuado para perfis gratuitos. Não depender dele.

Sempre validar por screenshot, porque a interface carrega tarde e leitura de DOM sozinha devolve dado incompleto. Fechar as abas que a skill abrir.

## Como interpretar (regras do curso)

- **Cargo dos pesquisadores:** devem aparecer recrutadores ou pessoas de RH. Se nenhum aparece, as palavras-chave podem estar erradas.
- **Cargos usados na pesquisa:** é comum aparecerem cargos aleatórios. O que importa é que **pelo menos um seja o cargo-alvo**. O LinkedIn usa nomes padrão da plataforma, então não espere a nomenclatura exata do perfil.
- **Perfil novo, parado ou com pouca atividade** pode não mostrar esses dados porque falta volume para o LinkedIn calcular. Não é erro, é sinal para ganhar atividade.
- **Não existe número ideal** de ocorrências. Varia com senioridade, localização e demanda da área. Pessoas em cargos muito altos ou muito baixos aparecem menos. O que importa é a **tendência semana a semana**.

## Como interpretar (regras de leitura de dados)

- **Procurar padrão, não total.** Em conteúdo orgânico é normal 2 posts concentrarem 80% do alcance do mês. O total esconde isso. O que importa é o que separa os acertos dos fracassos.
- **Cruzar ao menos duas variáveis.** Um post fraco isolado não diz nada. Comparar posts da mesma pessoa, na mesma semana, com resultados de ordens de grandeza diferentes.
- **Ler os comentários, não só contar.** Discordância densa de alguém sênior vale mais que dez concordâncias: indica território disputado, de onde vem tema novo.
- **Comparar salvamento com comentário.** Salvamento indica utilidade, comentário indica debate. Cada perfil tem um motor dominante.
- **Janela fixa de leitura.** Ler cada post sempre na mesma janela (por exemplo, 48 horas depois), porque a impressão continua subindo e comparar janelas diferentes engana. Todo número é um piso.
- **Experimento sujo:** se mais de uma variável mudou entre semanas (dia, formato, gancho), avisar e dizer o que não dá para concluir. Admitir isso é melhor que gravar uma causa falsa.
- **Comentário que a tela mostra mas o post não exibe:** tratar como não confirmado.

## Horário exato de uma publicação (truque técnico)

O identificador numérico da publicação carrega o horário de criação. Em JavaScript: `new Date(Number(BigInt(idDaPublicacao) >> 22n))`. O identificador aparece nos atributos do post e nos links de análise. Serve para cruzar horário real com desempenho.

## O que o LinkedIn não entrega

- Horário de atividade da audiência para perfil pessoal (só demografia).
- Em alguns períodos, alcance e percentual dentro e fora da rede por publicação deixaram de aparecer. Usar impressão por post contra a mediana da própria conta como substituto.

## Registro

Gravar em `metricas.md`, com a data de cada leitura:

```markdown
# Métricas
## Perfil
| Data | Visualizações (90d) | Ocorrências em pesquisa (7d) | Cargo-alvo nos cargos buscados | Recrutador nos cargos de quem buscou |
|---|---|---|---|---|

## Rede e candidaturas (revisão mensal)
| Mês | Conexões qualificadas novas | Candidaturas | Respostas | Convites para entrevista |
|---|---|---|---|---|

## Posts (se publica)
| Data | Gancho | Impressões (48h) | Reações | Comentários | Salvamentos | Seguidores |
|---|---|---|---|---|---|---|

## Leitura e decisão
Data, o que os números dizem, o que muda no plano.
```

## Cadência

Mensal para perfil, rede e candidaturas, junto com o check-in da skill `linkedin-entrevista`. Semanal para posts, se a pessoa publica, antes de planejar a semana seguinte. Observar a tendência e não reagir a um dia ruim.

## Limites

- Não inventar métrica. Dado não visível vira `[NÃO DISPONÍVEL]`.
- Não prometer resultado a partir de número.
- Sem travessão.
