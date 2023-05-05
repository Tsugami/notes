# Vimrc

```
set number
set relativenumber
set mouse=a
set tabstop=2
set wildmenu
set wildmode=list:longest
```

# Buffers

`:help windows`

`Ctrl-6` ..... Alterar entre buffers (:buffer#)
Ctrl-w-v ..... Divide a janela verticalmente (:vsplit)
Ctrl-w-n ..... Faz a janela atual ser a única (:only)
Ctrl-w-q ..... Fecha a janela atual (:quit)
Ctrl-w-c ..... Fecha a janela atual (:quit)

:wall ..... salva todas janelas (write all)
:qall ..... fecha todas janelas (quit all)

## Movimentação entre janelas

`:help jumps`

Usando o conjunto de `h`, `k`, `l`, `j`, mas com Ctrl-w na frente.

Ctrl-w-h ..... move para a janela da esquerda
Ctrl-w-j ..... move para a janela de baixo
Ctrl-w-k ..... move para a janela de cima
Ctrl-w-l ..... move para a janela da direita

## Movendo janelas

Da mesma forma que [movimenta entre janelas](#movimentacao-entre-janelas) mas com `h`, `k`, `l` e `j` em maisculo.

Ctrl-w-H ..... move janela para esquerda
Ctrl-w-J ..... move janela para baixo
Ctrl-w-K ..... move janela para cima
Ctrl-w-L ..... move janela para direita

## File explorer

:Vex ............ abre o file explorer verticalmente
:Sex ............ abre o file explorer em nova janela
:Tex ............ abre o file explorer em nova aba
:E .............. abre o file explorer na janela atual
após abrir chame a ajuda <F1>

# Digitar em multiplas linhas

1. Ctrl-v para entrar modo VISUAL BLOCK.
2. 3j para mover para 3 linhas para baixo.
3. Ctrl+I para entrar em modo de edição.
4. Esc para adicionar o texto nas proximas linhas.

[Link de exemplo](https://stackoverflow.com/a/9549765)

# Convertendo para Maiúsculas

gUU ....... converte a linha para maiúsculo
guu ....... converte a linha para minúsculo
gUiw ...... converte a palavra atual para maiúsculo
~ ......... altera o case do caractere atual

# File Navigator

% ...... Cria um arquivo novo
d ...... Cria uma pasta nova
