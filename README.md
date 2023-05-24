<h1 align="center">
  Bash (Ubuntu)
</h1>

<p align="center">
  <img alt="badge" src="https://img.shields.io/badge/author-RogerFernando-191F2B?style=flat-square">
  <img alt="badge" src="https://img.shields.io/github/stars/abantes/bash-for-developers?color=191F2B&style=flat-square">
  <img alt="badge" src="https://img.shields.io/badge/license-MIT-191F2B?style=flat-square">
  <img alt="badge" src="https://img.shields.io/github/contributors/abantes/bash-for-developers?color=191F2B&style=flat-square">
</p>

# Roadmap

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

* [Git](#Git)
  * [Configurando o git](#configurando-o-git)
  * [Comandos](#comandos)
  * [Criando boas mensagens de commits](#criando-boas-mensagens-de-commits)
  * [Alias](#alias)

* [Vim](#vim)

* [Referências](#referências)

# Básico antes dos comandos

## Atalhos globais do Bash

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

## Diretórios

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

## Ajuda no terminal

Você pode consultar a documentação e o manual de uso dos comandos das seguintes maneiras:

* `[comando] --help`: Documentação do comando.
* `man [comando]`: Manual do comando.
* `info [comando]`: Semelhante ao man, mas geralmente fornece informações mais detalhadas.

## Histórico de comandos

* `!!`: Repete o último comando.
* `history`: Lista o histórico de 2000 comandos digitados.
* `Seta para cima e seta para baixo`: Últimos comandos digitados.

# Manipulando arquivos

## Listagem de arquivos

`ls [opções]`: Podemos listar o conteúdo de um diretório utilizando o comando ls.

* `-a`: Lista todos os arquivos e diretórios ocultos.
* `-l`: Formato longo, mostra permissões, número de links, propietário, grupo, tamanho, data de modificação e nome do arquivo.
* `-h`: Lista arquivos e diretórios com informações formatadas (Tem que ser usado com o -l).
* `-R`: Lista os arquivos e pastas recursivamente.
* `-p`: Mostra uma barra (/) na frente de nomes de diretórios.

[Ver exemplo](examples/listagem-de-arquivos.md)

## Entrando e saíndo de diretórios

`cd`: Podemos entrar e sair de um diretório utilizando o comando cd.

* `cd [destino]`: Parte do local corrente até o diretório passado como referência.
* `cd /[destino]`: Partindo da raiz até o último diretório passado como referência.
* `cd ..`: Volta um diretório.
* `cd /`: Vai direto para o diretório raiz.
* `cd ~`: Vai direto para o diretório home.
* `cd -`: Nos retorna para o último diretório acessado.

[Ver exemplo](examples/entrando-e-saindo-de-diretorios.md)

## Exibindo o diretório atual

`pwd`: Exibe o caminho de diretório atual.

[Ver exemplo](examples/exibindo-o-diretorio-atual.md)

## Exibindo o tamanho de um diretório

`du [diretório]`: Exibe o tamanho de um diretório e todos os seus subdiretórios.

[Ver exemplo](examples/exibindo-o-tamanho-de-um-diretorio.md)

## Criando diretórios

`mkdir [nome-do-diretorio]`: Podemos criar diretórios utilizando o comando mkdir.

* `mkdir pasta1 pasta2 pasta3`: Cria três pastas, pasta1, pasta2 e pasta3.
* `mkdir -p A/B/C`: Cria a pasta A, dentro da pasta A cria a pasta B e dentro da pasta B cria a pasta C.

[Ver exemplo](examples/criando-diretorios.md)

## Criando arquivos

`touch [opções] [arquivo]`: Podemos criar arquivos utilizando o comando touch.

* `-a`: Altera a hora de acesso do arquivo.
* `-m`: Altera a hora de modificação do arquivo.
* `-am`: Altera a hora de acesso e modificação do arquivo.
* `-c`: Altera a hora de acesso sem criar um novo arquivo.

__Observação__: podemos gerar nomes automáticos usando as chaves `{}`, desta maneira: `touch exemplo{1..3}.txt`, este comando irá criar 3 arquivos chamados exemplo1.txt, exemplo2.txt e exemplo3.txt.

[Ver exemplo](examples/criando-arquivos.md)

## Excluíndo diretórios e arquivos

`rm [opções] [arquivo]`: Podemos excluir arquivos utilizando o comando rm.

* `-f`: Exclui arquivos forçadamente.
* `-r`: Exclui o diretório e os arquivos na direção recursiva.
* `-d`: Remove somente diretórios vazios.
* `-i`: Pergunta se queremos remover o arquivo/diretório antes de excluir.

[Ver exemplo](examples/excluindo-diretorios-e-arquivos.md)

## Copiando diretórios e arquivos

`cp [opções] [arquivo] [destino]`: Podemos copiar arquivos utilizando o comando cp.

* `-r`: Copia diretórios de forma recursiva.
* `-p`: Preserva as permissões originais do arquivo (proprietário, grupo, etc.).
* `-i`: Pergunta se desejamos sobrescrever um arquivo destino já existente.
* `-n`: Não sobrescreve um arquivo já existente.

[Ver exemplo](examples/copiando-diretorios-e-arquivos.md)

## Movendo e renomeando arquivos e pastas

`mv [opções] [arquivo] [destino]`: Podemos mover arquivos com o comando mv.

* `-b`: Cria um backup de cada arquivo destino existente.
* `-f`: Apaga destinos existente sem perguntar ao usuário.
* `-i`: Pergunta se desejamos sobrescrever o arquivo destino já existente.
* `-n`: Não sobrescrever um arquivo destino já existente.

O comando mv também é usado para renomear arquivos.

* `mv [nome_atual.extenção] [novo_nome.extenção]`

[Ver exemplo](examples/movendo-e-renomeando-arquivos-e-pastas.md)

## Visualização de arquivos

`more [arquivo]`: Mostra o conteúdo de um arquivo em partes.

`less [arquivo]`: Exibi o conteúdo de um arquivo páginado.

`tac [arquivo]`: Exibi o conteúdo de um arquivo de trás pra frente (da última linha pra primeira).

`cat [opções] [arquivo]`: Abre o arquivo em modo de visualização.
  
* `-n`: Mostra a quantidade de linas do arquivo.
* `-v`: Exibe caracteres não exibíveis.
* `-T`: Exibe tabulação mostradas como ^I.
* `-s`: Remove linhas repetidas em branco.
* `-b`: Numera as linhas que possuem algum conteúdo.

Busca e manilupalção de conteúdo:

* `cat [arquivo] | grep [busca]`: Busca no arquivo (case sensitive).
* `cat [arquivo] | grep [busca] -i`: Busca no arquivo (case insensitive).
* `cat [arquivo] > [arquivo]`: Copia o conteúdo do arquivo para outro.
* `cat [arquivo] >> [arquivo]`: Adiciona o conteúdo do arquivo para outro.

[Ver exemplo](examples/visualizacao-de-arquivos.md)

## Compressão de arquivos

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

`ps [opções]`: O comando ps exibe informações sobre os processos que estão executando na máquina.

* `-a`: Mostra os processos de todos os usuários.
* `-A` ou `-e`: Mostra todos os processos.
* `-f`: Mostra a árvore de execução de comandos.
* `-g [grupo]`: Mostra os processos de um determinado grupo.
* `-x`: Mostra os processos que não foram iniciados no console.
* `-u`: Fornece o nome do usuário e a hora de início do processo.
* `-aux`: exibe todos os processos do sistema independente de terminal.

[Ver exemplo](examples/processos.md)

## Informações do sistema

* `whereis [programa]`: Exibe possíveis localizações de um determinado programa.
* `date`: Exibe a data e hora atual.
* `whoami`: Imprime o nome de usuário usado no momento em que foi digitado.
* `sudo su`: Entra no modo usuário root.
* `exit`: Sai do usuário logado no momento que o comando é executado.

`uname [opções]`: Mostra informações sobre o sistema operacional.

* `-a`: imprime todas as informações, omitindo uname -p e uname -i se as informações forem desconhecidas.
* `-s`: Imprime o nome do kernel.
* `-n`: Imprime o nome do host do nó da rede.
* `-r`: Imprime a versão do kernel.
* `-v`: Imprime a versão do kernel.
* `-m`: Imprime o nome do hardware da máquina.
* `-p`: Imprime o tipo de processador ou " desconhecido ".
* `-i`: Imprime a plataforma de hardware, ou " desconhecido ".
* `-o`: Imprime o sistema operacional.
* `--version`: Exibe informações da versão.

[Ver exemplo](examples/informacoes-do-sistema.md)

## Memória

* `free`: Este comando exibe a quantidade de espaço livre disponível no sistema.

`df [opções]`: Exibe informações sobre o uso do espaço em disco de todos os sistemas de arquivos montados.

* `-a`: Inclui sistema de arquivos com 0 (zero) blocos.
* `-h`: Mostra o espaço livre/ocupado em MB, KB, GB em vez de bloco.
* `-k`: Lista em Kbyts.
* `-l`: Somente lista sistema de arquivos locais.
* `-m`: Lista em Mbytes.
* `-T`: Lista o tipo de sistema de arquivos de cada partição.

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

`passwd [opções] [usuário]`: O passwd é um comando utilizado para configurar ou trocar a senha das contas dos usuários do sistema. É necessário possuir privilégios administrativos para executá-lo, mas um usuário comum consegue alterar sua própria senha.

* `-l`: Trava a senha do usuário, ficando impedido de se logar e não pode trocar a senha (não é desabilitado).
* `-u`: Destrava a senha do usuário.
* `-d`: Exclui a senha do usuário.
* `-e`: Expira a senha do usuário, forçando-o a fornecer uma nova ao logar-se novamente.
* `-x dias`: Expira a senha do usuário quando atingir o número de dias especificados.
* `-n dias`: Define a quantidade mínima de dias que o usuário deverá esperar para trocar a senha.
* `-w dias`: define a quantidade mínima de dias que o usuário receberá o aviso que a senha precisa ser alterada.
* `-i`: Deixa o usuário inativo, caso a senha tenha expirado.
* `-S`: Exibe o status da conta.
* `-a`: Usada em conjunto com a opção -S mostra o status das contas de todos os usuários.

### Adicionar usuários

Criar um usuário novo no Linux é bem simples, apenas é necessário o comando useradd e indicar o nome do novo usuário.

`useradd [opções] [nomeusuario]`: Cria um novo usuário.

* `-d`: Define o nome do diretório home do usuário (mas não o cria).
* `-s`: Define o shell padrão do usuário.
* `-h`: Exibe as opções do comando.

### Alterar usuários

Para alterarmos uma conta de usuário basta apenas utilizarmos o comando usermod.

`usermod [opções] [nomeusuário]`: Altera um usário.

* `-d diretório [-m]`: Cria uma nova home para o usuário. A opção -m move os arquivos da home atual do usuário para a nova.
* `-e yyyy-mm-dd`: Altera a data de expiração da conta do usuário.
* `-g grupo`: Altera o GID do grupo do usuário para o especificado.
* `-G grupo[, grupo2, ...]`: Define o GID dos outros grupos que o usuário pertence.
* `-l nome`: Altera o nome do usuário (ele não pode estar logado).
* `-s shell`: Altera o shell do usuário.
* `-u uid`: Altera o número de UID do usuário.

### Remover usuários

Para removermos um usuário utilizamos o comando userdel.

`userdel [opções] [nomeusuario]`: Remove um usuário.

* `userdel -h [nomeusuario]`: Exibe as opções do comando.
* `userdel -r [nomeusuario]`: Deleta a home e todos os seus arquivos.

## Calculadora

* `bc`: Abre uma calculadora do Bash

__Observação__: Para sair bastas digitar 'quit' e apertar enter ou 'Ctrl+d'.

[Ver exemplo](examples/calculadora.md)

# Git

## Configurando o git

1. Instalção: https://git-scm.com/downloads
2. Documentação: https://git-scm.com/docs

Antes de começar a usar o Git é importante que você tenha ele configurado corretamente em sua máquina:

* `git config --global user.name "Fulano de Tal"`: Nome, coloque o mesmo nome do github;
* `git config --global user.email fulanodetal@exemplo.br`: Email, coloque o mesmo email do github;
* `git config --global core.editor vim`: Editor, aqui você pode escolher o editor padrão do git;
* `git config --list`: Use para ver o resultado das suas confirugarções.

## Comandos

### Básico

* `git init`: Cria um repositório git vazio.

* `git status`: Informa o estado das alterações do nosso projeto.

* `git add [arquivo]`: Adiciona novos arquivos ou atualiza mudanças para irem para o nosso repositório.
  * `git add .`: Você pode adicionar todos os arquivo usando o "." (ponto).

* `git commit -m "message"`: Registra alterações no repositório.
  * `git commit --amend -m "New message"`: Troca a mensagem feita no último commit.

* `git log`: Mostra os pontos na "linha do tempo" do repositório (commits).
  * `git log --oneline`: Mostra os pontos da "linha do tempo" de forma resumida.
  * `git log --abbrev-commit`: Mostra o _hash_ dos commits com 7 caracteres.
  * `git log --graph`: Desenha uma representação gráfica dos commits no lado esquerdo da saída do terminal.
  * `git log --grep="palavra"`: Busca por commits que tenha uma palavra ou parte de uma especificada.

* `git diff`: Mostra o que foi alterado em um arquivo, de vermelho o que foi excluído, de verde o que foi adicionando. Use-o antes do `git add`.

* `git show`: Apresenta o último ponto na "história" do nosso projeto.
  * `git show [hash]`: Apresenta determinado ponto na "história" do nosso projeto.

* `git remote`: Verifica se existe um repositório remoto.

* `git push`: Envia alterações locais para o repositório remoto.

* `git clone [link-do-repositório]`: Clona um repositório (Github por exemplo).

* `git pull`: Puxa as alterações feitas no repositório remoto (Github por exemplo).

### Avançado

* `git reset [arquivo]`: Remove um arquivo adicionado com o `git add`, use antes do `git commit`.
  * `git reset --hard [hash]`: Reverte um commit. Vai para um determinado ponto da "história" do projeto.

* `git branch`: Lista ramificações do nosso repositório.
  * `git branch -d [ramificação]`: Exclui uma ramificação do nosso repositório.

* `git checkout [hash]`: Restaura arquivos da árvore de trabalho.
  * `git checkout -b [minha-ramificação]`: Cria uma nova ramificação no nosso projeto.
  * `git checkout [minha-ramificação]`: Vai para a ramificação criada pelo desenvolvedor.

* `git merge [branch]`: Faz a fusão de uma branch X com uma branch Y.

* `git mv [arquivo] [diretório]`: Move um arquivo para um diretório especificado.
* `git mv [nome-original] [novo-nome]`: Renomea um arquivo.

* `git rm -f [file]`: Exclúi um arquivo do nosso repositório forçadamente.

* `git clean -f`: Remove arquivos não rastreados forçadamente.

## Criando boas mensagens de commits

Cada mensagem tem um formato pré-definido, que inclui um `tipo` e um `título`:

```
git commit -m "[type]: [message]"
```

Evite escrever mensagens do commit com mais de 100 caracteres, assim fica mais fácil para ler no GitHub, Gitlab e outras ferramentas.

Tipos:

* `build`: Alterações que afetam o sistema de build ou dependências externas.
* `static`: Alterações no conteúdo de arquivos estáticos (dados .json, imagens, etc).
* `ci`: Alterações em nossos arquivos e scripts de configuração de CI.
* `cd`: Alterações em nossos arquivos e scripts de configuração para CD.
* `docs`: Somente alterações na documentação.
* `feat`: Um novo recurso.
* `fix`: Uma correção de bug da aplicação.
* `perf`: Uma alteração de código que melhora o desempenho.
* `refactor`: Uma alteração de código que não corrige um bug nem adiciona um recurso.
* `improve`: Alguma alteração de código que melhore o comportamento de um recurso.
* `style`: Alterações que não afetam o significado do código (espaço em branco, formatação, ponto e vírgula, etc).
* `test`: Adicionando testes ausentes ou corrigindo testes existentes.
* `revert`: Reverter para um commit anterior.

Título:

O título contém uma descrição sucinta da mudança:

* Use o imperativo, tempo presente: "mudança" não "mudou" nem "muda".
* Não capitalize a primeira letra.
* Sem ponto (.) no final.

```
git commit -m "fix: fix typo in introduction to user guide"
```

## Alias

Você pode criar alias para os comandos do git, basta ir no arquivo ".gitconfig" e definir seus alias.
No Linux o arquivo ".gitconfig" fica localizado em: /home/seuusuário/.gitconfig

```
[alias]
  cl = clone
  it = init
  ad = add
  bn = branch
  ci = commit -m
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

# Vim

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

Meu setup atual no vim, fique a vontade para usar e melhorar:

```.vimrc
 """""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Maintainer:
"       Amir Salihefendic — @amix3k
"
" Awesome_version:
"       Get this config, nice color schemes and lots of plugins!
"
"       Install the awesome version from:
"
"           https://github.com/amix/vimrc
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

try
    colorscheme desert
catch
endtry

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

## Referências

confira os link's abaixos para saber mais:

* [Curso de Linux - Primeiros Passos](https://www.youtube.com/watch?v=6nN2EglOqCM&list=PLHz_AreHm4dlIXleu20uwPWFOSswqLYbV)
* [Curso de Linux Básico / Certificação LPIC - 1](https://www.youtube.com/watch?v=UsHiWIgxj2M&list=PLucm8g_ezqNp92MmkF9p_cj4yhT-fCTl7)
* [linux4noobs](https://github.com/LucasHe4rt/linux4noobs)

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
