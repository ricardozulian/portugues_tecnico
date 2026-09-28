---
name: portugues-tecnico
description: >
  Escrever, revisar e adaptar documentação técnica em português brasileiro
  (pt-BR): procedimentos, manuais de operação, relatórios, instruções para
  agentes e respostas técnicas. Transfere princípios de clareza do ASD-STE100
  para a gramática e a terminologia brasileiras, com pesquisa contextual de
  termos. Use quando o texto técnico de saída for em português brasileiro
  ou quando o usuário pedir português técnico ou linguagem técnica simples.
  Não aplicar a prosa literária, publicidade ou texto técnico em inglês.
---

# Português técnico brasileiro

Produza texto técnico que permita identificar a ação, o responsável, a condição e o resultado esperado.
Use português brasileiro natural e terminologia adequada ao domínio.

Esta skill adapta conceitos do subconjunto local `asd-ste100`.
Não é uma tradução oficial, uma norma de português controlado ou uma certificação de conformidade com ASD-STE100.

## Aplicação

Aplique a procedimentos, instruções, explicações técnicas, relatórios, planos, diagnósticos, prompts e memórias de agentes em pt-BR.
Em documentos mistos, revise apenas os trechos técnicos abrangidos pelo pedido.
Preserve código, comandos, caminhos, chaves, identificadores, mensagens de erro, citações e rótulos reais da interface.
Explique esses elementos fora do trecho literal, quando necessário.
Não reescreva comentários de código nem textos normativos sem um pedido específico.

## Processo

1. Identifique o público, o domínio e a finalidade do texto.
2. Preserve fatos, valores, condições, sequência, restrições e grau de certeza.
3. Escolha os termos pelo conceito e pelo uso brasileiro no domínio.
4. Redija com as regras abaixo.
5. Compare a revisão com o original antes de entregar.

Se faltar uma informação técnica necessária, indique a lacuna.
Não invente limites, responsáveis, evidências, resultados de testes ou condições de segurança para tornar o texto mais específico.
Uma revisão de estilo não autoriza mudar um plano ou executar as ações descritas.

## Regras essenciais

- Use voz ativa quando o responsável for conhecido. Nos passos, use o imperativo: “Abra o arquivo.”
- Escreva uma ação principal por passo. Apresente a condição antes da ação: “Se o teste falhar, interrompa a instalação.”
- Use ordem direta. Mantenha próximos o verbo, seu objeto e os complementos necessários.
- Trate 20 palavras por frase de procedimento e 25 por frase descritiva como metas editoriais. Revise parágrafos com mais de seis frases.
- Não retire condições ou termos necessários para cumprir essas metas. Esses números são convenções locais, não limites normativos do português.
- Escolha tempos verbais que preservem a relação temporal. “O teste falhou”, “O teste está falhando” e “O teste tem falhado” não são equivalentes.
- Reduza nominalizações desnecessárias: “Atualize o cadastro” em vez de “Efetue a atualização do cadastro”. Preserve nomes de processos técnicos.
- Use um termo estável para cada conceito no documento. Não varie sinônimos apenas para evitar repetição.
- Preserve artigos, preposições, concordância, regência e crase. Não imite a estrutura nominal do inglês.
- Use linguagem literal. Troque avaliações vagas por fatos disponíveis e critérios observáveis.
- Coloque avisos antes da ação à qual se aplicam. Preserve a classificação de risco do manual de origem.
- Prefira afirmações diretas. Mantenha proibições explícitas quando necessárias: “Não desconecte o cabo durante a atualização.”
- Use passos numerados para sequências e tabelas para comparações. Não transforme toda resposta curta em um procedimento.
- Diferencie obrigação, recomendação, permissão e possibilidade. Não troque “pode falhar” por “falha” nem “recomenda-se” por “deve”.

Leia [regras e transferência de conceitos](references/regras.md) ao adaptar regras do inglês ou revisar construções gramaticais.

## Terminologia

Não traduza a lista inglesa de termos preferidos e rejeitados.
Não classifique uma palavra portuguesa como incorreta apenas porque seu equivalente inglês foi desaconselhado.
“Executar”, “obter”, “verificar”, “validar” e “inspecionar” podem expressar conceitos técnicos necessários.

Leia [terminologia contextual](references/terminologia.md) ao escolher substituições.
Ela distingue evidência de uso, recomendação da fonte e decisão editorial desta skill.
Consulte [fontes e atualização](references/fontes.md) para pesquisar termos ausentes ou sujeitos a mudança.

Em cada substituição, confirme:

- O termo designa o mesmo objeto, ação ou estado?
- A fonte usa português brasileiro e trata do mesmo domínio?
- A mudança preserva a diferença entre conceitos próximos?
- O texto continua compatível com os nomes reais da interface e do produto?

Se a equivalência não estiver demonstrada, mantenha o termo técnico e acrescente uma explicação curta.
Não é necessário pesquisar novamente cada palavra comum já documentada.

### Termos em inglês

Mantenha o termo inglês quando não houver equivalente brasileiro preciso e consolidado.
Também o mantenha quando a tradução dificultar a identificação de um conceito, recurso, padrão ou elemento da interface.
O vocabulário estabelecido pela equipe ou exigido pelo usuário pode justificar sua manutenção.
Não force traduções artificiais para cumprir uma preferência pelo português.

Na primeira ocorrência, explique o termo em português se o público precisar.
Depois, use a mesma forma. Preserve grafia, capitalização e identificadores oficiais.
Use código para elementos literais e a convenção editorial do documento para termos estrangeiros em prosa.
Não transforme automaticamente um termo inglês em verbo português informal.
Veja os [critérios e exemplos de inglês técnico](references/terminologia.md#ingles-tecnico).

## Revisão final

- O leitor identifica o que deve fazer e em qual condição?
- Cada pronome tem um referente claro?
- Números, unidades, negações, quantificadores e relações temporais mantêm o sentido original?
- O texto distingue hipótese, observação e resultado confirmado?
- A terminologia é consistente sem juntar conceitos distintos?
- Os elementos literais permanecem exatos?
- Os avisos aparecem antes das ações pertinentes?

Corrija qualquer alteração de sentido antes de otimizar o estilo.
Não use uma nota de legibilidade como prova de precisão técnica.
Leia [exemplos](references/exemplos.md) para casos de aplicação e limites.
