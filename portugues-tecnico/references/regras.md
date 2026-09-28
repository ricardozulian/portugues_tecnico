# Transferência de conceitos para pt-BR

Origem: `asd-ste100/SKILL.md` e seus arquivos `references/rules.md`, `references/words.md` e `references/examples.md`, no projeto ASD-STE100.
A origem é um subconjunto para agentes; não representa o conteúdo integral da norma.
As decisões abaixo são adaptações editoriais desta skill.

## Correspondência

| Conceito do subconjunto de origem | Aplicação em português brasileiro |
|---|---|
| Voz ativa; imperativo nas instruções | Manter. Use “Registre a pressão”. Em descrições, identifique quem registra quando isso for relevante e conhecido. |
| Uma instrução por frase | Manter como uma ação principal por passo. A condição pode ficar na mesma frase. |
| Limites de 20/25 palavras e seis frases | Usar como metas de revisão. Não são limites comprovados para todo texto brasileiro. |
| Tempos simples; restrição a tempos perfeitos do inglês | Adaptar ao sentido temporal. O pretérito perfeito português, como “concluiu”, é normal e não está proibido. |
| Restrição a formas em “-ing” | Não transferir como proibição do gerúndio português. Retirar perífrases vazias e preservar duração ou simultaneidade. |
| Manter artigos | Manter os artigos e as relações expressas por preposições e contrações. Evitar texto telegráfico. |
| Um termo, um significado | Manter consistência no domínio e no documento. Não exigir que uma palavra tenha um único sentido em toda a língua. |
| Linguagem literal | Manter. Descrever o efeito técnico de expressões como “dar um jeito” ou “o sistema engasgou”. |
| Grupos nominais de até três palavras | Não impor a contagem inglesa. Explicitar relações entre os substantivos e preservar nomes técnicos compostos. |
| Avisos antes da ação | Manter a posição e a classificação adotada no domínio. Não inventar uma escala universal de rótulos de risco. |
| Forma afirmativa | Preferir quando equivalente. Preservar proibições, ausência de evidência e condições negativas relevantes. |
| Listas e tabelas | Escolher conforme a tarefa. Separar sequência, alternativas, critérios e resultados. |
| Nota agregada de qualidade | Substituir por revisão de sentido e clareza. Uma pontuação alta não compensa um erro técnico. |
| Elementos literais preservados | Manter comandos, código, nomes, caminhos, mensagens e citações. |

## Verbos, aspecto e modalidade

Use “Abra”, “Selecione”, “Aguarde” e “Confirme” em instruções dirigidas ao leitor.
Não alterne com infinitivos sem uma razão de formato. Preserve padrões existentes de listas de verificação e títulos.
O sujeito pode ficar implícito no imperativo quando o executor estiver claro.

| Intenção | Redação possível | Cuidado |
|---|---|---|
| Ação concluída | “A rotina terminou às 14h.” | Não mudar para presente se o horário for parte da evidência. |
| Ação em andamento | “O sistema está copiando os arquivos.” | “O sistema copia os arquivos” pode descrever comportamento habitual. |
| Repetição recente | “O serviço tem falhado após cada reinício.” | “Falhou” pode apagar a repetição. |
| Anterioridade | “O serviço já tinha parado quando o teste começou.” | Preserve a ordem dos eventos. |
| Condição futura | “Quando a cópia terminar, confira o arquivo.” | O subjuntivo é necessário e natural. |
| Obrigação | “O operador deve registrar o resultado.” | Use apenas se a obrigação existir. |
| Possibilidade | “A conexão pode falhar.” | Não transformar em previsão certa. |
| Permissão | “É permitido repetir o teste.” | Não confundir permissão com capacidade do sistema. |

Evite “vamos estar enviando” quando apenas adia ou alonga a ação.
Mantenha “estará funcionando durante o teste” quando a duração fizer parte da informação.
Mantenha a passiva quando o agente for desconhecido ou quando o estado for o foco: “O arquivo foi excluído às 14h.”
Não invente um agente para obter voz ativa.

## Relações e referências

Repita o nome do componente se “ele”, “isso”, “seu” ou “o mesmo” permitir mais de uma interpretação.
Escreva “Envie o relatório ao técnico” quando o destinatário for o técnico.
Use crase quando a construção exigir: “Envie o relatório à equipe”.
Não remova preposições para reduzir a contagem de palavras.

Preserve “sistema de gerenciamento de banco de dados” como nome técnico.
Divida relações mais extensas em frases quando a associação entre componentes ficar incerta.
Não substitua um termo composto por um nome inventado mais curto.

Explicite se as condições são cumulativas ou alternativas.
Preserve diferenças como “todos”, “algum”, “somente”, “pelo menos” e “no máximo”.
“Não houve falha” afirma mais que “Não foi encontrada evidência de falha”.

## Números e unidades

Em texto destinado a pessoas, use a convenção decimal brasileira: `2,5`.
Em código, CSV, comandos ou formatos de intercâmbio, preserve a sintaxe exigida pelo sistema.
Não converta automaticamente pontos e vírgulas.

Nas grandezas do SI, separe o número do símbolo: `5 mm`, `25 °C`.
Não acrescente plural nem ponto aos símbolos das unidades.
Preserve maiúsculas e minúsculas, como `mW` e `MW`.
As unidades de ângulo plano têm convenções próprias, como `90°`.
Consulte [F7](fontes.md#f7--inmetro) quando houver dúvida.

Explicite o fuso horário quando ele afetar a operação.
Preserve datas e horários literais em registros.
Não converta unidades nem acrescente tolerâncias sem base no pedido e nos dados.
