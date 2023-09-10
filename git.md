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

* `git diff`: Mostra o que foi alterado em um arquivo, de vermelho o que foi excluído, de verde o que foi adicionando. Use-o antes do git add.

* `git show`: Apresenta o último ponto na "história" do nosso projeto.
  * `git show [hash]`: Apresenta determinado ponto na "história" do nosso projeto.

* `git remote`: Verifica se existe um repositório remoto.

* `git push`: Envia alterações locais para o repositório remoto.

* `git clone [link-do-repositório]`: Clona um repositório (Github por exemplo).

* `git pull`: Puxa as alterações feitas no repositório remoto (Github por exemplo).

* `git reset [arquivo]`: Remove um arquivo adicionado com o git add, use antes do git commit.
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

Cada mensagem tem um formato pré-definido, que inclui um tipo e um título:

```
git commit -m "[tipo]: [menssagem]"
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

Use o imperativo, tempo presente: "mudança" não "mudou" nem "muda".
Não capitalize a primeira letra.
Sem ponto (.) no final.

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