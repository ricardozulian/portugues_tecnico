# Exemplos de aplicação

Estes exemplos são próprios desta skill. Os textos de entrada são fictícios.
As revisões preservam os fatos declarados; não demonstram que uma operação real foi executada.

## Procedimento com condição e critério

Entrada:

> Depois que a cópia terminar, deverá ser efetuada a reinicialização do serviço e a verificação do código HTTP, que deve ser 200.

Revisão:

Após o término da cópia:

1. Reinicie o serviço.
2. Confira o código HTTP retornado.

Resultado esperado: `200`.

A condição rege a sequência inteira. O resultado esperado não é apresentado como resultado observado.

## Aviso antes da ação

Entrada:

> Exclua o volume temporário. Crie outro volume vazio. A exclusão remove todos os dados desse volume.

Revisão:

Aviso: a exclusão remove todos os dados do volume temporário.

1. Exclua o volume temporário.
2. Crie outro volume vazio.

O exemplo não autoriza a exclusão de um volume real nem declara a existência de uma cópia de segurança.

## Distinção técnica preservada

Entrada:

> Proceda à validação do método para o uso pretendido.

Revisão:

> Valide o método para o uso pretendido.

Não substituir por “Olhe o método” ou “Confira o método”. A tarefa de validação permanece explícita.

## Duração e repetição

Entrada:

> O serviço tem falhado após cada reinício desde segunda-feira.

Revisão:

> O serviço tem falhado após cada reinício desde segunda-feira.

A frase pode permanecer. “O serviço falhou” retiraria a informação de repetição.

## Inglês necessário e elementos literais

Entrada:

> No botão “Retry”, realize uma nova tentativa. A mensagem exibida é “Connection timed out”. O parâmetro é `request_timeout`.

Revisão:

> Selecione **Retry** para tentar novamente. O sistema mostra “Connection timed out”. O parâmetro é `request_timeout`.

O rótulo, a mensagem e a chave permanecem em inglês.
Uma explicação pode informar que o tempo limite da conexão foi excedido, sem alterar a mensagem citada.

Entrada para uma equipe que adota o objeto pull request:

> Encaminhe o pull request para revisão.

Revisão:

> Envie o pull request para revisão.

Para leitores novos, explique o objeto na primeira ocorrência.
Não crie um nome português que dificulte localizá-lo na plataforma.

## Incerteza preservada

Entrada:

> A falha pode estar relacionada à configuração. Não encontramos evidência de perda de dados.

Revisão:

> A configuração pode ter causado a falha. Não encontramos evidência de perda de dados.

Não escrever “A configuração causou a falha” nem “Não houve perda de dados”.

## Critério ausente

Entrada:

> Confira se a temperatura está boa antes de iniciar.

Resultado da revisão:

> Falta informar a faixa de temperatura permitida para iniciar.

Não inventar `25 °C` ou qualquer outro limite para completar o procedimento.

## Formato numérico e código

Entrada:

> A espera é de dois segundos e meio. Use `timeout=2.5`.

Revisão:

> A espera é de 2,5 s. Use `timeout=2.5`.

A convenção decimal do texto não altera a sintaxe do comando.

## Limite da revisão de estilo

Pedido:

> Simplifique a descrição do plano aprovado sem alterar a arquitetura.

Conduta:

Reescreva as frases e preserve a arquitetura.
Se houver uma contradição técnica, informe o problema em separado.
Não escolha outra arquitetura para tornar o texto mais fácil de explicar.
