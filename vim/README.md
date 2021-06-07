# Vim

[screenshot](screenshot.png)

Eu escolhi usar o editor vim, mas você pode usar outros editores além do vim como o __nano__ por exemplo.

O vim (VI Improvement) é uma melhoria do antigo editor de texto __vi__. Este por sua vez é uma melhoria do editor de texto orientado a linha chamado __ed__. Existe também uma versão do vim para ambiente X chamada __gvim__.

O vim possui três formas de trabalho: `modo de linha`, `modo de edição` e `modo de comandos`. A mudança de um modo para outro modo é feita através do uso da tecla `Esc`.

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

## Fontes e Recomendações

confira os link's abaixos para saber mais:

* [Vim para Noobs](https://leanpub.com/vimparanoobs/read)
* [Vimbook](https://vimbook.gitbook.io/vimbook/)
* [Vim - Mais que um editor](https://www.youtube.com/watch?v=UUzW46SeLhg&list=LLRzk-2RgRW7ksClaSKNBMMw&index=23&t=1856s)
* [Vim - Portal brasileiro do editor de textos Vim (VI)](https://aurelio.net/vim/vi-vim-venci.html)
* [VI, Vim e venci](https://aurelio.net/vim/vi-vim-venci.html)
* [Mapeamento de teclas do Vim](https://www.mundotibrasil.com.br/mapeamento-de-teclas-do-vim/)
* [.vimrc - Viva o Linux](https://www.vivaolinux.com.br/etc/vimrc-2/)
* [Como editar preferencias - WikiBooks](https://pt.wikibooks.org/wiki/Vim/Como_editar_prefer%C3%AAncias)
* [A goo vimrc - Doug Black](https://dougblack.io/words/a-good-vimrc.html)
* [Vim Config](https://vimconfig.com/)
* [Vim Bootstrap](https://vim-bootstrap.com/)
