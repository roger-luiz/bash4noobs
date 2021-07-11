<h1 align="center">
  Git
</h1>

<p align="center">
  <img src="../.github/gitcommit.png"/>
</p>

# Roadmap

* [Explicando alguns conceitos](#explicando-alguns-conceitos)
* [Configurando o git](#configurando-o-git)
* [Comandos](#comandos)
* [Alias (Opcional)](#alias-opcional)
* [Padronização de commits (Opcional)](#padronização-de-commits-opcional)
* [Ajustando o histórico de commits no github](#ajustando-o-histórico-de-commits-no-github)

## Explicando alguns conceitos

__`Repositório`__: O repositório é a pasta do projeto. Todo repositório tem uma pasta oculta `.git`. Isso é o que mostra o para o git e para você que existe  um repositório naquela pasta.

__`Commit`__: Um commit é um grupo de alterações no código. Toda vez que você quiser "salvar" as alerações feitas por você no repositório, você commita essas mudanças. Um commit contém as alterações que foram feitas nele e uma mensagem descritiva, além de informações meta (data, autor, etc). O ideal é que os commits sejam feitos de forma lógica e organizada, por exemplo: Você criou uma alteração no layout e vai comitar ela depois, aos invés de fazer commits separados ("Adição de div no HTML", "Alteração do CSS", "Link do CSS"), faça um só commit ("Alteração no layout: <pequena descrição sobre a alteração>").

__`Branch`__: Branches são separações de código. O branch padrão do projeto é o `master`. Branches normalmente são utilizados para separar __alterações grandes__ ou __novas funcionalidades__ do projeto, por exemplo: Existe um projeto de blog, os desenvolvedores já fizeram quase toda a parte do blog, mas existem alterações para fazer no sistema de usuário do blog e algumas a fazer no sistema de post do blog. Para isso, cria-se uma branch "users" e uma "posts" e fazem-se as aterações nessas branches, um time trabalha em cada uma dessas branches, enquanto isso, outro time continua trabalhando em pequenas mudanças ou bugkixies na branch master.

__`Merge`__: Um merge é a união de duas brnches, normalmente, merges são feitos na branch master. No exemplo do blog, quando a alteração do blog for terminada, alguém vai unir essas alterações na branch master para que elas possam finalmente fazer parte do projeto de fato. Os merges constumam dar bastante problema, pois os códigos podem (e provavelmente vão entrar em conflito). Se houveram alterações no mesmo arquivo ou o git não conseguir definir se alguma linha deve ou não entrar no projeto por motivo de conflito, essas alterações deverão ser corrigidas manualmente.

__`Clone`__: Um clone de um repositório funciona como uma branch de um repositório online em um repositório local. Ou seja, quando se deseja trabalhar em um repositório hospedado no github, clona-se esse repositório para o seu computador, trabalha-se nele, e então é pedido a permissão para atualizar as alterações online.

__`Pull`__: É uma atualização do repositório local. É feito um merge de repositório online com o local para que os conflitos sejam resolvidos e seja possível eviar o código (sem conflitos) para o repositório online por meio de um push.

__`Push`__: Enviar o código para o repositório online

__`Fork`__: O fork é como um clone, porém dentro do Github. Isso quer dizer que o repositório não vai ser baixado para seu computador, mas será criado um igual na sua conta.

__`Pull Request`__: um pull request é um pedido que faz ao dono do repositório para que esse atualize o código dele com o seu código. Ou seja, você pede para que o dono do projeto ao qaul você quer contribuir adicione suas modificações ap projeto oficial.

## Configurando o git

1. Instalção: https://git-scm.com/downloads
2. Documentação: https://git-scm.com/do

Antes de começar a usar o git é importante que você tenha ele configurado corretamente em sua máquina.

* `git config --global user.name "Fulano de Tal"`: Nome, coloque o mesmo nome do __github__;
* `git config --global user.email fulanodetal@exemplo.br`: Email, coloque o mesmo email do __github__;
* `git config --global core.editor vim`: Editor, aqui você pode escolher o editor padrão do git;
* `git config --list`: Use para ver o resultado das suas confirugarções.

## Comandos

* `git init`: Cria um repositório git vazio.

* `git status`: Informa o estado das alterações do nosso projeto.

* `git add [file]`: Adiciona ou atualiza mudanças para irem para o nosso repositório.
  * `git add .`: Você pode adicionar todos os arquivo usando o ".".

* `git rm [file]`: Remove os arquivos que foram adicionados com o `git add`.

* `git commit -m "message"`: Registra alterações no repositório.
  * `git commit --amend -m "message"`: __Troca__ a mensagem feita no último commit.

* `git log`: Mostra os pontos na "linha do tempo" do repositório (commits).
  * `git log --oneline`: Mostra os pontos da "linha do tempo" de forma resumida.
  * `git log --abbrev-commit`: Mostra o hash dos commits com 7 caracteres.
  * `git log --pretty=oneline`: Faz com que caiba toda a mesagem de commit em uma linha.
  * `git log --graph`: Desenha uma representação gráfica dos commits no lado esquerdo da saída do terminal.
  * `git log --grep="palavra"`: Busca por commits que tenha a palavra especificada.

* `git diff`: Mostra o que foi alterado em um arquivo, de vermelho o que foi excluído, de verde o que foi adicionando. Use-o antes do `git add`.

* `git show`: Apresenta o último ponto na "história" do nosso projeto.
  * `git show [hash]`: Apresenta determinado ponto na "história" do nosso projeto.

* `git branch`: Lista e exclui ramificações do nosso repositório.
  * `git branch -d [ramificação]`: Exclui uma ramificação.

* `git checkout [hash]`: Alterna ramificações ou restaura arquivos da árvore de trabalho.
  * `git checkout -b [minha-feature]`: Cria uma nova ramificação no nosso projeto.
  * `git checkout [minha-ramificação]`: Vai para a ramificação criada pelo desenvolvedor.
  * `git checkout master`: Vai para a ramificação master.
  * `git checkout -- [arquivo-modificado]`: Descarta as mudanças feitas no arquivo. Use antes do `git add`.

* `git merge [branch]`: Faz a fusão de uma branch X com uma branch Y. Para fazer a fusão das branchs você tem que estar na branch que vai recber a outra branch.

* `git mv [arquivo] [diretório]`: Move um arquivo para um diretório especificado.
* `git mv [nome-original] [novo-nome]`: Renomea um arquivo.

* `git clean -f`: Remove arquivos não rastreados.

* `git reset --hard [hash]`: Reverte um commit.

* `git remote`: Verifica se existe um repositório remoto.

* `git push`: Envia alterações locais para o repositório remoto.

* `git clone [link-do-repositório]`: Clonar um projeto / repositório.

* `git pull`: Puxa do repositório remoto.

## Alias (Opcional)

Você pode criar alias para os comandos do git, basta ir no arquivo ".gitconfig" e definir seus alias.
No uninx (Linux e Mac) o arquivo ".gitconfig" fica localizado em: /home/seuusuário/.gitconfig

Alias que eu gosto de usar:

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

## Padronização de commits (Opcional)

De acordo com a documentação do __Convetional Commits__, Commits Semânticos são uma convenção simples para ser utilizada nas mensagens de commit. Essa convenção define um conjunto de regras para criar um histórico de commit explícito, o que facilita a criação de ferramentas automatizadas.

Esses commits auxiliarão você e sua equipe a entenderem de forma facilitada quais alterações foram realizadas no trecho de código que foi commitado.

Essa identificação ocorre por meio de uma palavra e emoji que identifica se aquele commit realizado se trata de uma alteração de código, atualização de pacotes, documentação, alteração de visual, teste...

Mas por que devo padronnizar meus commits?

* Criação automatizada de CHANGELOGs;
* Determinar automaticamente um aumento de versionamento semântico (com base nos tipos de commits);
* Comunicar a natureza das mudanças para colegas de equipe, o público e outras partes interessadas de forma padronizada
* Disparar processos de build e deploy;
* Facilitar a contribuição de outras pessoas em seus projetos, permitindo que eles explorem um histórico de commits mais estruturado e com melhor rastreabilidade.

Para poder padronizar seus commits, você pode usar duas ferramentas, o [commitlint](https://github.com/conventional-changelog/commitlint) e o [commitizen](https://github.com/commitizen/cz-cli), você pode instalar essas dependências usando o __npm__ ou o __yarn__.

__Formato da mensagem__: Cada mensagem de commit consiste em um `cabeçalho`, um `corpo` e um `rodapé`.

### Cabeçalho

O cabeçalho é obrigatório, tem um formato pré-definido, que inclui um `tipo` e um `título`:

```
<tipo>(<escopo opcional>): <título>

<corpo opcional>

<rodapé opcional>
```

Qualquer linha da mensagem do commit não pode ter mais de 100 caracteres! Assim fica mais fácil para ler no GitHub, Gitlab e outras ferramentas de git.

#### Tipos

Deve ser um dos seguintes:

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

#### Título

O título contém uma descrição sucinta da mudança:

* Use o imperativo, tempo presente: "mudança" não "mudou" nem "muda".
* Não capitalize a primeira letra.
* Sem ponto (.) no final.

:x: RUIM: `git commit -m "add user.js"`

:white_check_mark: BOM: `git commit -m ":recycle: - Migration created to person"`

Emojis para o título do `commit`:

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

### Corpo

Um corpo de mensagem de commit mais longo PODE ser fornecido após o título, fornecendo informações contextuais adicionais sobre as alterações no código. Configure a mensagem com um wrap de 80 caracteres. Use para explicar "o que" e "porque" foi realizado essa modificação, ao invez de "como". O corpo DEVE começar depois de uma linha em branco após a descrição.

### Rodapé

Um rodapé PODE ser fornecido depois de uma linha em branco após o corpo. Caso exista um ticket no jira, criar um referência assim: `issue TP-666` ou `closes issue TP-666`.

## Ajustando o histórico de commits no github

Pode acontecer do seu nome ou email no git serem diferente do seu nome ou email do github. Isso pode afetar diretamente o seu número de commits no github (quadro branco com quadradinhos verdes). Mas para concertar é simples.

Primeiro ajuste o nome e email que você deseja no git:

* `git config --global user.name "Nome Correto"`
* `git config --global user.email emailcorreto@exemplo.br"`

Crie um script sh (dê o nome fixing-commits.sh para ficar intuitivo) com o seguinte conteúdo:

```sh
#!/bin/sh

git filter-branch --env-filter '

OLD_NAME="Nome Antigo"
CORRECT_NAME="Nome Novo"
OLD_EMAIL="emailantigo@exemplo.br"
CORRECT_EMAIL="emailcorreto@exemplo.br"

if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
export GIT_COMMITTER_NAME="$CORRECT_NAME"
export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
export GIT_AUTHOR_NAME="$CORRECT_NAME"
export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi

if [ "$GIT_COMMITTER_NAME" = "$OLD_NAME" ]
then
export GIT_COMMITTER_NAME="$CORRECT_NAME"
export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_NAME" = "$OLD_NAME" ]
then
export GIT_AUTHOR_NAME="$CORRECT_NAME"
export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags
```

1. Mude o conteúdo da variável `OLD_NAME` para seu nome atual que será mudado.
2. Mude o conteúdo da variável `CORRECT_NAME` para o novo nome que você deseja colocar.
3. Mude o conteúdo da variável `OLD_EMAIL` para seu email atual que será mudado.
4. Mude o conteúdo da variável `CORRECT_EMAIL` para o novo email que você deseja colocar.

No console:

```console
# Clone o repositório que você deseja ajustar os commits usando a flag --bare
git clone --bare [repo]

# Navegue até o repositório pelo terminal
cd [repo]

# Rode o script sh
fixing-commits.sh

# Faça o push
git push --force --tags origin 'refs/heads/*'

# Delete o repo pois não se usa ele em modo bare
cd ..
rm -rf [repo]
```

É importante destacar que o script `não precisa` está na mesma pasta do projeto, mas no momento em que você roda o script você `deve estar` na pasta do projeto.
