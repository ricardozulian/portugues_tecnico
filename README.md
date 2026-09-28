# Português técnico brasileiro

Skill para escrever e revisar documentação técnica em português brasileiro (`pt-BR`), com clareza e precisão.
Adapta os princípios da skill original **`asd-ste100`** à gramática e ao uso técnico brasileiro.

Use em procedimentos, manuais de operação, relatórios, diagnósticos, planos, instruções para agentes e respostas técnicas.
O objetivo é tornar explícitos a ação, o responsável, as condições e o resultado esperado, sem alterar o conteúdo técnico.

## Origem e atribuição

Este projeto deriva conceitualmente da skill **`asd-ste100`**, do projeto **ASD-STE100**, descrita como “ASD-STE100 for technical literature”.
A adaptação tomou como referência estes arquivos da skill original:

- `/SKILL.md` — escopo e regras principais;
- `asd-ste100/references/rules.md` — regras de redação;
- `asd-ste100/references/words.md` — critérios de vocabulário;
- `asd-ste100/references/examples.md` — exemplos de aplicação.

A skill original apresenta um subconjunto prático de Simplified Technical English para agentes.
Seu README e seu `SKILL.md` indicam a licença MIT.
Essa informação descreve a origem; não estabelece uma licença para este repositório.

O endereço público do repositório original não consta da cópia local usada nesta adaptação.
A atribuição acima identifica a skill e os arquivos consultados.

**Esta adaptação não é uma tradução oficial da norma ASD-STE100 nem uma certificação de conformidade.**
O [mapa de transferência dos conceitos](portugues-tecnico/references/regras.md) documenta as decisões de adaptação.

## O que foi adaptado

| Princípio de origem | Aplicação em pt-BR |
|---|---|
| Voz ativa e instruções diretas | Imperativo nos passos e identificação do responsável quando necessário. |
| Frases curtas | Metas editoriais de extensão, sem retirar condições ou informações essenciais. |
| Vocabulário consistente | Um termo estável por conceito no documento, respeitando o domínio técnico. |
| Restrições gramaticais do inglês | Regras próprias para tempos verbais, gerúndio, artigos, preposições e concordância em português. |
| Avisos antes das ações | Preservação da sequência e da classificação de risco do documento de origem. |
| Elementos técnicos literais | Preservação de código, comandos, caminhos, identificadores, mensagens e citações. |

A lista inglesa de termos preferidos e desaconselhados não foi traduzida diretamente.
As escolhas em português consideram o conceito, o público e o uso documentado no Brasil.
O [guia de terminologia](portugues-tecnico/references/terminologia.md) distingue recomendações das fontes, evidências de uso e decisões editoriais do projeto.

## Termos em inglês

A skill permite termos em inglês quando não existe equivalente brasileiro preciso e consolidado.
Também os preserva quando a tradução dificulta reconhecer um conceito, um recurso ou um elemento da interface.
O vocabulário estabelecido pela equipe pode justificar a manutenção do termo.

Explique termos desconhecidos na primeira ocorrência e mantenha a mesma forma no restante do documento.
Não force traduções artificiais.
Rótulos como **Retry**, chaves como `request_timeout` e mensagens de erro permanecem exatos.

## Instalação no Codex

Copie a pasta `portugues-tecnico` inteira para o diretório de skills da sua instalação.
Use `$CODEX_HOME/skills` quando `CODEX_HOME` estiver definido; caso contrário, use `~/.codex/skills`.

No PowerShell, execute o bloco abaixo na raiz deste repositório.
Ele interrompe a instalação se a pasta de destino já existir.

```powershell
$skillSource = Join-Path (Get-Location) 'portugues-tecnico'
$skillRoot = if ($env:CODEX_HOME) {
    Join-Path $env:CODEX_HOME 'skills'
} else {
    Join-Path $env:USERPROFILE '.codex\skills'
}
$skillDestination = Join-Path $skillRoot 'portugues-tecnico'

if (-not (Test-Path -LiteralPath (Join-Path $skillSource 'SKILL.md'))) {
    throw 'Execute este bloco na raiz do repositório.'
}
if (Test-Path -LiteralPath $skillDestination) {
    throw 'A skill já existe no destino. Compare as versões antes de atualizar.'
}

New-Item -ItemType Directory -Path $skillRoot -Force | Out-Null
Copy-Item -LiteralPath $skillSource -Destination $skillDestination -Recurse -ErrorAction Stop
```

## Uso

Depois da instalação, invoque a skill em uma nova mensagem:

```text
Use $portugues-tecnico para revisar este procedimento em pt-BR.
Preserve o significado, os comandos e os termos ingleses necessários.
```

Outros exemplos:

```text
Use $portugues-tecnico para adaptar este manual ao público brasileiro.
Pesquise os termos técnicos cuja equivalência seja incerta.
```

```text
Use $portugues-tecnico para simplificar este relatório.
Preserve as diferenças entre hipótese, observação e resultado confirmado.
```

## Exemplo de revisão

Texto de entrada:

> Depois que a cópia terminar, deverá ser efetuada a reinicialização do serviço e a verificação do código HTTP, que deve ser 200.

Texto revisado:

> Após o término da cópia:
>
> 1. Reinicie o serviço.
> 2. Confira o código HTTP retornado.
>
> Resultado esperado: `200`.

A revisão preserva a condição inicial e distingue o resultado esperado de um resultado observado.
Consulte os [demais exemplos](portugues-tecnico/references/exemplos.md).

## Arquivos

| Arquivo | Conteúdo |
|---|---|
| [SKILL.md](portugues-tecnico/SKILL.md) | Escopo, processo e regras essenciais. |
| [regras.md](portugues-tecnico/references/regras.md) | Transferência de conceitos e particularidades do português. |
| [terminologia.md](portugues-tecnico/references/terminologia.md) | Escolhas contextuais, distinções técnicas e uso de inglês. |
| [fontes.md](portugues-tecnico/references/fontes.md) | Referências, datas de consulta e limites das evidências. |
| [exemplos.md](portugues-tecnico/references/exemplos.md) | Casos de revisão e preservação do significado. |
| [openai.yaml](portugues-tecnico/agents/openai.yaml) | Nome e instrução de uso exibidos na interface. |

## Fontes e contribuições

As referências incluem materiais do Senado Federal, LA-BORA! gov, ANA, CERT.br/NIC.br, ITI, Inmetro e documentação de fabricantes em pt-BR.
Consulte o [registro de fontes](portugues-tecnico/references/fontes.md) para os links e o alcance de cada referência.

Ao propor um novo termo, informe o conceito, o domínio, a fonte brasileira, a data da consulta e os limites da substituição.
Distinga uma preferência editorial de uma definição normativa.
Não trate uma ocorrência isolada como prova de equivalência em todos os contextos.

## Limites

A skill não se destina a prosa literária ou publicidade.
Uma revisão de estilo não autoriza mudar arquitetura, planos aprovados, requisitos ou ações operacionais.
Ela também não substitui a revisão técnica do domínio nem comprova que um procedimento foi executado.
