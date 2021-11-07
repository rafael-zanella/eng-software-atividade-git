# Guia de uso GIT

## Inicialização do repositório local

```bash
$ git init
```

A execução desse comando cria um novo subdiretório `.git` no diretório de trabalho atual. Essa ação também vai criar uma ramificação principal (`master` ou `main`).

## Clonagem

```bash
$ git clone <repo url>
```

Se um projeto já foi configurado em um repositório central, o comando clonar é a forma mais comum para os usuários obterem um clone de desenvolvimento local. Como o `git init`, a clonagem é geralmente uma operação única. Depois que um desenvolvedor obtiver uma cópia ativa, todas as operações de controle de versão serão gerenciadas pelo seu repositório local.

## Criação de branches

```bash
$ git checkout -b <nome da branch>
```

Uma `branch` ou "ramificação" representa uma linha independente de desenvolvimento. As ramificações funcionam como uma abstração para o processo de edição/estágio/confirmação. Você pode pensar nelas como uma forma de solicitar um diretório de trabalho, uma área de `staging` e um histórico do projeto totalmente novos. Novas confirmações são registradas no histórico para a ramificação atual, que resulta em uma bifurcação na história do projeto.

## Add & Commit

```bash
$ git add <arquivo ou diretorio>
$ git commit -m "meu primeiro commit"
```

O comando `git add` adiciona uma alteração no diretório ativo à área de `staging`. Ele diz ao Git que você quer incluir atualizações a um arquivo específico no próximo `commit`. No entanto, `git add` não tem efeito real e significativo no repositório — as alterações não são gravadas mesmo até você executar `git commit`.

Junto com esses comandos, você também vai precisar de `git status` para ver o estado do diretório ativo e da área de `staging`.

## Push

```bash
$ git push origin <nome da branch>
$ git pull
```

O comando `git push` envia tudo que foi "commitado" para um repositório remoto em uma `branch` especifica.

O comando usa dois argumentos:

- Um nome de remote, por exemplo, `origin`
- Um nome de `branch`, por exemplo, `master`

## Pull

O comando `git pull` é uma abreviação do comando `git fetch` seguido por `git merge FETCH_HEAD`, que é usado para buscar e baixar conteúdo de repositórios remotos e fazer a atualização imediata ao repositório local para que os conteúdos sejam iguais.

## Pull Requests (PR)

Os `pull requests` permitem que você informe outras pessoas sobre as alterações das quais você fez `push` para um `branch` em um repositório no GitHub.

## Merge

```bash
$ git merge develop
```

`Merge` ou "mesclagem" é o jeito do Git de unificar um histórico bifurcado. O comando `git merge` permite que você pegue as linhas de desenvolvimento independentes criadas pelo `git branch` e as integre em uma ramificação única.

# Referências

[https://www.atlassian.com/br/git/tutorials/learn-git-with-bitbucket-cloud](https://www.atlassian.com/br/git/tutorials/learn-git-with-bitbucket-cloud)

[https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/about-collaborative-development-models](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/about-collaborative-development-models)

[https://git-scm.com/docs](https://git-scm.com/docs)