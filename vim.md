# Vim

Eu escolhi usar o editor vim, mas você pode usar outros editores além do vim como o __nano__ por exemplo.

O vim (VI Improvement) é uma melhoria do antigo editor de texto __vi__. Este por sua vez é uma melhoria do editor de texto orientado a linha chamado __ed__. Existe também uma versão do vim para ambiente X chamada __gvim__.

O vim possui três formas de trabalho: `modo de linha`, `modo de edição` e `modo de comandos`. A mudança de um modo para outro modo é feita através do uso da tecla Esc.

Após o arquivo ser aberto pelo vim, o modo de comando é ativado. No modo de comando, as teclas digitadas pelo usuário são interpretadas pelo vim como ações a serem executadas dentro do arquivo aberto. No modo de edição, as teclas digitadas pelo usuário são ecoadas na tela. Para entrar neste modo, pode-se digitar, por exemplo, "a" (adicionar), "i" (incluir), etc. No modo de linha, o usuário define ações a serem executadas no arquivo como um todo (por exemplo, salvar, substituir caracteres, sair do aplicativo, etc). Para entrar neste modo, deve-se digitar `Esc`.

* `vim [opções] [arquivo]`

São alguns dos comandos do vim no __modo de comandos__:

* `0`: Mover o cursor para o início da linha em que o cursor está posicionado.
* `a`: Inserir texto após a posição atual do cursor.
* `A`: Inserir texto no final da linha atual.
* `-b`: Permite editar arquivo binário.
* `dd`: Deletar linha atual.
* `[n]+dd`: Deletar n linhas a partir da linha atual.
* `G`: Ir para o fim do arquivo.
* `[n]+G`: Ir para a n-ésima linha do arquivo.
* `h`: Voltar um caractere.
* `H`: Ir para a primeira linha exibida na tela atual.
* `i`: Inserir texto a partir da posição atual do cursor.
* `I`: Inserir texto no início da linha atual.
* `j`: Descer uma linha.
* `J`: Juntar a linha atual com a linha seguinte.
* `[n]+J`: Juntar n linhas consecutivas a partir da linha atual.
* `k`: Subir uma linha.
* `l`: Avançar um caractere.
* `L`: Ir para a última linha exibida na tela atual.
* `n`: Procurar, a partir da posição atual do cursor, a próxima ocorrência do texto definido no último comando /.
* `N`: Procurar, a partir da posição atual do cursor e indo em direção ao início do arquivo, a próxima ocorrência do texto definido no último comando /.
* `o`: Inserir uma linha em branco após a linha atual.
* `O`: Inserir uma linha em branco acima da linha atual.
* `p`: Inserir linhas copiadas após a linha atual.
* `P`: Inserir linhas copiadas antes da linha atual.
* `r`: Substituir o caractere atual.
* `R`: Substituir um conjunto de caracteres.
* `s`: Deletar o caractere atual e inserir texto.
* `S`: Apagar linha e inserir novo texto na linha.
* `u`: Desfazer a última alteração feita no texto e ainda não desfeita.
* `U`: Desfazer a última alteração feita no texto.
* `x`: Apagar caractere onde o cursor está posicionado.
* `$`: Mover o cursor para o fim da linha em que o cursor está posicionado.
* `[n]+y`: Copiar n linhas a partir da linha atual.
* `yy`: Copiar a linha atual.
* `[n]+Y`: Copiar n linhas a partir da linha atual.
* `YY`: Copiar a linha atual.
* `CTRL+B`: Voltar uma página.
* `CTRL+F`: Avançar uma página.
* `F1`: Exibir tela de ajuda.
* `[n]+ENTER`: Ir para n linhas abaixo da linha atual.
* `[n]+.`: Repetir o último comando que alterou o texto n vezes a partir da posição atual do cursor.
* `[n]+~+ENTER`: Inverter a caixa (case) dos n caracteres seguintes ao cursor.
* `/texto`: Procurar pela primeira ocorrência do texto especificado a partir da posição atual do cursor.

São alguns dos comandos do vim no __modo de linha__:

* `:r arquivo`: Incluir arquivo a partir da linha atual do cursor.
* `:q+ENTER`: Sair da tela de ajuda.
* `:q!`: Sair do vim sem salvar as alterações.
* `:w arquivo`: Salvar arquivo com o nome especificado.
* `:wq!`: Sair do vim salvando as alterações.
* `:X`: Criptografa o arquivo.
* `:n`: Ir para a linha "n". Exemplo: Para ir para linha 10 do arquivo, :10

Busca:

* `/palavra`: Procura por "palavra" do início para o fim.
* `?palavra`: Procura por "palavra" do fim para o início.
* `/Mari[oa]`: Procura por "Mario" ou "Maria".
* `/\< pal`: Procura por expressões que começem com "pala" como, "palavra" ou "palíndromo".
* `/ismo\>`: Procura por expressões que terminem com "ismo" como, "autismo".
* `/\< para\>`: Procura pela palavra "para".
* `/\<...\>`: Procura por todas as palavras com 3 letras.
* `/maria\|joao`: Procura por maria ou joao.
* `/\<\d\d\d\d\>`: Procura exatamente por 4 dígitos numéricos.
* `/^\n\{3}`: Procura por três linhas em branco.
* `:bufdo /palavra/`: Procura "palavra" em todos os arquivos abertos.

Substituição:

* `:%s/antigo/novo/g`: Substitui todas as ocorrências de "antigo" por "novo" no arquivo.
* `:%s/antigo/novo/gw`: Substitui todas as ocorrências com confirmação.
* `:2,35s/antigo/novo/g`: Substitui todas as ocorrências entre as linhas 2 e 35.
* `:5,$s/antigo/novo/g`: Substitui todas as ocorrências da linha 5 até EOF (fim da linha).
* `:%s/^/legal/g`: Substitui o começo de cada linha com "legal".
* `:%s/$/Oh/g`: Substitui o fim de cada linha por "Oh".
* `:%s/antigo/novo/gi`: Substitui "antigo" por "novo" desconsiderando maíusculas e/ou minúsculas.
* `:%s/ *$//g`: Apaga todos os espaços em branco.
* `:g/palavra/d`: Apaga todas as linhas contendo "palavra".
* `:v/palavra/d`: Apaga todas as linhas que não contém "palavra".
* `:s/maria/joao/`: Substitui a primeira ocorrência de "maria" por "joao" na linha corrente.
* `:s/maria/joao/g`: Substitui todas as ocorrências de "maria" por "joao" na linha corrente.
* `:%s/maria/joao/g`: Substitui "maria" por "joao" em todo o arquivo.
* `:%s/\r//g`: Apaga retornos de carro do windows (\n).
* `:%s/\r/\r/g`: Transforma os retornos de carro do windows (\n) em retornos do Linux (\r).
* `:%s#<[^>]\+>##g`: Apaga tags HTML mas mantêm o texto.
* `:%s/^\(.*\)\n\1$/\1/`: Apaga linhas repetidas.
* `Ctrl+a`: Incrementa o número sob o cursor.
* `Ctrl+x`: Decrementa o número sob o cursor.
* `ggVGg?`: Muda o texto usando Rot13.

Minúsculo / Maiúsculo:

* `Vu`: Torna todos os caracteres da linha minúsculos.
* `VU`: Torna todos os caracteres da linha maiúsculos.
* `g~~`: Inverte os caracteres do texto inteiro.
* `vEU`: Coloca as letras da palavra em maiúsculas.
* `vE~~`: Inverte os caracteres da palavra selecionada.
* `ggguG`: Coloca todo o texto em minúsculas.
* `:set ignorecase`: Ignora minúsculos/maiúsculos nas buscas.
* `:set smartcase`: Ignora minúsculos/maiúsculos em buscas exceto quando uma letra msiúscula é usada.
* `:%s/\<./\u&/g`: Coloca a primeira letra de cada palavra em maiúscula.
* `:%s/\<./\l&/g`: Coloca a primeira letra de cada palavra em minúscula.
* `:%s/.*/\u&`: Coloca a primeira letra de cada linha em maiúscula.
* `:%s/.*/\l&`: Coloca a primeira letra de cada linha em minúscula.

Lendo/Gravando arquivos:

* `:1,10 w arquivo`: Salva as linhas de 1 a 10 em "arquivo".
* `:1,10 w >> arquivo`: Adiciona as linhas de 1 a 10 em "Arquivo".
* `:r arquivo`: Insere o conteúdo de "arquivo" no atual.
* `:23r arquivo`: Insere o conteúdo de "arquivo" a partir da linha 23.

Explorando arquivos:

* `:e .`: Abre o gerenciador de arquivos integrado do Vim.
* `:Sex`: Divide a janela e abre o gerenciador de arquivos integrado.
* `:browse e`: Abre o gerenciador de arquivos integrado na janela corrente.
* `:ls`: Lista os buffers carregados.
* `:cd ..`: Move para a pasta superior.
* `:args`: Lista os arquivos.
* `:args *.php`: Abre lista de arquivos.
* `:grep expressao *.php`: retorna uma lista de arquivos .php que contenham a expressão informada.
* `gf`: Abre o arquivo sob o cursor.

Interação com o Linux:

* `:!pwd`: Executa o comando "pwd" e retorna para o Vim.
* `!!pwd`: Executa o comando "pwd" e insere a saída no buffer.
* `:sh`: Retorna temporariamente para o shell.
* `exit`: Retorna para o Vim.

Alinhamento:

* `:%!fmt`: Alinha todas as linhas.
* `!}fmt`: Alinha todas as linhas a partir da posição corrente.
* `5!!fmt`: Alinha as próximas 5 linhas.

Abas:

* `:tabnew`: Cria uma nova aba.
* `gt`: Mostra a próxima aba.
* `:tabfirst`: Mostra a primeira aba.
* `:tablast`: Mostra a última aba.
* `:tabm n(posicao)`: Reorganiza as abas.
* `:tabdo %s/foo/bar/g`: Executa um comando em todas as abas.
* `:tab ball`: Coloca todos os arquivos abertos em abas.

Divisão da janela do Vim:

* `:e arquivo`: Edita "arquivo" na janela corrente.
* `:split arquivo`: Divide a janela e abre "arquivo".
* `ctrl-w "seta para cima"`: Coloca o cursor na janela do topo.
* `ctrl-w ctrl-w`: Coloca o cursor na próxima janela.
* `ctrl-w_`: Maximiza a janela corrente.
* `ctrl-w=`: Coloca todas as janelas com o mesmo tamanho.
* `10 ctrl-w+`: Adiciona 10 linhas de tamanho na janela corrente.
* `:vsplit arquivo`: Divide a janela verticalmente.
* `:sview arquivo`: O mesmo que split, mas em modo somente-leitura.
* `:hide`: Fecha a janela corrente.
* `:only`: Fecha todas as janelas, exceto a janela atual.
* `:b 2`: Abre #2 na janela corrente.

Auto-completion do texto:

* `Ctrl+n Ctrl+p (em modo de inserção)`: Completa palavra.
* `Ctrl+x Ctrl+l`: Completa linha.
* `:set dictionary=dict`: Define dict como o dicionário atual.
* `Ctrl+x Ctrl+k`: Completa usando o dicionário.

Marcações:

* `mk`: Marca a posição corrente como k.
* `‘k`: Move o cursor para a marca k.
* `d’k`: Apaga tudo até a marca k.

Abreviações:

* `:ab email me@me.com`: Define email como abreviação de me@me.com.

Identação de Texto:

* `:set autoindent`: Liga a identação automática.
* `:set smartindent`: Liga a identação inteligente.
* `:set shiftwidth=4`: Define o tamanho da identação em 4 espaços.
* `ctrl-t, ctrl-d`: Identa/Deidenta no modo de inserção.
* `>>`: Identa.
* `<<`: Deidenta.

Marcação de sintaxe:

* `:syntax on`: Liga a marcação de sintaxe.
* `:syntax off`: Desliga a marcação de sintaxe.
* `:set syntax=perl`: Força a usar a marcação de sintaxe do perl.

Este é meu setup atual no vim, fique a vontade para usar e melhorar:

```.vimrc
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
"
" Sections:
"    -> General
"    -> VIM user interface
"    -> Colors and Fonts
"    -> Files and backups
"    -> Text, tab and indent related
"    -> Visual mode related
"    -> Moving around, tabs and buffers
"    -> Status line
"    -> Editing mappings
"    -> vimgrep searching and cope displaying
"    -> Spell checking
"    -> Misc
"    -> Helper functions
"
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => General
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Set line numbers
set nu!

" Sets how many lines of history VIM has to remember
set history=500

" Enable filetype plugins
filetype plugin on
filetype indent on

" Set to auto read when a file is changed from the outside
set autoread
au FocusGained,BufEnter * checktime

" With a map leader it's possible to do extra key combinations
" like <leader>w saves the current file
let mapleader = ","

" Fast saving
nmap <leader>w :w!<cr>

" :W sudo saves the file
" (useful for handling the permission-denied error)
command! W execute 'w !sudo tee % > /dev/null' <bar> edit!


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => VIM user interface
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Set 7 lines to the cursor - when moving vertically using j/k
set so=7

" Avoid garbled characters in Chinese language windows OS
let $LANG='en'
set langmenu=en
source $VIMRUNTIME/delmenu.vim
source $VIMRUNTIME/menu.vim

" Turn on the Wild menu
set wildmenu

" Ignore compiled files
set wildignore=*.o,*~,*.pyc
if has("win16") || has("win32")
    set wildignore+=.git\*,.hg\*,.svn\*
else
    set wildignore+=*/.git/*,*/.hg/*,*/.svn/*,*/.DS_Store
endif

" Always show current position
set ruler

" Height of the command bar
set cmdheight=1

" A buffer becomes hidden when it is abandoned
set hid

" Configure backspace so it acts as it should act
set backspace=eol,start,indent
set whichwrap+=<,>,h,l

" Ignore case when searching
set ignorecase

" When searching try to be smart about cases
set smartcase

" Highlight search results
set hlsearch

" Makes search act like search in modern browsers
set incsearch

" Don't redraw while executing macros (good performance config)
set lazyredraw

" For regular expressions turn magic on
set magic

" Show matching brackets when text indicator is over them
set showmatch

" How many tenths of a second to blink when matching brackets
set mat=2

" No annoying sound on errors
set noerrorbells
set novisualbell
set t_vb=
set tm=500

" Properly disable sound on errors on MacVim
if has("gui_macvim")
    autocmd GUIEnter * set vb t_vb=
endif

" Add a bit extra margin to the left
set foldcolumn=1


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Colors and Fonts
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Enable syntax highlighting
syntax enable

" Enable 256 colors palette in Gnome Terminal
if $COLORTERM == 'gnome-terminal'
    set t_Co=256
endif

"try
"    colorscheme yourthemehere
"catch
"endtry

set background=dark

" Set extra options when running in GUI mode
if has("gui_running")
    set guioptions-=T
    set guioptions-=e
    set t_Co=256
    set guitablabel=%M\ %t
endif

" Set utf8 as standard encoding and en_US as the standard language
set encoding=utf8

" Use Unix as the standard file type
set ffs=unix,dos,mac


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Files, backups and undo
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Turn backup off, since most stuff is in SVN, git etc. anyway...
set nobackup
set nowb
set noswapfile


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Text, tab and indent related
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Use spaces instead of tabs
set expandtab

" Be smart when using tabs ;)
set smarttab

" 1 tab == 2 spaces
set shiftwidth=2
set tabstop=2

" Linebreak on 500 characters
set lbr
set tw=500

set ai "Auto indent
set si "Smart indent
set wrap "Wrap lines


""""""""""""""""""""""""""""""
" => Visual mode related
""""""""""""""""""""""""""""""
" Visual mode pressing * or # searches for the current selection
" Super useful! From an idea by Michael Naumann
vnoremap <silent> * :<C-u>call VisualSelection('', '')<CR>/<C-R>=@/<CR><CR>
vnoremap <silent> # :<C-u>call VisualSelection('', '')<CR>?<C-R>=@/<CR><CR>


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Moving around, tabs, windows and buffers
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Map <Space> to / (search) and Ctrl-<Space> to ? (backwards search)
map <space> /
map <C-space> ?

" Disable highlight when <leader><cr> is pressed
map <silent> <leader><cr> :noh<cr>

" Smart way to move between windows
map <C-j> <C-W>j
map <C-k> <C-W>k
map <C-h> <C-W>h
map <C-l> <C-W>l

" Close the current buffer
map <leader>bd :Bclose<cr>:tabclose<cr>gT

" Close all the buffers
map <leader>ba :bufdo bd<cr>

map <leader>l :bnext<cr>
map <leader>h :bprevious<cr>

" Useful mappings for managing tabs
map <leader>tn :tabnew<cr>
map <leader>to :tabonly<cr>
map <leader>tc :tabclose<cr>
map <leader>tm :tabmove
map <leader>t<leader> :tabnext

" Let 'tl' toggle between this and the last accessed tab
let g:lasttab = 1
nmap <Leader>tl :exe "tabn ".g:lasttab<CR>
au TabLeave * let g:lasttab = tabpagenr()


" Opens a new tab with the current buffer's path
" Super useful when editing files in the same directory
map <leader>te :tabedit <C-r>=expand("%:p:h")<cr>/

" Switch CWD to the directory of the open buffer
map <leader>cd :cd %:p:h<cr>:pwd<cr>

" Specify the behavior when switching between buffers
try
  set switchbuf=useopen,usetab,newtab
  set stal=2
catch
endtry

" Return to last edit position when opening files (You want this!)
au BufReadPost * if line("'\"") > 1 && line("'\"") <= line("$") | exe "normal! g'\"" | endif


""""""""""""""""""""""""""""""
" => Status line
""""""""""""""""""""""""""""""
" Always show the status line
set laststatus=2

" Format the status line
set statusline=\ %{HasPaste()}%F%m%r%h\ %w\ \ CWD:\ %r%{getcwd()}%h\ \ \ Line:\ %l\ \ Column:\ %c


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Editing mappings
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Remap VIM 0 to first non-blank character
map 0 ^

" Move a line of text using ALT+[jk] or Command+[jk] on mac
nmap <M-j> mz:m+<cr>`z
nmap <M-k> mz:m-2<cr>`z
vmap <M-j> :m'>+<cr>`<my`>mzgv`yo`z
vmap <M-k> :m'<-2<cr>`>my`<mzgv`yo`z

if has("mac") || has("macunix")
  nmap <D-j> <M-j>
  nmap <D-k> <M-k>
  vmap <D-j> <M-j>
  vmap <D-k> <M-k>
endif

" Delete trailing white space on save, useful for some filetypes ;)
fun! CleanExtraSpaces()
    let save_cursor = getpos(".")
    let old_query = getreg('/')
    silent! %s/\s\+$//e
    call setpos('.', save_cursor)
    call setreg('/', old_query)
endfun

if has("autocmd")
    autocmd BufWritePre *.txt,*.js,*.py,*.wiki,*.sh,*.coffee :call CleanExtraSpaces()
endif


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Spell checking
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Pressing ,ss will toggle and untoggle spell checking
map <leader>ss :setlocal spell!<cr>

" Shortcuts using <leader>
map <leader>sn ]s
map <leader>sp [s
map <leader>sa zg
map <leader>s? z=


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Misc
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Remove the Windows ^M - when the encodings gets messed up
noremap <Leader>m mmHmt:%s/<C-V><cr>//ge<cr>'tzt'm

" Quickly open a buffer for scribble
map <leader>q :e ~/buffer<cr>

" Quickly open a markdown buffer for scribble
map <leader>x :e ~/buffer.md<cr>

" Toggle paste mode on and off
map <leader>pp :setlocal paste!<cr>


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Helper functions
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Returns true if paste mode is enabled
function! HasPaste()
    if &paste
        return 'PASTE MODE  '
    endif
    return ''
endfunction

" Don't close window, when deleting a buffer
command! Bclose call <SID>BufcloseCloseIt()
function! <SID>BufcloseCloseIt()
    let l:currentBufNum = bufnr("%")
    let l:alternateBufNum = bufnr("#")

    if buflisted(l:alternateBufNum)
        buffer #
    else
        bnext
    endif

    if bufnr("%") == l:currentBufNum
        new
    endif

    if buflisted(l:currentBufNum)
        execute("bdelete! ".l:currentBufNum)
    endif
endfunction

function! CmdLine(str)
    call feedkeys(":" . a:str)
endfunction

function! VisualSelection(direction, extra_filter) range
    let l:saved_reg = @"
    execute "normal! vgvy"

    let l:pattern = escape(@", "\\/.*'$^~[]")
    let l:pattern = substitute(l:pattern, "\n$", "", "")

    if a:direction == 'gv'
        call CmdLine("Ack '" . l:pattern . "' " )
    elseif a:direction == 'replace'
        call CmdLine("%s" . '/'. l:pattern . '/')
    endif

    let @/ = l:pattern
    let @" = l:saved_reg
endfunction
```
 