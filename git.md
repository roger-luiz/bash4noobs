# Git

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