# Linux para iniciantes

## Um pouco de História

O Kernel do Linux foi inicialmente desenvolvido pelo estudante finlandês Linus Torvalds numa tentativa de conseguir o seu próprio sistema operativo semelhante ao Unix (Unix-like) que corresse em processadores Intel 80386.

Linus obteve uma cópia do Minix estudou a mesma não ficando satisfeito com sua arquitetura. O projeto foi lançado em 1991 numa famosa mensagem para um grupo de discussão da Usenet. Curiosamente, o nome Linux foi criado por Ari Lemmke, administrador do site ftp.funet.fi que deu esse nome ao diretório FTP onde o kernel do linux estava inicialmente disponível (Linus tinha batizado como "Freax", inicialmente). Desde o princípio, ele recebeu a ajuda de hackers do Minix, e hoje recebe contribuições de milhares de programadores de todo mundo.

## Arquitetura

O Linux é um núcleo (kernel) monolítico. Isto é, as funções do núcleo (agendamento de processos, gerenciamento de memória, operações de entrada e saída, acesso ao sistema de arquivos) são executadas no espaço do núcleo. Uma característica do Linux é que algumas das funções (drivers de dispositivos, suporte à rede, sistemas de arquivo, por exemplo) podem ser compiladas e executadas
como módulos (LKM - loadable kernel modules), que são bibliotecas compiladas separadamente da parte principal do núcleo e podem ser carregadas e descarregadas após o núcleo estar em execução

## Portabilidade

Embora Linus Torvalds não tenha tido como objetivo inicial tornar o Linux um sistema portável, ele evoluiu nessa direção. Linux é hoje, na verdade, um dos núcleos (kernels) de sistema operacional com mais portabilidade, correndo em sistemas desde o iPaq (um computador portátil) até o IBM S/390 (um denso e altamente custoso mainframe)

De qualquer modo, é importante notar que os esforços de Linus foram também dirigidos a um diferente tipo de portabilidade. Portabilidade, de acordo com Linus, era a habilidade de facilmente compilar aplicações de uma variedade de fontes no seu sistema; portanto o Linux originalmente tornou-se popular em parte devido ao esforço para que as fontes GPL ou outras favoritas de todos executassem em Linux.

## Termos de Licenciamento

Inicialmente, Torvalds lançou o Linux sob uma licença que proibia qualquer uso comercial. Isso foi mudado de imediato para a Licença Pública Geral GNU. Essa licença permite a distribuição e mesmo a venda de versões possivelmente modificadas do Linux mas requer que todas as cópias sejam lançadas dentro da mesma licença e acompanhadas do código fonte.

## Distribuições

Atualmente, um Sistema Operacional GNU/Linux completo (equivalente a "distribuição de GNU/Linux") é uma coleção de software livre (e alguns não-livres) criados por indivíduos, grupos e organizações de todo o mundo, tendo o Linux como seu núcleo. Companhias como a Red Hat, a SuSE, a Mandriva (união da Mandrake com a Conectiva), bem como projetos de comunidades como o Debian ou o Gentoo,
compilam o software e fornecem um sistema completo, pronto para instalação e uso.

Dentre as maiores, distribuídas em CDs, podem-se citar: Slackware, Debian, Suse, Ubuntu e Conectiva. O que faz a diferença é como estão organizadas e pré-configuradas as aplicações. A distribuição Conectiva Linux, por exemplo, tinha as suas aplicações traduzidas em português, o que facilitou que usuários que falam a Lingua Portuguesa tenham aderido melhor a esta distribuição. Hoje esta Apostila elaborada por Fernando Henrique e Paula da Luz - presidente@ifsc.usp.br Mestrando em Física Computacional pelo Instituto de Física de São Carlos distribuição foi incorporada à Mandrake, o que resultou na Mandriva. Para o português, existe também a distribuição brasileira Kurumin, construída sobre Knoppix e Debian.

## O que é uma shell?

No mundo da computação, uma shell é um programa que interpreta comandos do usuario para que o sistema operacional possa entender e executar o que lhe é pedido.

A shell é uma interface em linha de comando, baseada em texto. O usuário pode digitar comandos para executar funções ou programas, abrir e navegar diretórios, e ver processos que estão ocorrendo no momento. Sendo a shell a unica camada para o sistema operacional, você pode fazer operações que não são possiveis usando usando uma interface grafica do usuario (do ingles GUI - graphical user interface). Alguns exemplos inclui mover arquivos dentro das pastas de sistema e deletar arquivos que são
tipicamentes bloqueados. Para executar isso, você precisa saber as a sintaxe correta dos comandos e permitir o seu acesso como administrador do sistema.

Duas shells mais comumente utilizadas são a Bourne Again Shell (bash) e a Tenex C shell (tcsh).

Vale ressaltar que na linha de comandos de uma shell, podemos utilizar diversos comandos um após o outro, ou até mesmo combiná-los numa mesma linha. Se colocarmos diversas linhas de comandos em um arquivo texto simples, teremos em mãos um Shell Script, ou um script em shell, já que Script é uma descrição geral de qualquer programa escrito em linguagem inte

## Terminal Linux

### Atalhos globais

Atalho                  | Ação
------------------------|------------------------
`Ctrl + Shift + C`      | Copiar.
`Ctrl + Shift + V`      | Colar.
`Ctrl + C`              | Cancela o comando atual em funcionamento.
`Ctrl + Z`              | Pausa o comando atual, retorna com "fg" em primeiro plano Linux ou "bg" em segundo plano.
`Ctrl + D`              | Faz o logout da sessão atual (similar ao comando "exit").
`Ctrl + W`              | Apaga uma palavra na linha atual.
`Ctrl + U`              | Apaga a linha inteira.
`Ctrl + R`              | Tecle para Exiber um comando recente.
`Ctrl + L`              | Limpa a tela.

### Diretórios

Duretório   | Ação
------------|------------------------
`/`         | É o diretório raiz, todos os demais diretórios estão abaixo dele.
`/bin/`     | Binários principais dos usuários.
`/boot/`    | Arquivos do sistema de Boot.
`/dev/`     | Arquivos de dispositivos.
`/etc/`     | Arquivos de configuração do sistema.
`/home/`    | Diretório dos usuários comuns do sistema.
`/lib/`     | Bibliotecas essenciais do sistema e os módulos do kernel.
`/media/`   | Diretório de montagem e dispositivos.
`/mnt/`     | Diretório de montagem de dispositivos - mesmo que "media".
`/opt/`     | Instalação de programas não oficiais da distribuição ou por conta do usuário.
`/sbin/`    | Armazena arquivos executáveis que representam comandos administrativos. Exemplo: shutdown
`/srv/`     | Diretório para dados de serviços fornecidos pelo sistema.
`/tmp/`     | Diretório para arquivos temporários.
`/usr/`     | Segunda hierarquia do sistema, onde ficam os usuários comuns do sistema e programas.
`/var/`     | Diretório com arquivos variáveis gerados pelos programas do sistema. Exemplo: logs, spool de impressoras, e-mail e cache.
`/root/`    | Diretório do usuário root - O usuário root tem o total poder sobre o sistema. Podendo instalar, desinstalar e configurar.
`/proc/`    | Diretório virtual controlado pelo Kernel com configuração total do sistema.

### Ajuda no Terminal

*`apropos [expressão]`: Este comando procura por uma determinada expressão nas páginas de documentação do Linux.

Observações:
  * O comando man -k tem o mesmo comportamento do comando apropos.
  * O comando mandb cria/atualiza a base de dados acessada pelo comando apropos.
  * O comando whatis mostra um resumo sobre um ou mais comandos.
  * O comando xman é um navegador para as páginas on-line.

* `[comando] --help`: Documentação do comando.

* `man [comando]`: Manual do comando.

* `info [comando]`: Semelhante ao man, mas geralmente fornece informações mais detalhadas.

Histórico de comandos:

* `!!`: Repete o último comando.
* `history`: Lista o histórico de 2000 comandos digitados.
* Seta para cima e seta para baixo: Últimos comandos digitados.

* `bc`: Abre uma calculadora

Observação: Para sair bastas digitar 'q' ou 'Ctrl+d'.

### Manipulando Arquivos e Diretórios

Listagem de arquivos:

* `ls [opções]`: Podemos listar o conteúdo de um diretório utilizando o comando ls.
  * -a: Lista todos os arquivos e diretórios ocultos.
  * -l: Formato longo, mostra permissões, número de links, propietário, grupo, tamanho, data de modificação e nome do arquivo.
  * -h: Lista arquivos e diretórios com informações formatadas (Tem que ser usado com o -l).
  * -R: Lista os arquivos e pastas recursivamente.
  * -p: Mostra uma barra (/) na frente de nomes de diretórios.

Entrando e saíndo de diretórios:

* `cd`: Podemos entrar e sair de um diretório utilizando o comando cd.
  * cd [destino]: Parte do local corrente até o diretório passado como referência.
  * cd /[destino]: Partindo da raiz até o último diretório passado como referência.
  * cd ..: Volta um diretório.
  * cd /: Vai direto para o diretório raiz.
  * cd ~: Vai direto para o diretório home.
  * cd -: Nos retorna para o último diretório acessado.

* `pwd`: Exibe o caminho de diretório atual.

* `du` [diretório]: Exibe o tamanho de um diretório e todos os seus subdiretórios.

Criando diretórios:

* `mkdir [nome-do-diretorio]`: Podemos criar diretórios utilizando o comando mkdir.
  * mkdir pasta1 pasta2 pasta3: Cria três pastas, pasta1, pasta2 e pasta3.
  * mkdir -p A/B/C: Cria a pasta A, dentro da pasta A cria a pasta B e dentro da pasta B cria a pasta C.

Criando arquivos:

* `touch [opções] [arquivo]`: Podemos criar arquivos utilizando o comando touch.
  * -a: Altera a hora de acesso do arquivo.
  * -m: Altera a hora de modificação do arquivo.
  * -am: Altera a hora de acesso e modificação do arquivo.
  * -c: Altera a hora de acesso sem criar um novo arquivo.

Observação: podemos gerar nomes automáticos usando as chaves {}, desta maneira: touch exemplo{1..3}.txt, este comando irá criar 3 arquivos chamados exemplo1.txt, exemplo2.txt e exemplo3.txt.

Excluíndo diretórios e arquivos: 

* `rm [opções] [arquivo]`: Podemos excluir arquivos utilizando o comando rm.
  * -f: Exclui arquivos forçadamente.
  * -r: Exclui o diretório e os arquivos na direção recursiva.
  * -d: Remove somente diretórios vazios.
  * -i: Pergunta se queremos remover o arquivo/diretório antes de excluir.

Copiando diretórios e arquivos:

* `cp [opções] [arquivo] [destino]`: Podemos copiar arquivos utilizando o comando cp.
  * -r: Copia diretórios de forma recursiva.
  * -p: Preserva as permissões originais do arquivo (proprietário, grupo, etc.).
  * -i: Pergunta se desejamos sobrescrever um arquivo destino já existente.
  * -n: Não sobrescreve um arquivo já existente.

Movendo e renomeando arquivos e diretórios:

* `mv [opções] [arquivo] [destino]`: Podemos mover arquivos com o comando mv.
  * -b: Cria um backup de cada arquivo destino existente.
  * -f: Apaga destinos existente sem perguntar ao usuário.
  * -i: Pergunta se desejamos sobrescrever o arquivo destino já existente.
  * -n: Não sobrescrever um arquivo destino já existente.

O comando mv também é usado para renomear arquivos.

* `mv [nome_atual.extenção] [novo_nome.extenção]`

Visualização de arquivos:

* `more [arquivo]`: Mostra o conteúdo de um arquivo em partes.

* `less [arquivo]`: Exibi o conteúdo de um arquivo páginado.

* `tac [arquivo]`: Exibi o conteúdo de um arquivo de trás pra frente (da última linha pra primeira).

* `cat [opções] [arquivo]`: Abre o arquivo em modo de visualização.
  * -n: Mostra a quantidade de linas do arquivo.
  * -v: Exibe caracteres não exibíveis.
  * -T: Exibe tabulação mostradas como ^I.
  * -s: Remove linhas repetidas em branco.
  * -b: Numera as linhas que possuem algum conteúdo.

Busca e manilupalção de conteúdo:

* `cat [opções] [arquivo] | grep [busca]`: Busca no arquivo (case sensitive).
* `cat [opções] [arquivo] | grep [busca] -i`: Busca no arquivo (case insensitive).
* `cat [opções] [arquivo] > [arquivo]`: Copia o conteúdo do arquivo para outro.
* `cat [opções] [arquivo] >> [arquivo]`: Adiciona o conteúdo do arquivo para outro.

Compressão de arquivos:

Tar:

* `tar cf pacote.tar [arquivos]`: Cria um pacote TAR (nomeado pacote.tar) com os arquivos especificados.
* `tar xf pacote.tar`: Extrai os arquivos de "pacote.tar" (substituir a variável pacote.tar pelo nome do arquivo).

GZip:

* `tar czf pacote.tar.gz [arquivos]`: Cria um pacote TAR (nomeado pacote.tar.gz) com compressão GZip.
* `tar xzf pacote.tar.gz`: Extrai um pacote TAR (nomeado pacote.tar.gz) com compressão GZip.

bz2:

* `tar cjf pacote.tar.bz2 [arquivos]`: Cria um pacote TAR (nomeado pacote.tar.bz2) com compressão BZip2.
* `tar xjf pacote.tar.bz2`: Extrai um pacote TAR (nomeado pacote.tar.gz) com compressão BZip2.

Gz:
* `gzip arq`: Compacta um arquivo e o renomeia para arq.gz (substituir a variável arq pelo nome do arquivo).
* `gzip -d arq.gz`: Descompacta arq.gz para um arquivo (substituir a variável arq.gz pelo nome do arquivo).

### Buscas no Terminal

Buscando por arquivos

Podemos buscar por arquivos específicos em todo nosso sistema com o comando find.

* `find .`: Lista todos os arquivos contidos em um diretório e subdiretórios.

* `find . -name [arquivo]`: Busca um arquivo com um nome especifico.

* `find [diretório] -iname [arquivo]`: Procura ignorando case sensitive.

Referência global:

Referências globais são recursos para especificar um ou mais arquivos ou diretórios de uma vez. Vamos usar o comando 'ls' para os exemplos, mas pode ser usado qualquer outro comando.

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

### Sistema

Processos:

* `top`: Exibe os processos usando a maioria dos recursos do sistema, a qualquer momento. "Q" pode ser usado para sair.

* `htop`: O comando HTOP é uma evolução do comando TOP. As informações são semelhantes às produzidas pelo comando TOP, mas apresentadas num interface mais intuitivo e colorido.

* `kill pid`: Mata o processo com o id de processo pid.

* `killall Discord`: Mata todos os processo com o nome "Discord".

* `pkill fire`: Mata todos os processo que tenha "fire" em seu nome.

* `ps [opções]`: O comando ps exibe informações sobre os processos que estão executando na máquina.
  * -a: Mostra os processos de todos os usuários.
  * -A ou -e: Mostra todos os processos.
  * -f: Mostra a árvore de execução de comandos.
  * -g [grupo]: Mostra os processos de um determinado grupo.
  * -x: Mostra os processos que não foram iniciados no console.
  * -u: Fornece o nome do usuário e a hora de início do processo.
  * -aux: exibe todos os processos do sistema independente de terminal.

Informações do sistema:

* `whereis [programa]`: Exibe possíveis localizações de um determinado programa.

* `date`: Exibe a data e hora atual.

* `whoami`: Imprime o nome de usuário usado no momento em que foi digitado.

* `sudo su`: Entra no modo usuário root.

* `uname [opções]`: Mostra informações sobre o sistema operacional.
  * -a: imprime todas as informações, omitindo uname -p e uname -i se as informações forem desconhecidas.
  * -s: Imprime o nome do kernel.
  * -n: Imprime o nome do host do nó da rede.
  * -r ou -v: Imprime a versão do kernel.
  * -m: Imprime o nome do hardware da máquina.
  * -p: Imprime o tipo de processador ou " desconhecido ".
  * -i: Imprime a plataforma de hardware, ou " desconhecido ".
  * -o: Imprime o sistema operacional.
  * --version: Exibe informações da versão.

Memória:

* `free`: Este comando exibe a quantidade de espaço livre disponível no sistema.

* `df [opções]`: Exibe informações sobre o uso do espaço em disco de todos os sistemas de arquivos montados.
  * -a: Inclui sistema de arquivos com 0 (zero) blocos.
  * -h: Mostra o espaço livre/ocupado em MB, KB, GB em vez de bloco.
  * -k: Lista em Kbyts.
  * -l: Somente lista sistema de arquivos locais.
  * -m: Lista em Mbytes.
  * -T: Lista o tipo de sistema de arquivos de cada partição.

Programas e atualizações:

Cada distribuição linux possúi o seu gerenciador de pacotes própio. Neste caso usarei o `apt`

* `sudo apt update`: Baixa os pacotes disponíveis.
* `sudo apt upgrade`: Atualiza os pacotes do sistema.

* `sudo apt install [programa]`: Instala um programa.
* `sudo apt remove [pacote] --purge`: Remove programas e configs.
* `sudo apt cache [busca]`: Busca um programa.

* `sudo apt autoremove`: Remove pacotes que não são mais requeridos dentro do sistema.
* `sudo apt clean`: Remove cache de programas.
* `sudo apt autoclean`: limpa o seu repositório local, removendo os arquivos de pacotes que não podem mais ser baixados (versões antigas…) e são completamente inúteis e obsoletos.

Observação: Se você estiver logado como usuário root, não é necessário o uso do 'sudo' na frente dos comandos.

Usuários:

Adicionar usuários:

Criar um usuário novo no Linux é bem simples, apenas é necessário o comando useradd e indicar o nome do novo usuário.

* `useradd [opções] [nomeusuario]`: Cria um novo usuário.
  * -d: Define o nome do diretório home do usuário (mas não o cria).
  * -s: Define o shell padrão do usuário.
  * -h: Exibe as opções do comando.

Alterar usuários:

Para alterarmos uma conta de usuário basta apenas utilizarmos o comando usermod.

* `usermod [opções] [nomeusuário]`: Altera um usário.
  * -d diretório [-m]: Cria uma nova home para o usuário. A opção -m move os arquivos da home atual do usuário para a nova.
  * -e yyyy-mm-dd: Altera a data de expiração da conta do usuário.
  * -g grupo: Altera o GID do grupo do usuário para o especificado.
  * -G grupo[, grupo2, ...]: Define o GID dos outros grupos que o usuário pertence.
  * -l nome: Altera o nome do usuário (ele não pode estar logado).
  * -s shell: Altera o shell do usuário.
  * -u uid: Altera o número de UID do usuário.

Remover usuários:

Para removermos um usuário utilizamos o comando userdel.

* `userdel [opções] [nomeusuario]`: Remove um usuário.
  * -h: Exibe as opções do comando.
  * -r: Deleta a home e todos os seus arquivos.

Trocar senha de usuários:

* `passwd [opções] [usuário]`: O passwd é um comando utilizado para configurar ou trocar a senha das contas dos usuários do sistema. É necessário possuir privilégios administrativos para executá-lo, mas um usuário comum consegue alterar sua própria senha.
  * -l: Trava a senha do usuário, ficando impedido de se logar e não pode trocar a senha (não é desabilitado).
  * -u: Destrava a senha do usuário.
  * -d: Exclui a senha do usuário.
  * -e: Expira a senha do usuário, forçando-o a fornecer uma nova ao logar-se novamente.
  * -x dias: Expira a senha do usuário quando atingir o número de dias especificados.
  * -n dias: Define a quantidade mínima de dias que o usuário deverá esperar para trocar a senha.
  * -w dias: define a quantidade mínima de dias que o usuário receberá o aviso que a senha precisa ser alterada.
  * -i: Deixa o usuário inativo, caso a senha tenha expirado.
  * -S: Exibe o status da conta.
  * -a: Usada em conjunto com a opção -S mostra o status das contas de todos os usuários.
