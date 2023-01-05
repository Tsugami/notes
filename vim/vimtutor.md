# Vim

O Vim tem 4 modos: Normal, Inserção, Seleção e ?.

Movimentação:

Use botões de cursor ou `h` para esquerda, `j` para baixo, `k` para cima e `l` para o lado.

Fechar a janela (window):

Use `:q<Enter>`

Sair do vim:

Use `:qa!<Enter>` (cuidado, todas as mudanças serão perdidas.)

Pular para uma palavra (subject, acho que é links):

Use `CTRL-]` em cima da palavra.

`CTRL-O` para voltar aonde vc estava

## TEXT EDITING

Deletar:

Use `x` para deletar uma letra (character).

Inserir:

Use `i` para entrar no mode de inserção onde está o cursor e use `<ESC>` para sair.

Adicionar:

Use `a` para entrar no modo de inserção no final da linha e use `<ESC>` para sair.

## EDITING A FILE

Use `:wq` para sair e salvar o arquivo.

## DELETION COMANDOS

Use `dw` para deletar uma palavra. (dw = delete word)

> NOTE: A letra `d` aparecerá na última linha da tela enquanto você digita isto. O Vim está esperando que você digite w . Se você ver outro personagem do que você digitou algo errado; pressione `<ESC>` e recomece.

Use `d$` para deletar tudo do cursor até o final da linha.

## Operation and motion

Alguns comandos que mudam o texto usa feito para um operador e um _motion_.
O formato para deletar comandos com o `d` delete operator segue:

d motion

Onde:

`d` - o operador de deletar.
`motion` - o que o operator irá operar.

Usando "motion" com quantidade:

Use `d2e` para deletar duas palavras.

Use `2w` para mover para o começo da segunda palavra.

Use `3e` para mover para o fim da terceira palavra.

## Operações em linhas

Use `dd` para deletar toda linha.
Use `2dd` para deletar duas linhas.

## Desfazer operações

Use `u` para desfazer operações. (Undo).
Yse `U` para desfazer TODAS as operações.
Use `CTRL+R` para refazer as operações desfeitas.

## PUT

Use `p` para colar a ultima coisa deletada depois do cursor.

## REPLACE

Use `r` para na palavra que vc quer substituir, e depois para digite qual palavra que vc quer.

## CHANGE

Use `ce` para deletar o resto da palavra do cursor atual e digitar oq quer. (`c` change `e` edit)

Use `c$` para deletar o resto da linha e digitar oq quer.

## CURSOR LOCATION AND FILE STATUS

Use `CTRL-G` para ver o status do arquivo e sua localização.
use `CTRL-G+.` para sumir o status.
use `G` para ir pro final do arquivo.
Use `gg` para ir pro começo do arquivo,
use `__number__ G` para mover para o numero da linha.

## SEARCH

Use `/` seguido da palavra para pesquisar PARA FRENTE e `$` para pesquisar PARA ATRÁS:

- `n` para navegar para proxima mesma palavra.
- `N` para navegar na direção oposta.
- `CTRL-O` para voltar aonde vc estava.

## Match

Use `%` para mover entre o final e começo de ), ] e }

## SUBSTITUTE

Use `:s/__old__/__new__` e regex para substituir algo

Exemplo:

`the best animal is an animal.`

para mudar o `animal` dessa fazer de cima, vc pode usar: `:s/animal/vegetal`.

`the best vegetal is an animal`

para mudar todos de uma linha, vc pode usar: `:s/animal/vegetal/g`

`the best vegetal is an vegetal`

o `g` é de globalmente (globally).

Use `:#,#s/__old__/__new__/g` para mudar em um range de linhas.
Use `:%s/__old__/__new__/g` para mudar em todo o arquivo.
Use `:%s/__old__/__new__/gc` para mudar em todo o arquivo, mas com um "prompt", perguntando em cada palavra, se deve mudar ou não.

## HOW TO EXECUTE AN EXTERNAL COMMAND

Para executar um comando externo, fora do terminal.

Use `:!` seguindo do comando. Por exemplo:

`:!ls` usa ls no terminal

## Navigation Files

Use `vim <directory>` para abrir no modo de navegação de arquivos

> Proximos comandos são apenas ativos no modo de navegação de arquivos

Use `d` para criar uma pasta
Use `%` para criar um arquivo

stop 634
