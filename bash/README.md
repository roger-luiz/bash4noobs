<h1 align="center">
  Bash (Ubuntu)
</h1>

<p align="center">
  <img src="../.github/linux_terminal.png"/>
</p>

# Roadmap

* [Explicando alguns conceitos](#explicando-alguns-conceitos)
  * [Terminal](#terminal)
  * [Console](#console)
  * [Emulador de terminal](#emulador-de-terminal)
  * [Shell](#shell)
  * [Linha de comandos - CLI](#linha-de-comandos---cli)
  * [Shell vs Linha de comandos](#shell-vs-linha-de-comandos)

* [Básico antes dos comandos](#básico-antes-dos-comandos)
  * [Atalhos globais do Bash](#atalhos-globais-do-bash)
  * [Diretórios](#diretórios)
  * [Ajuda no terminal](#ajuda-no-terminal)
  * [Histórico de comandos](#histórico-de-comandos)

* [Manipulando arquivos](#manipulando-arquivos)
  * [Listagem de arquivos](#listagem-de-arquivos)
  * [Entrando e saíndo de diretórios](#entrando-e-saíndo-de-diretórios)
  * [Exibindo o diretório atual](#exibindo-o-diretório-atual)
  * [Exibindo o tamanho de um diretório](#exibindo-o-tamanho-de-um-diretório)
  * [Criando diretórios](#criando-diretórios)
  * [Criando arquivos](#criando-arquivos)
  * [Excluíndo diretórios e arquivos](#excluíndo-diretórios-e-arquivos)
  * [Copiando diretórios e arquivos](#copiando-diretórios-e-arquivos)
  * [Movendo e renomeando arquivos e pastas](#movendo-e-renomeando-arquivos-e-pastas)
  * [Visualização de arquivos](#visualização-de-arquivos)
  * [Compressão de arquivos](#compressão-de-arquivos)

* [Buscas](#buscas)
  * [Buscando por arquivos](#buscando-por-arquivos)
  * [Referência global](#referência-global)

* [Sistema](#sistema)
  * [Processos](#processos)
  * [Informações do sistema](#informações-do-sistema)
  * [Memória](#memória)
  * [Programas e atualizações](#programas-e-atualizações)
  * [Usuários](#usuários)
  * [Calculadora](#calculadora)

* [Referências](#referências)

# Explicando alguns conceitos

## Terminal

O terminal é um ambiente para entrada e saída de comandos, a palavra terminal também pode significar um dispositivo no qual podemos interagir com o computador, como por exemplo um teclado e monitor. No caso do terminal que estamos habituados ele é um software que emula os terminais tradicionais.

## Console

O console é um tipo especial de terminal. Geralmente é um painel de controle conectado a um computador. Originalmente um console é um dispositivo eletrônico no qual nos permite controlar um computador, por meio de entrada de texto e saída de vídeo.

No linux, nós também temos o console porém geralmente acessamos o console quando temos uma distribuição no modo texto, ou seja, sem interface gráfica.

## Emulador de terminal

Os terminais em software, também podem ser chamados de pseudo-terminais ou terminais virtuais, são softwares fornecidos por programas, específicos, que são do tipo emulador de terminais, alguns exemplos deles são:

* Xterm
* Konsole
* Gnome Terminal
* Terminator
* Termux
* Sakura

## Shell

O shell é um interpretador de linha de comandos. É a interface primária que nós vemos, caso o sistema não possuir interface gráfica, ao fazermos login, e sua função básica é iniciar outros programas e executar comandos. Quando estamos falando de linux, o shell se refere a shell de linha de comandos, alguns exemplos de shells comuns no linux:

* Bash
* csh
* zsh
* fish

## Linha de comandos - CLI

Uma linha de comandos, ou CLI que é um acrônimo para _command line interface_, é uma interface na qual nós podemos digitar comandos e pressionarmos alguma tecla para que o comando seja, de fato, executado. Ou seja, na linha de comando nós não temos botões, menus, mouse, atalhos entre outros itens que possam ser clicados com o mouse.

Exemplo de uma linha de comando:

```console
roger@abantes-PC:~$
```

Quando pressionamos a tecla que faça o nosso comando ser executado, geralmente a tecla `enter`, o shell captura esse comando, interpreta e executa adequadamente.

Agora que vimos o que é uma linha de comando e o que é um shell, vamos entender quais são suas diferenças, já que os dois são bem semelhantes.

## Shell vs Linha de comandos

A linha de comando não passa de uma interface, na qual, nós escrevemos os comandos. Já o shell é um programa especial que consegue interpretar esse comandos que estamos digitando.

__Observação__: No __Linux__ tudo é representado em forma de __arquivos__, um usuário do terminal é represtentado como um arquivo, assim como os própios comandos, os hardwares conectados na máquina, diretórios e etc.

# Básico antes dos comandos

## Atalhos globais do Bash

* `Ctrl + Shift + C`: Copiar.
* `Ctrl + Shift + V`: Colar.
* `Ctrl + C`: Cancela o comando atual em funcionamento.
* `Ctrl + Z`: Pausa o comando atual, retorna com "fg" em primeiro plano Linux ou "bg" em segundo plano.
* `Ctrl + D`: Faz o logout da sessão atual (similar ao comando "exit").
* `Ctrl + W`: Apaga uma palavra na linha atual.
* `Ctrl + U`: Apaga a linha inteira.
* `Ctrl + R`: Tecle para Exiber um comando recente.
* `Ctrl + L`: Limpa a tela.

## Diretórios

* `/`: É o diretório raiz, todos os demais diretórios estão abaixo dele.
* `/bin/`: Binários principais dos usuários.
* `/boot/`: Arquivos do sistema de Boot.
* `/dev/`: Arquivos de dispositivos.
* `/etc/`: Arquivos de configuração do sistema.
* `/home/`: Diretório dos usuários comuns do sistema.
* `/lib/`: Bibliotecas essenciais do sistema e os módulos do kernel.
* `/media/`: Diretório de montagem e dispositivos.
* `/mnt/`: Diretório de montagem de dispositivos - mesmo que "media".
* `/opt/`: Instalação de programas não oficiais da distribuição ou por conta do usuário.
* `/sbin/`: Armazena arquivos executáveis que representam comandos administrativos. Exemplo: shutdown
* `/srv/`: Diretório para dados de serviços fornecidos pelo sistema.
* `/tmp/`: Diretório para arquivos temporários.
* `/usr/`: Segunda hierarquia do sistema, onde ficam os usuários comuns do sistema e programas.
* `/var/`: Diretório com arquivos variáveis gerados pelos programas do sistema. Exemplo: logs, spool de impressoras, e-mail e cache.
* `/root/`: Diretório do usuário root - O usuário root tem o total poder sobre o sistema. Podendo instalar, desinstalar e configurar.
* `/proc/`: Diretório virtual controlado pelo Kernel com configuração total do sistema.

## Ajuda no terminal

Você pode consultar a documentação e o manual de uso dos comandos das seguintes maneiras:

* `[comando] --help`: Documentação do comando.
* `man [comando]`: Manual do comando.
* `info [comando]`: Semelhante ao man, mas geralmente fornece informações mais detalhadas.

## Histórico de comandos

* `history`: Lista o histórico de 2000 comandos digitados.
* `!!`: Repete o último comando.
* `Seta para cima e seta para baixo`: Últimos comandos digitados.

# Manipulando arquivos

## Listagem de arquivos

Podemos listar o conteúdo de um diretório utilizando o comando ls.

* `ls`: Lista arquivos e diretórios.
  * `ls -r`: Lista arquivos e diretórios em ordem reversa.
  * `ls -a`: Lista todos os arquivos e diretórios, incluindo arquivos ocultos.
  * `ls -l`: Formato longo, mostra permissões, número de links, propietário, grupo, tamanho, data de modificação e nome do arquivo.
  * `ls -h`: Lista arquivos e diretórios com informações formatadas ( Tem que ser usado com o -l ).
  * `ls -ls`: Lista arquivos e diretórios pelo tamanho, no caso começará pelo o arquivo de maior tamanho.
  * `ls -R`: Lista os arquivos e pastas recursivamente da pasta selecionada.
  * `ls -m`: Arquivos listados em sequência, separados por vírgula.
  * `ls -n`: Semelhante ao -l, porém mostra UID E GID Em vez de nomes de proprietário e grupo.
  * `ls -o`: Semelhante ao -l, porém não mostra o grupo do arquivo.
  * `ls -p`: Mostra uma barra ( / ) na frente de nomes de diretórios.
  * `ls -A`: Semelhante ao -a, mas não mostra o diretório corrente ( . ) ou o diretório acima ( .. ).
  * `ls -i`: Mostra o número do inode de cada arquivo na primeira coluna.

[Ver exemplo](examples/listagem-de-arquivos.md)

## Entrando e saíndo de diretórios

Podemos entrar e sair de um diretório utilizando o comando cd.

* `cd .`: Diretório atual.
* `cd ..`: Volta um diretório.
* `cd /`: Vai direto para o diretório raiz.
* `cd ~`: Vai direto para o diretório home.
* `cd -`: Nos retorna para o último diretório acessado.
* `cd /[destino]`: Partindo da raiz até o último diretório passado como referência.
* `cd [destino]`: Parte do local corrente até o diretório passado como referência.

[Ver exemplo](examples/entrando-e-saindo-de-diretorios.md)

## Exibindo o diretório atual

* `pwd`: Exibe o caminho de diretório atual.

[Ver exemplo](examples/exibindo-o-diretorio-atual.md)

## Exibindo o tamanho de um diretório

* `du [diretório]`: Exibe o tamanho de um diretório e todos os seus subdiretórios.

[Ver exemplo](examples/exibindo-o-tamanho-de-um-diretorio.md)

## Criando diretórios

Podemos criar diretórios utilizando o comando mkdir.

* `mkdir [nome-do-diretorio]`: Cria uma pasta.
* `mkdir pasta1 pasta2 pasta3`: Cria três pastas, pasta1, pasta2 e pasta3.
* `mkdir -p A/B/C`: Cria a pasta A, dentro da pasta A cria a pasta B e dentro da pasta B cria a pasta C.

[Ver exemplo](examples/criando-diretorios.md)

## Criando arquivos

Podemos criar arquivos utilizando o comando touch.

* `touch [arquivo]`: Cria uma arquivo.
  * `touch -a [arquivo]`: Altera a hora de acesso do arquivo.
  * `touch -m [arquivo]`: Altera a hora de modificação do arquivo.
  * `touch -am [arquivo]`: Altera a hora de acesso e modificação do arquivo.
  * `touch -c [arquivo]`: Altera a hora de acesso sem criar um novo arquivo.

__Observação__: podemos gerar nomes automáticos usando as chaves `{}`, desta maneira: `touch exemplo{1..3}.txt`, este comando irá criar 3 arquivos chamados exemplo1.txt, exemplo2.txt e exemplo3.txt.

[Ver exemplo](examples/criando-arquivos.md)

## Excluíndo diretórios e arquivos

Podemos excluir arquivos utilizando o comando rm.

* `rm [arquivo]`: Exclui um arquivo.
  * `rm -f [arquivo]`: Exclui arquivos forçadamente.
  * `rm -r [arquivo]`: Exclui o diretório e os arquivos na direção recursiva, o diretório especificado junto com seu subdiretório e arquivos.
  * `rm -d [arquivo]`: Remove somente diretórios vazios.
  * `rm -i [arquivo]`: Pergunta se queremos remover o arquivo/diretório antes de excluir.

[Ver exemplo](examples/excluindo-diretorios-e-arquivos.md)

## Copiando diretórios e arquivos

Podemos copiar arquivos utilizando o comando cp.

* `cp [arquivo] [destino]`: Copia um arquivo para um determinado destino.
  * `cp -i [arquivo] [destino]`: Pergunta se desejamos sobrescrever um arquivo destino já existente.
  * `cp -n [arquivo] [destino]`: Não sobrescreve um arquivo já existente.
  * `cp -r [arquivo] [destino]`: Copia diretórios de forma recursiva.
  * `cp -p [arquivo] [destino]`: Preserva as permissões originais do arquivo (proprietário, grupo, etc.).
  * `cp -vr [arquivo] [destino]`: Copia diretorios recursivamente.

[Ver exemplo](examples/copiando-diretorios-e-arquivos.md)

## Movendo e renomeando arquivos e pastas

Podemos mover arquivos com o comando mv.

* `mv [arquivo] [destino]`: Move um arquivo para um determinado destino.
  * `mv -b [arquivo] [destino]`: Cria um backup de cada arquivo destino existente.
  * `mv -f [arquivo] [destino]`: Apaga destinos existente sem perguntar ao usuário.
  * `mv -i [arquivo] [destino]`: Pergunta se desejamos sobrescrever o arquivo destino já existente.
  * `mv -n [arquivo] [destino]`: Não sobrescrever um arquivo destino já existente.

O comando mv também é usado para renomear arquivos.

* `mv [nome_atual.extenção] [novo_nome.extenção]`

[Ver exemplo](examples/movendo-e-renomeando-arquivos-e-pastas.md)

## Visualização de arquivos

* `more [arquivo]`: Mostra o conteúdo de um arquivo em partes.

* `less [arquivo]`: Exibi o conteúdo de um arquivo páginado.

* `tac [arquivo]`: Exibi o conteúdo de um arquivo de trás pra frente (da última linha pra primeira).

* `cat [arquivo]`: Abre o arquivo em modo de visualização.
  * `cat -E [arquivo]`: Marca o término de linha mostrando o caractere $ ao final de cada uma delas.
  * `cat -n [arquivo]`: Mostra a quantidade de linas do arquivo.
  * `cat -v [arquivo]`: Exibe caracteres não exibíveis.
  * `cat -T [arquivo]`: Exibe tabulação mostradas como ^I.
  * `cat -s [arquivo]`: Remove linhas repetidas em branco.
  * `cat -b [arquivo]`: Numera as linhas que possuem algum conteúdo.
  * `cat [arquivo] | grep [busca]`: Busca no arquivo (case sensitive).
  * `cat [arquivo] | grep [busca] -i`: Busca no arquivo (case insensitive).
  * `cat [arquivo] > [arquivo]`: Copia o conteúdo do arquivo para outro.
  * `cat [arquivo] >> [arquivo]`: Adiciona o conteúdo do arquivo para outro.

[Ver exemplo](examples/visualizacao-de-arquivos.md)

## Compressão de arquivos

* `tar cf pacote.tar [arquivos]`: Cria um pacote TAR (nomeado pacote.tar) com os arquivos especificados.
* `tar xf pacote.tar`: Extrai os arquivos de "pacote.tar" (substituir a variável pacote.tar pelo nome do arquivo).

* `tar czf pacote.tar.gz [arquivos]`: Cria um pacote TAR (nomeado pacote.tar.gz) com compressão GZip.
* `tar xzf pacote.tar.gz`: Extrai um pacote TAR (nomeado pacote.tar.gz) com compressão GZip.

* `tar cjf pacote.tar.bz2 [arquivos]`: Cria um pacote TAR (nomeado pacote.tar.bz2) com compressão BZip2.
* `tar xjf pacote.tar.bz2`: Extrai um pacote TAR (nomeado pacote.tar.gz) com compressão BZip2.

* `gzip arq`: Compacta um arquivo e o renomeia para arq.gz (substituir a variável arq pelo nome do arquivo).
* `gzip -d arq.gz`: Descompacta arq.gz para um arquivo (substituir a variável arq.gz pelo nome do arquivo).

[Ver exemplo](examples/compressao-de-arquivos.md)

# Buscas

## Buscando por arquivos

Podemos buscar por arquivos específicos em todo nosso sistema com o comando find.

* `find .`: Lista todos os arquivos contidos em um diretório e subdiretórios.
* `find . -name [arquivo]`: Busca um arquivo com um nome especifico.
* `find [diretório] -iname [arquivo]`: Procura ignorando case sensitive.

[Ver exemplo](examples/buscando-por-arquivos.md)

## Referência global

Referências globais são recursos para especificar um ou mais arquivos ou diretórios de uma vez. Vamos usar o comando 'ls' para os exemplos, mas pode ser usado __qualquer__ outro comando.

* `ls /etc/*.conf`: Lista todos os arquivos que tem a extenção '.conf'.
* `ls /etc/*x*`: Lista todos os aquivos que em algum lugar do nome tem a lera 'x'.
* `ls /etc/f*`: Lista todos os aquivos que começa com a letra 'f'.
* `ls /etc/?as*`: Lista todos os arquivos que começa com uma letra qualquer, tem segundo caractere 'a', o terceiro 's' e qualquer caractere depois.
* `ls /etc/???a*`: Lista todos os arquivos que tem o quarto caractere 'a'.
* `ls /etc/f[a-t]*`: Lista todos os aqruivos que começa com a letra 'f', depois a segunda letra varia do 'a' ao 't' e depois qualquer caractere.
* `ls /etc/f[u,o]*`: Lista todos os aqruivos que começa com a letra 'f', depois a segunda letra é 'u' ou 'o' e depois qualquer caractere.
* `ls /etc/?[a,e,i,o,u]*`: Lista todos os aqruivos que começa com uma letra qualquer, depois a segunda letra é uma vogal e depois qualquer caractere.
* `ls /etc/?[a,e,i,o,u]???`: Lista todos os aqruivos que começa com uma letra qualquer, depois a segunda letra é uma vogal e depois tem mais 3 caracteres qualquer.
* `ls /etc/?{am,ul}*`: Lista todos os aqruivos que começa com uma letra qualquer, depois a segunda e a terceira letra é 'am' ou 'ul' e depois qualquer caractere.
* `ls /etc/*{ev,ux}`: Lista todos os aqruivos que termina com 'ev' ou 'ux'.
* `ls /etc/*.{conf,db}`: Lista todos os aqruivos que tem a extenção '.conf' ou '.db'.

# Sistema

## Processos

* `top`: Exibe os processos usando a maioria dos recursos do sistema, a qualquer momento. "Q" pode ser usado para sair.

* `htop`: O comando HTOP é uma evolução do comando TOP. As informações são semelhantes às produzidas pelo comando TOP, mas apresentadas num interface mais intuitivo e colorido.

* `kill pid`: Mata o processo com o id de processo pid.
* `killall Discord`: Mata todos os processo com o nome discord.
* `pkill fire`: Mata todos os processo que tenha "fire" em seu nome.

* `ps`: O comando ps exibe informações sobre os processos que estão executando na máquina.
  * `ps -a`: Mostra os processos de todos os usuários.
  * `ps -A` ou `ps -e`: Mostra todos os processos.
  * `ps -f`: Mostra a árvore de execução de comandos.
  * `ps -g [grupo]`: Mostra os processos de um determinado grupo.
  * `ps -x`: Mostra os processos que não foram iniciados no console.
  * `ps -u`: Fornece o nome do usuário e a hora de início do processo.
  * `ps -aux`: exibe todos os processos do sistema independente de terminal.

[Ver exemplo](examples/processos.md)

## Informações do sistema

* `whereis [programa]`: Exibe possíveis localizações de um determinado programa.
* `date`: Exibe a data e hora atual.
* `whoami`: Imprime o nome de usuário usado no momento em que foi digitado.
* `sudo su`: Entra no modo usuário root.
* `exit`: Sai do usuário logado no momento que o comando é executado.

__Observação__: Quando você for digitar sua senha para entrar no modo usuário root, por questões de segurança o terminal não exibe nada na tela o que foi digitado.

* `uname -a ou uname --all`: imprime todas as informações, omitindo uname -p e uname -i se as informações forem desconhecidas.
* `uname -s ou uname --kernel-name`: Imprime o nome do kernel.
* `uname -n ou uname --nodename`: Imprime o nome do host do nó da rede.
* `uname -r ou uname --kernel-release`: Imprime a versão do kernel.
* `uname -v ou uname --kernel-version`: Imprime a versão do kernel.
* `uname -m ou uname --machine`: Imprime o nome do hardware da máquina.
* `uname -p ou uname --processor`: Imprime o tipo de processador ou " desconhecido ".
* `uname -i ou uname --hardware-platform`: Imprime a plataforma de hardware, ou " desconhecido ".
* `uname -o ou uname --operating-system`: Imprime o sistema operacional.
* `uname --version`: Exibe informações da versão.

[Ver exemplo](examples/informacoes-do-sistema.md)

## Memória

* `free`: Este comando exibe a quantidade de espaço livre disponível no sistema.

* `df`: Exibe informações sobre o uso do espaço em disco de todos os sistemas de arquivos montados.
  * `df -a`: Inclui sistema de arquivos com 0 (zero) blocos.
  * `df -h`: Mostra o espaço livre/ocupado em MB, KB, GB em vez de bloco.
  * `df -k`: Lista em Kbyts.
  * `df -l`: Somente lista sistema de arquivos locais.
  * `df -m`: Lista em Mbytes.
  * `df -T`: Lista o tipo de sistema de arquivos de cada partição.

[Ver exemplo](examples/memoria.md)

## Programas e atualizações

* `sudo apt-get update`: Baixa os pacotes disponíveis.
* `sudo apt-get upgrade`: Atualiza os pacotes do sistema.
* `sudo apt-get clean`: Remove cache de programas.
* `sudo apt-get cache [busca]`: Busca um programa.
* `sudo apt-get install [programa]`: Instala um programa.
* `sudo apt-get remove [pacote] --purge`: Remove programas e configs.

__Observação__: Se você estiver logado como usuário root, não é necessário o uso do 'sudo' na frente dos comandos.

## Usuários

### Trocando senha de usuários

O `passwd` é um comando utilizado para configurar ou trocar a senha das contas dos usuários do sistema. É necessário possuir privilégios administrativos para executá-lo, mas um usuário comum consegue alterar sua própria senha.

* `passwd [usuário]`: Troca/Configura a senha de um determinado usruário.
  * `passwd -l [usuário]`: Trava a senha do usuário, ficando impedido de se logar e não pode trocar a senha (não é desabilitado).
  * `passwd -u [usuário]`: Destrava a senha do usuário.
  * `passwd -d [usuário]`: Exclui a senha do usuário.
  * `passwd -e [usuário]`: Expira a senha do usuário, forçando-o a fornecer uma nova ao logar-se novamente.
  * `passwd -x dias [usuário]`: Expira a senha do usuário quando atingir o número de dias especificados.
  * `passwd -n dias [usuário]`: Define a quantidade mínima de dias que o usuário deverá esperar para trocar a senha.
  * `passwd -w dias [usuário]`: define a quantidade mínima de dias que o usuário receberá o aviso que a senha precisa ser alterada.
  * `passwd -i [usuário]`: Deixa o usuário inativo, caso a senha tenha expirado.
  * `passwd -S [usuário]`: Exibe o status da conta.
  * `passwd -a [usuário]`: Usada em conjunto com a opção -S mostra o status das contas de todos os usuários.

## Tipos de usuários

### Usuários comuns

São os usuários que podem se conectar no sistema. Geralmente, estes usuários possuem uma home e podem manipular arquivos quando tem as permissões para tal. Porém estes usuários geralmente não tem permissão para certos arquivos e diretórios na maquina e não podem executar muitas funções a nível de sistema.

Exemplo de um usuário comum: `roger@roger:~$`

### Usuários de sistema

Diferente dos usuários comuns, estes usuários não se conectam no sistema. São contas usadas para tarefas específicas dentro do sistema que não são de propriedade de uma pessoa em particular.

### Root

O usuário root, também chamado de superusuário, tem controle total sobre o sistema operacional. Ele pode acessar todos os arquivos e normalmente é o único que pode executar certos programas, como por exemplo o httpd.

Exemplo de um usuário root: `root@roger:~#`

__Observação__: Não é recomendado que você use o terminal no modo root o tempo inteiro.

### Grupos

Um grupo é um conjunto de um ou mais usuários. É interessante reunir vários usuários em um grupo para definir suas propriedades, como as permissões. Como o arquivo passwd nós temos um arquivo somente para armazenar detalhes sobre os grupos.
Esse arquivo esta localizado em: `/etc/group`.

## Gerenciamento de usuários

### Adicionar usuários

Criar um usuário novo no Linux é bem simples, apenas é necessário o comando useradd e indicar o nome do novo usuário.

* `useradd [nomeusuario]`: Cria um novo usuário.
  * `useradd -d [nomeusuario]`: Define o nome do diretório home do usuário (mas não o cria).
  * `useradd -s [nomeusuario]`: Define o shell padrão do usuário.
  * `useradd -h [nomeusuario]`: Exibe as opções do comando.

### Alterar usuários

Para alterarmos uma conta de usuário basta apenas utilizarmos o comando usermod.

* `usermod [nomeusuário]`: Altera um usário.
  * `usermod -d diretório [-m] [nomeusuário]`: Cria uma nova home para o usuário. A opção -m move os arquivos da home atual do usuário para a nova.
  * `usermod -e yyyy-mm-dd [nomeusuário]`: Altera a data de expiração da conta do usuário.
  * `usermod -g grupo [nomeusuário]`: Altera o GID do grupo do usuário para o especificado.
  * `usermod -G grupo[, grupo2, ...] [nomeusuário]`: Define o GID dos outros grupos que o usuário pertence.
  * `usermod -l nome [nomeusuário]`: Altera o nome do usuário (ele não pode estar logado).
  * `usermod -s shell [nomeusuário]`: Altera o shell do usuário.
  * `usermod -u uid [nomeusuário]`: Altera o número de UID do usuário.

### Remover usuários

Para removermos um usuário utilizamos o comando userdel.

* `userdel [nomeusuario]`: Remove um usuário.
  * `userdel -h [nomeusuario]`: Exibe as opções do comando.
  * `userdel -r [nomeusuario]`: Deleta a home e todos os seus arquivos.

## Calculadora

* `bc`: Abre uma calculadora do Bash

__Observação__: Para sair bastas digitar 'quit' e apertar enter ou 'Ctrl+d'.

[Ver exemplo](examples/calculadora.md)

## Referências

* [Curso de Linux - Primeiros Passos](https://www.youtube.com/watch?v=6nN2EglOqCM&list=PLHz_AreHm4dlIXleu20uwPWFOSswqLYbV)
* [Curso de Linux Básico / Certificação LPIC - 1](https://www.youtube.com/watch?v=UsHiWIgxj2M&list=PLucm8g_ezqNp92MmkF9p_cj4yhT-fCTl7)
* [linux4noobs](https://github.com/LucasHe4rt/linux4noobs)

[VOLTAR AO TOPO](#roadmap)
