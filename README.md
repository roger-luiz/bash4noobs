# Tutorial Git e Bash

Tutorial de Git e Bash para devs iniciantes.

## Bash

## Atalhos globais do Bash

- [X] **`Ctrl + Shift + C`** - Copiar.
- [X] **`Ctrl + Shift + V`** - Colar.
- [X] **`Ctrl + C`** - Cancela o comando atual em funcionamento.
- [X] **`Ctrl + Z`** - Pausa o comando atual, retorna com "fg" em primeiro plano Linux ou "bg" em segundo plano.
- [X] **`Ctrl + D`** - Faz o logout da sessão atual (similar ao comando "exit").
- [X] **`Ctrl + W`** - Apaga uma palavra na linha atual.
- [X] **`Ctrl + U`** - Apaga a linha inteira.
- [X] **`Ctrl + R`** - Tecle para Exiber um comando recente.
- [X] **`Ctrl + L`** - Limpa a tela.

## Diretórios

- [X] **`/`** - É o diretório raiz, todos os demais diretórios estão abaixo dele.
- [X] **`/bin/`** - Binários principais dos usuários.
- [X] **`/boot/`** - Arquivos do sistema de Boot.
- [X] **`/dev/`** - Arquivos de dispositivos.
- [X] **`/etc/`** - Arquivos de configuração do sistema.
- [X] **`/home/`** - Diretório dos usuários comuns do sistema.
- [X] **`/lib/`** - Bibliotecas essenciais do sistema e os módulos do kernel.
- [X] **`/media/`** - Diretório de montagem e dispositivos.
- [X] **`/mnt/`** - Diretório de montagem de dispositivos - mesmo que "media".
- [X] **`/opt/`** - Instalação de programas não oficiais da distribuição ou por conta do usuário.
- [X] **`/sbin/`** - Armazena arquivos executáveis que representam comandos administrativos. Exemplo: shutdown
- [X] **`/srv/`** - Diretório para dados de serviços fornecidos pelo sistema.
- [X] **`/tmp/`** - Diretório para arquivos temporários.
- [X] **`/usr/`** - Segunda hierarquia do sistema, onde ficam os usuários comuns do sistema e programas.
- [X] **`/var/`** - Diretório com arquivos variáveis gerados pelos programas do sistema. Exemplo: logs, spool de impressoras, e-mail e cache.
- [X] **`/root/`** - Diretório do usuário root - O usuário root tem o total poder sobre o sistema. Podendo instalar, desinstalar e configurar.
- [X] **`/proc/`** - Diretório virtual controlado pelo Kernel com configuração total do sistema.

## Ajuda

Você pode consultar a documentação e o manual de uso dos comandos das seguintes maneiras:

- [X] **`[comando] --help`** - Documentação do comando.
- [X] **`man [comando]`** - Manual do comando.
- [X] **`info [comando]`** - Semelhante ao man, mas geralmente fornece informações mais detalhadas ou precisas.

## Comando ls

O comando ls é usado para listar o conteúdo de um diretório.

- [X] **`ls [opções]`**
- [X] **`ls`** - Lista arquivos e diretórios.
- [X] **`ls -r`** - Lista arquivos e diretórios em ordem reversa.
- [X] **`ls -a`** - Lista todos os arquivos e diretórios, incluindo arquivos ocultos.
- [X] **`ls -l`** - Formato longo, mostra permissões, número de links, propietário, grupo, tamanho, data de modificação e nome do arquivo.
- [X] **`ls -h`** - Lista arquivos e diretórios com informações formatadas ( Tem que ser usado com o -l ).
- [X] **`ls -ls`** - Lista arquivos e diretórios pelo tamanho, no caso começará pelo o arquivo de maior tamanho.
- [X] **`ls -R`** - Lista os arquivos e pastas recursivamente da pasta selecionada.
- [X] **`ls -m`** - Arquivos listados em sequência, separados por vírgula.
- [X] **`ls -n`** - Semelhante ao -l, porém mostra UID E GID Em vez de nomes de proprietário e grupo.
- [X] **`ls -o`** - Semelhante ao -l, porém não mostra o grupo do arquivo.
- [X] **`ls -p`** - Mostra uma barra ( / ) na frente de nomes de diretórios.
- [X] **`ls -A`** - Semelhante ao -a, mas não mostra o diretório corrente ( . ) ou o diretório acima ( .. ).
- [X] **`ls -i`** - Mostra o número do inode de cada arquivo na primeira coluna.

## Comando cd

O comando cd é usado para entrar em uma determinda pasta.

- [X] **`cd [destino]`**
- [X] **`cd .`** ou **`.`** - Diretório atual.
- [X] **`cd ..`** - Volta um diretório.
- [X] **`cd /`** - Vai direto para o diretório raiz.
- [X] **`cd ~`** - Vai direto para o diretório home.
- [X] **`cd -`** - Nos retorna para o último diretório acessado.
- [X] **`cd /diretorio`** - Partindo da raiz até o último diretório passado como referência.
- [X] **`cd diretorio`** - Parte do local corrente até o diretório passado como referência.

## Comando pwd

- [X] **`pwd`** - Exibe o caminho de diretório atual.

## Comando mkdir

O comando mkdir é usado para criar pastas

- [X] **`mkdir [nomeDaPasta]`** - Cria uma pasta.
- [X] **`mkdir pasta1 pasta2 pasta3`** - Cria três pastas, pasta1, pasta2 e pasta3.
- [X] **`mkdir -p A/B/C`** - Cria a pasta A, dentro da pasta A cria a pasta B e dentro da pasta B cria a pasta C.

## Comando du

- [X] **`du`** - Exibe o tamanho de um diretório e todos os seus subdiretórios.

## Comando touch

O comando touch é usado para criar arquivos.

- [X] **`touch [opções] [arquivo]`**
- [X] **`touch [arquivo]`** - Cria uma arquivo.
- [X] **`touch -a [arquivo]`** - Altera a hora de acesso do arquivo.
- [X] **`touch -m [arquivo]`** - Altera a hora de modificação do arquivo.
- [X] **`touch -am [arquivo]`** - Altera a hora de acesso e modificação do arquivo.
- [X] **`touch -c [arquivo]`** - Altera a hora de acesso sem criar um novo arquivo.

**`Observação`**: podemos gerar nomes automáticos usando as chaves {} desta maneira: touch exemplo{1..3}.txt, este comando irá criar 3 arquivos chamados exemplo1.txt, exemplo2.txt e exemplo3.txt.

## Comando rm

O comando rm é usado para excluir arquivos.

- [X] **`rm [opções] [arquivo]`**
- [X] **`rm`** - Exclui um arquivo.
- [X] **`rm -f`** - Exclui arquivos forçadamente.
- [X] **`rm -r`** - Exclui o diretório e os arquivos na direção recursiva, o diretório especificado junto com seu subdiretório e arquivos.
- [X] **`rm -d`** - Remove somente diretórios vazios.
- [X] **`rm -i`** - Pergunta se queremos remover o arquivo/diretório antes de excluir.
- [X] **`rm -rf`** - (rm -r) + (rm -f) ( utilize esse comando com extrema atenção! ).

## Comando cp

O comando cp é usado para copiar arquivos.

- [X] **`cp [opções] [arquivo] [destino]`**
- [X] **`cp -i [arquivo] [destino]`** - Pergunta se desejamos sobrescrever um arquivo destino já existente.
- [X] **`cp -n [arquivo] [destino]`** - Não sobrescreve um arquivo já existente.
- [X] **`cp -r [arquivo] [destino]`** - Copia diretórios de forma recursiva.
- [X] **`cp -p [arquivo] [destino]`** - Preserva as permissões originais do arquivo (proprietário, grupo, etc.).
- [X] **`cp -vr [origem] [destino]`** - copiar diretorio recursivamente.

## Comando mv

O comando mv é usado para mover arquivos.

- [X] **`mv [opções] [arquivo] [destino]`**
- [X] **`mv -b [arquivo] [destino]`** - Cria um backup de cada arquivo destino existente.
- [X] **`mv -f [arquivo] [destino]`** - Apaga destinos existente sem perguntar ao usuário.
- [X] **`mv -i [arquivo] [destino]`** - Pergunta se desejamos sobrescrever o arquivo destino já existente.
- [X] **`mv -n [arquivo] [destino]`** - Não sobrescrever um arquivo destino já existente.

O comando mv também é usado para renomear arquivos.

- [X] **`mv [nomeAtual.extenção] [novoNome.extenção]`**

## Visualização de arquivos

- [X] **`more [arquivo]`** - Mostra o conteúdo de um arquivo em partes.
- [X] **`less [arquivo]`** - Exibi o conteúdo de um arquivo páginado.
- [X] **`tac [arquivo]`** - Exibi o conteúdo de um arquivo de trás pra frente (da última linha pra primeira).
- [X] **`cat [opção] [arquivo]`**
- [X] **`cat`** - Abre o arquivo em modo de visualização.
- [X] **`cat -E [arquivo]`** - Marca o término de linha mostrando o caractere $ ao final de cada uma delas.
- [X] **`cat -n [arquivo]`** - Mostra a quantidade de linas do arquivo.
- [X] **`cat -v [arquivo]`** - Exibe caracteres não exibíveis.
- [X] **`cat -T [arquivo]`** - Exibe tabulação mostradas como ^I.
- [X] **`cat -s [arquivo]`** - Remove linhas repetidas em branco.
- [X] **`cat -b [arquivo]`** - Numera as linhas que possuem algum conteúdo.
- [X] **`cat [arquivo] | grep [busca]`** - Busca no arquivo (case sensitive).
- [X] **`cat [arquivo] | grep [busca] -i`** - Busca no arquivo (case insensitive).
- [X] **`cat [arquivo] > [arquivo]`** - Copia o conteúdo do arquivo para outro.
- [X] **`cat [arquivo] >> [arquivo]`** - Adiciona o conteúdo do arquivo para outro.

## Comando bc

- [X] **`bc`** - Abre uma calculadora do Bash

**Observação**: Para sair bastas digitar 'quit' e dar enter.

## Processos

- [X] **`top`** - Exibe os processos usando a maioria dos recursos do sistema, a qualquer momento. "Q" pode ser usado para sair.
- [X] **`htop`** - O comando HTOP é uma evolução do comando TOP. As informações são semelhantes às produzidas pelo comando TOP, mas apresentadas num interface mais intuitivo e colorido.
- [X] **`kill pid`** - Mata o processo com o id de processo pid.
- [X] **`killall Discord`** - Mata todos os processo com o nome discord.
- [X] **`pkill fire`** - Mata todos os processo que tenha "fire" em seu nome.
- [X] **`ps [opções]`**
- [X] **`ps`** - O comando ps exibe informações sobre os processos que estão executando na máquina.
- [X] **`ps -a`** - Mostra os processos de todos os usuários.
- [X] **`ps -A`** ou **`ps -e`** - Mostra todos os processos.
- [X] **`ps -f`** - Mostra a árvore de execução de comandos.
- [X] **`ps -g [grupo]`** - Mostra os processos de um determinado grupo.
- [X] **`ps -x`** - Mostra os processos que não foram iniciados no console.
- [X] **`ps -u`** - Fornece o nome do usuário e a hora de início do processo.
- [X] **`ps -aux`** - exibe todos os processos do sistema independente de terminal.

## Informações do sistema

- [X] **`whereis [programa]`** - Exibe possíveis localizações de um determinado programa.
- [X] **`date`** - Exibe a data e hora atual.
- [X] **`whoami`** - Imprime o nome de usuário usado no momento em que foi digitado.
- [X] **`sudo su`** - Entra no modo usuário root.
- [X] **`exit`** - Sai do usuário logado no momento que o comando é executado.

**Observação**: Quando você for digitar sua senha para entrar no modo usuário root, por questões de segurança o terminal não exibe nada na tela o que foi digitado.

- [X] **`uname [opções]`**
- [X] **`uname -a ou uname`** --all imprime todas as informações, omitindo uname -p e uname -i se as informações forem desconhecidas.
- [X] **`uname -s ou uname`** --kernel-name - Imprime o nome do kernel.
- [X] **`uname -n ou uname`** --nodename - Imprime o nome do host do nó da rede.
- [X] **`uname -r ou uname`** --kernel-release - Imprime a versão do kernel.
- [X] **`uname -v ou uname`** --kernel-version - Imprime a versão do kernel.
- [X] **`uname -m ou uname`** --machine - Imprime o nome do hardware da máquina.
- [X] **`uname -p ou uname`** --processor - Imprime o tipo de processador ou ” desconhecido “.
- [X] **`uname -i ou uname`** --hardware-platform - Imprime a plataforma de hardware, ou ” desconhecido “.
- [X] **`uname -o ou uname`** --operating-system - Imprime o sistema operacional.
- [X] **`uname --version`** - Exibe informações da versão.

## Memória

- [X] **`free`** - Este comando exibe a quantidade de espaço livre disponível no sistema.
- [X] **`df [opções]`**
- [X] **`df`** - Exibe informações sobre o uso do espaço em disco de todos os sistemas de arquivos montados.
- [X] **`df -a`** - Inclui sistema de arquivos com 0 (zero) blocos.
- [X] **`df -h`** - Mostra o espaço livre/ocupado em MB, KB, GB em vez de bloco.
- [X] **`df -k`** - Lista em Kbyts.
- [X] **`df -l`** - Somente lista sistema de arquivos locais.
- [X] **`df -m`** - Lista em Mbytes.
- [X] **`df -T`** - Lista o tipo de sistema de arquivos de cada partição.

## Comando apt

- [X] **`sudo apt-get update`** - Baixa os pacotes disponíveis.
- [X] **`sudo apt-get upgrade`** - Atualiza os pacotes do sistema.
- [X] **`sudo apt-get clean`** - Remove cache de programas.
- [X] **`sudo apt-get cache [busca]`** - Busca um programa.
- [X] **`sudo apt-get install [programa]`** - Instala um programa.
- [X] **`sudo apt-get remove [pacote] --purge`** - Remove programas e configs.

**Observação**: Se você estiver logado como usuário root, não é necessário o uso do 'sudo' na frente dos comandos.

## Compressão de arquivos

- [X] **`tar cf pacote.tar arqs`** - Cria um pacote TAR (nomeado pacote.tar) com os arquivos especificados (substituir a variável arqs pelo nome do arquivo).
- [X] **`tar xf pacote.tar`** - Extrai os arquivos de “pacote.tar” (substituir a variável pacote.tar pelo nome do arquivo).
- [X] **`tar czf pacote.tar.gz arqs`** - Cria um pacote TAR (nomeado pacote.tar.gz) com compressão GZip.
- [X] **`tar xzf pacote.tar.gz`** - Extrai um pacote TAR (nomeado pacote.tar.gz) com compressão GZip.
- [X] **`tar cjf pacote.tar.bz2`** - Cria um pacote TAR (nomeado pacote.tar.bz2) com compressão BZip2.
- [X] **`tar xjf pacote.tar.bz2`** - Extrai um pacote TAR (nomeado pacote.tar.gz) com compressão BZip2.
- [X] **`gzip arq`** - Compacta um arquivo e o renomeia para arq.gz (substituir a variável arq pelo nome do arquivo).
- [X] **`gzip -d arq.gz`** - Descompacta arq.gz para um arquivo (substituir a variável arq.gz pelo nome do arquivo).

## Histórico de comandos

- [X] **`history`** - Lista o histórico de 2000 comandos digitados.
- [X] **`Seta para cima e seta para baixo`** - Últimos comandos digitados.
- [X] **`!!`** - Repete o último comando.

## Referência global

Referências globais são recursos para especificar um ou mais arquivos ou diretórios de uma vez. Vamos usar o comando 'ls' para os exemplos, mas pode ser usado qualquer outro comando.

- [X] **`ls /etc/*.conf`** - Lista todos os arquivos que tem a extenção '.conf'.
- [X] **`ls /etc/*x*`** - Lista todos os aquivos que em algum lugar do nome tem a lera 'x'.
- [X] **`ls /etc/f*`** - Lista todos os aquivos que começa com a letra 'f'.
- [X] **`ls /etc/?as*`** - Lista todos os arquivos que começa com uma letra qualquer, tem segundo caractere 'a', o terceiro 's' e qualquer caractere depois.
- [X] **`ls /etc/???a*`** - Lista todos os arquivos que tem o quarto caractere 'a'.
- [X] **`ls /etc/f[a-t]*`** - Lista todos os aqruivos que começa com a letra 'f', depois a segunda letra varia do 'a' ao 't' e depois qualquer caractere.
- [X] **`ls /etc/f[u,o]*`** - Lista todos os aqruivos que começa com a letra 'f', depois a segunda letra é 'u' ou 'o' e depois qualquer caractere.
- [X] **`ls /etc/?[a,e,i,o,u]*`** - Lista todos os aqruivos que começa com uma letra qualquer, depois a segunda letra é uma vogal e depois qualquer caractere.
- [X] **`ls /etc/?[a,e,i,o,u]???`** - Lista todos os aqruivos que começa com uma letra qualquer, depois a segunda letra é uma vogal e depois tem mais 3 caracteres qualquer.
- [X] **`ls /etc/?{am,ul}*`** - Lista todos os aqruivos que começa com uma letra qualquer, depois a segunda e a terceira letra é 'am' ou 'ul' e depois qualquer caractere.
- [X] **`ls /etc/*{ev,ux}`** - Lista todos os aqruivos que termina com 'ev' ou 'ux'.
- [X] **`ls /etc/*.{conf,db}`** - Lista todos os aqruivos que tem a extenção '.conf' ou '.db'.

## Comando find

O comando find é usado para busca de arquivos.

- [X] **`find .`** - Lista todos os arquivos contidos em um diretório e subdiretórios.
- [X] **`find . -name [arquivo]`** - Busca um arquivo com um nome especifico.
- [X] **`find [diretório] -iname [arquivo]`** - Procura ignorando case sensitive.

## Usuários

## Comando passwd

O passwd é um comando utilizado para configurar ou trocar a senha das contas dos usuários do sistema. É necessário possuir privilégios administrativos para executá-lo, mas um usuário comum consegue alterar sua própria senha.

- [X] **`passwd [opções] [usuários]`**
- [X] **`passwd -l`** - Trava a senha do usuário, ficando impedido de se logar e não pode trocar a senha (não é desabilitado).
- [X] **`passwd -u`** - Destrava a senha do usuário.
- [X] **`passwd -d`** - Exclui a senha do usuário.
- [X] **`passwd -e`** - Expira a senha do usuário, forçando-o a fornecer uma nova ao logar-se novamente.
- [X] **`passwd -x dias`** - Expira a senha do usuário quando atingir o número de dias especificados.
- [X] **`passwd -n dias`** - Define a quantidade mínima de dias que o usuário deverá esperar para trocar a senha.
- [X] **`passwd -w dias`** - define a quantidade mínima de dias que o usuário receberá o aviso que a senha precisa ser alterada.
- [X] **`passwd -i`** - Deixa o usuário inativo, caso a senha tenha expirado.
- [X] **`passwd -S`** - Exibe o status da conta.
- [X] **`passwd -a`** - Usada em conjunto com a opção -S mostra o status das contas de todos os usuários.

## Tipos de usuários

## Usuários comuns

São os usuários que podem se conectar no sistema. Geralmente, estes usuários possuem uma home e podem manipular arquivos quando tem as permissões para tal. Porém estes usuários geralmente não tem permissão para certos arquivos e diretórios na maquina e não podem executar muitas funções a nível de sistema.

Exemplo de um usuário comum: **`roger@AB4NT5S:~$`**

## Usuários de sistema

Diferente dos usuários comuns, estes usuários não se conectam no sistema. São contas usadas para tarefas específicas dentro do sistema que não são de propriedade de uma pessoa em particular.

## Root

O usuário root, também chamado de superusuário, tem controle total sobre o sistema operacional. Ele pode acessar todos os arquivos e normalmente é o único que pode executar certos programas, como por exemplo o httpd.

Exemplo de um usuário root: **`root@AB4NT5S:~#`**

**Observação**: Não é recomendado que você use o terminal no modo root o tempo inteiro.

## Grupos

Um grupo é um conjunto de um ou mais usuários. É interessante reunir vários usuários em um grupo para definir suas propriedades, como as permissões. Como o arquivo passwd nós temos um arquivo somente para armazenar detalhes sobre os grupos.
Esse arquivo esta localizado em: /etc/group.

## Gerenciamento de usuários

## Adicionar usuários

Criar um usuário novo no Linux é bem simples, apenas é necessário o comando useradd e indicar o nome do novo usuário.

- [X] **`useradd [opções] [nomeusuario]`**
- [X] **`useradd -d [nomeusuario]`** - Define o nome do diretório home do usuário (mas não o cria).
- [X] **`useradd -s [nomeusuario]`** - Define o shell padrão do usuário.
- [X] **`useradd -h [nomeusuario]`** - Exibe as opções do comando.

## Alterar usuários

Para alterarmos uma conta de usuário basta apenas utilizarmos o comando usermod.

- [X] **`usermod [opções] [nomeusuário]`**
- [X] **`usermod -d diretório [-m]`** - Cria uma nova home para o usuário. A opção -m move os arquivos da home atual do usuário para a nova.
- [X] **`usermod -e yyyy-mm-dd`** - Altera a data de expiração da conta do usuário.
- [X] **`usermod -g grupo`** - Altera o GID do grupo do usuário para o especificado.
- [X] **`usermod -G grupo[, grupo2, ...]`** - Define o GID dos outros grupos que o usuário pertence.
- [X] **`usermod -l nome`** - Altera o nome do usuário (ele não pode estar logado).
- [X] **`usermod -s shell`** - Altera o shell do usuário.
- [X] **`usermod -u uid`** - Altera o número de UID do usuário.

## Remover usuários

Para removermos um usuário utilizamos o comando userdel.

- [X] **`userdel [opções] [nomeusuario]`**
- [X] **`userdel -h [nomeusuario]`** - Exibe as opções do comando.
- [X] **`userdel -r [nomeusuario]`** - Deleta a home e todos os seus arquivos.

## vim

Eu escolhi o editor vim para este artigo, mas você pode usar vários editores além do vim como o nano e o vi por exemplo.

O vim (VI Improvement) é uma melhoria do antigo editor de texto vi. Este por sua vez é uma melhoria do editor de texto orientado a linha chamado ed. Existe também uma versão do vim para ambiente X chamada gvim.

O vim possui três formas de trabalho: modo de linha, modo de edição e modo de comandos. A mudança de um modo para outro modo é feita através do uso da tecla Esc.

Após o arquivo ser aberto pelo vim, o modo de comandos é ativado. No modo de comandos, as teclas digitadas pelo usuário são interpretadas pelo vim como ações a serem executadas dentro do arquivo aberto. No modo de edição, as teclas digitadas pelo usuário são ecoadas na tela. Para entrar neste modo, pode-se digitar, por exemplo, "a" (adicionar), "i" (incluir), etc. No modo de linha, o usuário define ações a serem executadas no arquivo como um todo (por exemplo, salvar, substituir caracteres, sair do aplicativo, etc). Para entrar neste modo, deve-se digitar " : ".

- [X] **`vim [opções] [arquivo]`**

São alguns dos comandos do vim no modo de comandos

- [X] **`0`** - Mover o cursor para o início da linha em que o cursor está posicionado.
- [X] **`a`** - Inserir texto após a posição atual do cursor.
- [X] **`A`** - Inserir texto no final da linha atual.
- [X] **`-b`** - Permite editar arquivo binário.
- [X] **`dd`** - Deletar linha atual.
- [X] **`[n]+dd`** - Deletar n linhas a partir da linha atual.
- [X] **`G`** - Ir para o fim do arquivo.
- [X] **`[n]+G`** - Ir para a n-ésima linha do arquivo.
- [X] **`h`** - Voltar um caractere.
- [X] **`H`** - Ir para a primeira linha exibida na tela atual.
- [X] **`i`** - Inserir texto a partir da posição atual do cursor.
- [X] **`I`** - Inserir texto no início da linha atual.
- [X] **`j`** - Descer uma linha.
- [X] **`J`** - Juntar a linha atual com a linha seguinte.
- [X] **`[n]+J`** - Juntar n linhas consecutivas a partir da linha atual.
- [X] **`k`** - Subir uma linha.
- [X] **`l`** - Avançar um caractere.
- [X] **`L`** - Ir para a última linha exibida na tela atual.
- [X] **`n`** - Procurar, a partir da posição atual do cursor, a próxima ocorrência do texto definido no último comando /.
- [X] **`N`** - Procurar, a partir da posição atual do cursor e indo em direção ao início do arquivo, a próxima ocorrência do texto definido no último comando /.
- [X] **`o`** - Inserir uma linha em branco após a linha atual.
- [X] **`O`** - Inserir uma linha em branco acima da linha atual.
- [X] **`p`** - Inserir linhas copiadas após a linha atual.
- [X] **`P`** - Inserir linhas copiadas antes da linha atual.
- [X] **`r`** - Substituir o caractere atual.
- [X] **`R`** - Substituir um conjunto de caracteres.
- [X] **`s`** - Deletar o caractere atual e inserir texto.
- [X] **`S`** - Apagar linha e inserir novo texto na linha.
- [X] **`u`** - Desfazer a última alteração feita no texto e ainda não desfeita.
- [X] **`U`** - Desfazer a última alteração feita no texto.
- [X] **`x`** - Apagar caractere onde o cursor está posicionado.
- [X] **`$`** - Mover o cursor para o fim da linha em que o cursor está posicionado.
- [X] **`[n]+y`** - Copiar n linhas a partir da linha atual.
- [X] **`yy`** - Copiar a linha atual.
- [X] **`[n]+Y`** - Copiar n linhas a partir da linha atual.
- [X] **`YY`** - Copiar a linha atual.
- [X] **`CTRL+B`** - Voltar uma página.
- [X] **`CTRL+F`** - Avançar uma página.
- [X] **`F1`** - Exibir tela de ajuda.
- [X] **`[n]+ENTER`** - Ir para n linhas abaixo da linha atual.
- [X] **`[n]+.`** - Repetir o último comando que alterou o texto n vezes a partir da posição atual do cursor.
- [X] **`[n]+~+ENTER`** - Inverter a caixa (case) dos n caracteres seguintes ao cursor.
- [X] **`/texto`** - Procurar pela primeira ocorrência do texto especificado a partir da posição atual do cursor.

São alguns dos comandos do vim no modo de linha

- [X] **`:r arquivo`** - Incluir arquivo a partir da linha atual do cursor.
- [X] **`:q+ENTER`** - Sair da tela de ajuda.
- [X] **`:q!`** - Sair do vim sem salvar as alterações.
- [X] **`:w arquivo`** - Salvar arquivo com o nome especificado.
- [X] **`:wq`** - Sair do vim salvando as alterações.
- [X] **`:X`** - Criptografa o arquivo.
- [X] **`:n`** - Ir para a linha "n". Exemplo: Para ir para linha 10 do arquivo, :1

Busca

- [X] **`/palavra`** - Procura por "palavra" do início para o fim.
- [X] **`?palavra`** - Procura por "palavra" do fim para o início.
- [X] **`/Mari[oa]`** - Procura por "Mario" ou "Maria".
- [X] **`/\< pal`** - Procura por expressões que começem com "pala" como, "palavra" ou "palíndromo".
- [X] **`/ismo\>`** - Procura por expressões que terminem com "ismo" como, "autismo".
- [X] **`/\< para\>`** - Procura pela palavra "para".
- [X] **`/\<...\>`** - Procura por todas as palavras com 3 letras.
- [X] **`/maria\|joao`** - Procura por maria ou joao.
- [X] **`/\<\d\d\d\d\>`** - Procura exatamente por 4 dígitos numéricos.
- [X] **`/^\n\{3}`** - Procura por três linhas em branco.
- [X] **`:bufdo /palavra/`** - Procura "palavra" em todos os arquivos abertos.

Substituição

- [X] **`:%s/antigo/novo/g`** - Substitui todas as ocorrências de "antigo" por "novo" no arquivo.
- [X] **`:%s/antigo/novo/gw`** - Substitui todas as ocorrências com confirmação.
- [X] **`:2,35s/antigo/novo/g`** - Substitui todas as ocorrências entre as linhas 2 e 35.
- [X] **`:5,$s/antigo/novo/g`** - Substitui todas as ocorrências da linha 5 até EOF (fim da linha).
- [X] **`:%s/^/legal/g`** - Substitui o começo de cada linha com "legal".
- [X] **`:%s/$/Oh/g`** - Substitui o fim de cada linha por "Oh".
- [X] **`:%s/antigo/novo/gi`** - Substitui "antigo" por "novo" desconsiderando maíusculas e/ou minúsculas.
- [X] **`:%s/ *$//g`** - Apaga todos os espaços em branco.
- [X] **`:g/palavra/d`** - Apaga todas as linhas contendo "palavra".
- [X] **`:v/palavra/d`** - Apaga todas as linhas que não contém "palavra".
- [X] **`:s/maria/joao/`** - Substitui a primeira ocorrência de "maria" por "joao" na linha corrente.
- [X] **`:s/maria/joao/g`** - Substitui todas as ocorrências de "maria" por "joao" na linha corrente.
- [X] **`:%s/maria/joao/g`** - Substitui "maria" por "joao" em todo o arquivo.
- [X] **`:%s/\r//g`** - Apaga retornos de carro do windows (\n).
- [X] **`:%s/\r/\r/g`** - Transforma os retornos de carro do windows (\n) em retornos do Linux (\r).
- [X] **`:%s#<[^>]\+>##g`** - Apaga tags HTML mas mantêm o texto.
- [X] **`:%s/^\(.*\)\n\1$/\1/`** - Apaga linhas repetidas.
- [X] **`Ctrl+a`** - Incrementa o número sob o cursor.
- [X] **`Ctrl+x`** - Decrementa o número sob o cursor.
- [X] **`ggVGg?`** - Muda o texto usando Rot13.

Minúsculo / Maiúsculo

- [X] **`Vu`** - Torna todos os caracteres da linha minúsculos.
- [X] **`VU`** - Torna todos os caracteres da linha maiúsculos.
- [X] **`g~~`** - Inverte os caracteres do texto inteiro.
- [X] **`vEU`** - Coloca as letras da palavra em maiúsculas.
- [X] **`vE~~`** - Inverte os caracteres da palavra selecionada.
- [X] **`ggguG`** - Coloca todo o texto em minúsculas.
- [X] **`:set ignorecase`** - Ignora minúsculos/maiúsculos nas buscas.
- [X] **`:set smartcase`** - Ignora minúsculos/maiúsculos em buscas exceto quando uma letra msiúscula é usada.
- [X] **`:%s/\<./\u&/g`** - Coloca a primeira letra de cada palavra em maiúscula.
- [X] **`:%s/\<./\l&/g`** - Coloca a primeira letra de cada palavra em minúscula.
- [X] **`:%s/.*/\u&`** - Coloca a primeira letra de cada linha em maiúscula.
- [X] **`:%s/.*/\l&`** - Coloca a primeira letra de cada linha em minúscula.

Lendo/Gravando arquivos

- [X] **`:1,10 w arquivo`** - Salva as linhas de 1 a 10 em "arquivo".
- [X] **`:1,10 w >> arquivo`** - Adiciona as linhas de 1 a 10 em "Arquivo".
- [X] **`:r arquivo`** - Insere o conteúdo de "arquivo" no atual.
- [X] **`:23r arquivo`** - Insere o conteúdo de "arquivo" a partir da linha 23.

Explorando arquivos

- [X] **`:e .`** - Abre o gerenciador de arquivos integrado do Vim.
- [X] **`:Sex`** - Divide a janela e abre o gerenciador de arquivos integrado.
- [X] **`:browse e`** - Abre o gerenciador de arquivos integrado na janela corrente.
- [X] **`:ls`** - Lista os buffers carregados.
- [X] **`:cd ..`** - Move para a pasta superior.
- [X] **`:args`** - Lista os arquivos.
- [X] **`:args *.php`** - Abre lista de arquivos.
- [X] **`:grep expressao *.php`** - retorna uma lista de arquivos .php que contenham a expressão informada.
- [X] **`gf`** - Abre o arquivo sob o cursor.

Interação com o Linux

- [X] **`:!pwd`** - Executa o comando "pwd" e retorna para o Vim.
- [X] **`!!pwd`** - Executa o comando "pwd" e insere a saída no buffer.
- [X] **`:sh`** - Retorna temporariamente para o shell.
- [X] **`exit`** - Retorna para o Vim.

Alinhamento

- [X] **`:%!fmt`** - Alinha todas as linhas.
- [X] **`!}fmt`** - Alinha todas as linhas a partir da posição corrente.
- [X] **`5!!fmt`** - Alinha as próximas 5 linhas.

Abas

- [X] **`:tabnew`** - Cria uma nova aba.
- [X] **`gt`** - Mostra a próxima aba.
- [X] **`:tabfirst`** - Mostra a primeira aba.
- [X] **`:tablast`** - Mostra a última aba.
- [X] **`:tabm n(posicao)`** - Reorganiza as abas.
- [X] **`:tabdo %s/foo/bar/g`** - Executa um comando em todas as abas.
- [X] **`:tab ball`** - Coloca todos os arquivos abertos em abas.

Divisão da janela do Vim

- [X] **`:e arquivo`** - Edita "arquivo" na janela corrente.
- [X] **`:split arquivo`** - Divide a janela e abre "arquivo".
- [X] **`ctrl-w "seta para cima"`** - Coloca o cursor na janela do topo.
- [X] **`ctrl-w ctrl-w`** - Coloca o cursor na próxima janela.
- [X] **`ctrl-w_`** - Maximiza a janela corrente.
- [X] **`ctrl-w=`** - Coloca todas as janelas com o mesmo tamanho.
- [X] **`10 ctrl-w+`** - Adiciona 10 linhas de tamanho na janela corrente.
- [X] **`:vsplit arquivo`** - Divide a janela verticalmente.
- [X] **`:sview arquivo`** - O mesmo que split, mas em modo somente-leitura.
- [X] **`:hide`** - Fecha a janela corrente.
- [X] **`:only`** - Fecha todas as janelas, exceto a janela atual.
- [X] **`:b 2`** - Abre #2 na janela corrente.

Auto-completion do texto

- [X] **`Ctrl+n Ctrl+p (em modo de inserção)`** - Completa palavra.
- [X] **`Ctrl+x Ctrl+l`** - Completa linha.
- [X] **`:set dictionary=dict`** - Define dict como o dicionário atual.
- [X] **`Ctrl+x Ctrl+k`** - Completa usando o dicionário.

Marcações

- [X] **`mk`** - Marca a posição corrente como k.
- [X] **`‘k`** - Move o cursor para a marca k.
- [X] **`d’k`** - Apaga tudo até a marca k.

Abreviações

- [X] **`:ab email me@me.com`** - Define email como abreviação de me@me.com.

Identação de Texto

- [X] **`:set autoindent`** - Liga a identação automática.
- [X] **`:set smartindent`** - Liga a identação inteligente.
- [X] **`:set shiftwidth=4`** - Define o tamanho da identação em 4 espaços.
- [X] **`ctrl-t, ctrl-d`** - Identa/Deidenta no modo de inserção.
- [X] **`>>`** - Identa.
- [X] **`<<`** - Deidenta.

Marcação de sintaxe

- [X] **`:syntax on`** - Liga a marcação de sintaxe.
- [X] **`:syntax off`** - Desliga a marcação de sintaxe.
- [X] **`:set syntax=perl`** - Força a usar a marcação de sintaxe do perl.

## Git

## Comandos

- [X] **`git init`** - Cria um repositório Git vazio ou reinicialize um existente.

- [X] **`git status`** - Informa o estado das alterações do nosso projeto.

- [X] **`git add [file]`** - Adiciona ou atualiza mudanças para irem para o repositório.
  - [X] **`git add .`** - Você pode adicionar todos os arquivo usando o " . ".

- [X] **`git commit -m "message"`** - Registra alterações no repositório.
  - [X] **`git commit -am "message"`** - Atualiza o repositório e registra alterações no repositório ao mesmo tempo.

- [X] **`git log`** - Mostra os pontos na "linha do tempo" do repositório ( commit ).
  - [X] **`git log --oneline`** - Mostra os pontos na "linha do tempo" de forma mais resumida.
  - [X] **`git log --abbrev-commit`** - Ao vez de mostrar o hash com 40 caracteres, mostra apenas com 7 caracteres.
  - [X] **`git log --pretty=oneline`** - Faz com que caiba tudo em uma linha.
  - [X] **`git log --graph`** - Desenha uma representação gráfica dos commits no lado esquerdo da saída.

- [X] **`git diff`** - Mostra o que foi alterado em um arquivo, de vermelho o que foi excluído, de verde o que foi adicionando. Use o "git diff" antes de dar o "git add".

- [X] **`git show`** - Apresenta o último ponto na "história" do nosso projeto.
  - [X] **`git show [hash]`** - Apresenta determinado ponto na "história" do nosso projeto.

- [X] **`git branch`** - Lista, cria ou exclui ramificações.
  - [X] **`git branch -d [ramificação]`** - Exclui ramificações.

- [X] **`git checkout [hash]`** - Alterna ramificações ou restaura arquivos da árvore de trabalho.
  - [X] **`git checkout [arquivo_modificado]`** - Descarta as mudanças feitas no arquivo. Use antes de dar o "git add".
  - [X] **`git checkout -b [minha-feature]`** - Cria uma nova ramificação no nosso projeto.
  - [X] **`git checkout master`** - Vai para a ramificação master.
  - [X] **`git checkout [minha_ramificação]`** - Vai para a ramificação criada pelo desenvolvedor.

- [X] **`git reset HEAD`** - Remove um arquivo adicionado pelo "git add". Usar depois do "git add" e antes do "git commit".
  - [X] **`git reset --hard [hash]`** - Remove um commit.

- [X] **`git merge [minha_ramificação]`** - Faz a fusão de uma ramificação x com a ramificação master. Para fazer a fusão você tem que estar na ramificação master.

- [X] **`git remote`** - Verifica se existe um repositório remoto.

- [X] **`git push`** - Envia alterações locais para o repositório remoto.

- [X] **`git clone [link_repositório]`** - Clonar um projeto / repositório.

- [X] **`git pull`** - Puxa do repositório remoto.

## Padronização de commits ( Opcional )

Para poder padronizar seus commits, você vai precisar de duas ferramentas, o [commitlint](https://github.com/conventional-changelog/commitlint) e o [commitizen](https://github.com/commitizen/cz-cli), você pode instalar essas dependências usando o npm ou o yarn.

**Formato da mensagem**: Cada mensagem de commit consiste em um **cabeçalho**, um **corpo** e um **rodapé**.

**Cabeçalho**: O cabeçalho é obrigatório. Tem um formato pré-definido, que inclui um **tipo** e um **título**:

```
<tipo>(<escopo opcional>): <título>

<corpo opcional>

<rodapé opcional>
```

**Exemplos:**

```
fix(integracao-erp): xxxxxxx

improve(app-toolbox): xxxxxxx

docs: Instruções de iniciar projeto com docker
```

Qualquer linha da mensagem do commit não pode ter mais de 100 caracteres! Assim fica mais fácil para ler no GitHub, Gitlab e outras ferramentas de git.

**Tipos**: Deve ser um dos seguintes:

* **build**: Alterações que afetam o sistema de build ou dependências externas.
* **static**: Alterações no conteúdo de arquivos estáticos (dados .json, imagens, etc).
* **ci**: Alterações em nossos arquivos e scripts de configuração de CI.
* **cd**: Alterações em nossos arquivos e scripts de configuração para CD.
* **docs**: Somente alterações na documentação.
* **feat**: Um novo recurso.
* **fix**: Uma correção de bug da aplicação.
* **perf**: Uma alteração de código que melhora o desempenho.
* **refactor**: Uma alteração de código que não corrige um bug nem adiciona um recurso.
* **improve**: Alguma alteração de código que melhore o comportamento de um recurso.
* **style**: Alterações que não afetam o significado do código (espaço em branco, formatação, ponto e vírgula, etc).
* **test**: Adicionando testes ausentes ou corrigindo testes existentes.
* **revert**: Reverter para um commit anterior.

**Emojis**: Emojis para o título do `commit`:

| Commit type            | Emoji                                           |
| :--------------------- | :---------------------------------------------- |
| Initial commit         | :tada: `:tada:`                                 |
| Version tag            | :bookmark: `:bookmark:`                         |
| New feature            | :sparkles: `:sparkles:`                         |
| Bugfix                 | :bug: `:bug:`                                   |
| Docker                 | :whale: `:whale:`                               |
| Fix names              | :pencil: `:pencil:`                             |
| Fix for iOS            | :apple: `:apple:`                               |
| Fix for Android        | :robot: `:robot:`                               |
| Security Fix           | :lock: `:lock:`                                 |
| Metadata               | :card_index: `:card_index:`                     |
| Refactoring            | :recycle: `:recycle:`                           |
| Documentation          | :books: `:books:`                               |
| Internationalization   | :globe_with_meridians: `:globe_with_meridians:` |
| Accessibility          | :wheelchair: `:wheelchair:`                     |
| Performance            | :racehorse: `:racehorse:`                       |
| Cosmetic               | :art: `:art:`                                   |
| Tooling                | :wrench: `:wrench:`                             |
| Tests                  | :rotating_light: `:rotating_light:`             |
| Deprecation            | :poop: `:poop:`                                 |
| Removal                | :wastebasket: `:wastebasket:`                   |
| Work In Progress (WIP) | :construction: `:construction:`                 |
| Additional comments    | :speech_balloon: `:speech_balloon:`             |

**Título**: O título contém uma descrição sucinta da mudança:

* use o imperativo, tempo presente: "mudança" não "mudou" nem "muda".
* não capitalize a primeira letra.
* sem ponto (.) no final.

❌ RUIM: `git commit -m "add user.js"`

✅ BOM: `git commit -m "♻️ - Migration created to person"`

**Corpo**: Um corpo de mensagem de commit mais longo PODE ser fornecido após o título, fornecendo informações contextuais adicionais sobre as alterações no código. Configure a mensagem com um wrap de 80 caracteres. Use para explicar "o que" e "porque" foi realizado essa modificação, ao invez de "como". O corpo DEVE começar depois de uma linha em branco após a descrição.

**Rodapé**: Um rodapé PODE ser fornecido depois de uma linha em branco após o corpo. Caso exista um ticket no jira, criar um referência assim: `issue TP-666` ou `closes issue TP-666`.

**Reverter um commit**: Se o commit reverte um commit anterior, ele deve começar por `revert:`, seguido pelo cabeçalho do commit revertido. No corpo, ele deve dizer: `Isso reverte o commit <hash> .`, onde o hash é o SHA do commit sendo revertido.

### Por quê?

* Criação automatizada de CHANGELOGs;
* Determinar automaticamente um aumento de versionamento semântico (com base nos tipos de commits);
* Comunicar a natureza das mudanças para colegas de equipe, o público e outras partes interessadas de forma padronizada
* Disparar processos de build e deploy;
* Facilitar a contribuição de outras pessoas em seus projetos, permitindo que eles explorem um histórico de commits mais estruturado e com melhor rastreabilidade.

### Alias ( Opcional )
Você pode criar alias para os comandos do git, basta ir no arquivo ".gitconfig" e definir seus alias.
No uninx ( Linux e Mac ) o arquivo ".gitconfig" fica localizado em: /home/seuusuário/.gitconfig

Alias que eu gosto de usar:

```
[alias]
  i = init
  a = add
  b = branch
  ci = commit
  co = checkout
  cm = checkout master
  cb = checkout -b
  st = status -sb
  sf = show --name-only
  pom = push origin master -u
  ps = push
  lg = log --pretty=format:'%Cred%h%Creset %C(bold)%cr%Creset %Cgreen<%an>%Creset %s' --max-count=30
  incoming = !(git fetch --quiet && git log --pretty=format:'%C(yellow)%h %C(white)- %C(red)%an %C(white)- %C(cyan)%d%Creset %s %C(white)- %ar%Creset' ..@{u})
  outgoing = !(git fetch --quiet && git log --pretty=format:'%C(yellow)%h %C(white)- %C(red)%an %C(white)- %C(cyan)%d%Creset %s %C(white)- %ar%Creset' @{u}..)
  unstage = reset HEAD --
  undo = checkout --
  rollback = reset --soft HEAD~1
```

## :thinking: Como contribuir

- Faça um fork desse repositório;
- Cria uma branch com a sua feature: **`git checkout -b minha-feature`**;
- Faça commit das suas alterações: **`git commit -m 'feat: Minha nova feature'`**;
- Faça push para a sua branch: **`git push origin minha-feature`**.

Depois que o merge da sua pull request for feito, você pode deletar a sua branch.

## :memo: Licença

Esse projeto está sob a licença MIT. Você pode clonar e redistrubir o conteúdo do repositório livrimente.
Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.
