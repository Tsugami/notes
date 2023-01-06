# Vim

O Vim tem 4 modos: Normal, Inserção, Seleção e ?.

## NAVIGATION

Use botões de cursor ou `h` para esquerda, `j` para baixo, `k` para cima e `l` para o lado.

Pular para uma palavra (subject, acho que é links):

Use `CTRL-]` em cima da palavra.

`CTRL-O` para voltar aonde vc estava

## EXIT

Fechar a janela (window):

Use `:q<Enter>` para fechar a janela ou sair do arquivo.

Use `:qa!<Enter>` para sair do vim sem salvar as mudanças.

Use `CTRL-C` para sai do command-line sem executar nada.

## TEXT EDITING

### DELETE

Use `x` para deletar uma letra (character).

## INSERT

Use `i` para entrar no mode de inserção **onde está o cursor**.

Use `a` para entrar no modo de inserção **depois do cursor**.

Use `o` para entrar no modo de inserção em uma **linha nova abaixo**.

Use `O` para entrar no modo de inserção em uma **linha nova acima**.

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

Use `R` para substituir **mais de uma** palavra.

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

Para ignorar case (lowercase, capital-case, uppercase), use `:set ic` (ic = ignore case).
Para desabilitar o ignore-case, use `:set noic`.

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

## SELECTING TEXT TO WRITE

1. Digite `v` para entrar no modo visual
2. Digite `:`, vai aparecer `:'<.'>`
3. Digite `w TEST` quando não existe um arquivo TEST. Vai ficar assim: `<,'>w TEST`, pressione `<ENTER>`
4. Vim irá criar um arquivo TEST com o conteúdo selecionado, use `:!ls` para ver.

## COPY

Entre no modo visual com `v`, selecione o texto e use `y` (yanks = copies) para copiar.

## RETRIEVING AND MERGING FILES

Para copiar o conteúdo de outro arquivo, use `:r <arquivo>`

Você pode ler o output de um **external command**. Por exemplo, `:r !;s` ler o output do comando ls e cola no vim.

## NAVIGATION FILES

Use `vim <directory>` para abrir no modo de navegação de arquivos

> Proximos comandos são apenas ativos no modo de navegação de arquivos

Use `d` para criar uma pasta
Use `%` para criar um arquivo

## HELP

Use `:help` ou `<F1>` para entrar no help.

Use `:help <command>` para pesquisar sobre um comando ou outra coisa, exemplos:

- `:help c_CTRL-ID`
- `:help w`
- `:help insert-index`
- `:help user-manual`
- `:help vimrc-intro`

## WINDOW

Para pular para outra janela aberta, use `CTRL-W+CTRL-W`

## CREATE A STARTUP SCRIPT

crie um **vimrc** no home

- `:e ~/.vimrc` para Unix.
- `:e $VIM/_vimrc` para Windows.

O vim vem com um exemplo em `$VIMRUNTIME/vimrc_example.vim`, você pode copia ele com `:r`. Para mais informações, use `:help vimrc-intro`

## AUTOCOMPLETE

Use `CTRL-D` ou `<TAB>` para autocomplete.

Pode testar com `:e` + (`CTRL-D` | `<TAB>`)

## FIM

Fim do vimtutor, agora continua no `:help user-manual`.
