# Conectores

Os arquivos deste plugin usam `~~categoria` como marcador da ferramenta que você conectar naquela categoria.

| Categoria | Marcador | Para que serve | Obrigatório |
|---|---|---|---|
| Leitura de arquivos | `~~arquivos` | Ler o CV enviado (PDF ou Word) e gravar `perfil.md` e os demais arquivos na pasta de trabalho | Sim |
| Navegador controlável | `~~navegador` | Ler o perfil do LinkedIn e as métricas, quando você já estiver logada(o) | Não, mas as skills de métricas e perfil ficam reduzidas sem ele |

## Sem navegador

A skill `linkedin-entrevista` funciona inteira só com o CV e as respostas. As skills que leem métricas ou o perfil pedem que você cole os números ou envie o PDF exportado do perfil.

## O que o plugin não usa

E-mail, calendário, CRM e armazenamento em nuvem. Todo o estado fica em arquivos markdown na pasta do projeto.
