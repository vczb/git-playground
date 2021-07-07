## Git Playground


Envie sua PR com qualquer coisa, crie issues faça o que quiser fazer

:octocat: 

### Configurando o git:

_adiciona nome e email_

```
git config --global user.name "FIRST_NAME LAST_NAME"
git config --global user.email "email@example.com"
```

_adiciona VS Code como editor padrão_

```
git config --global core.editor 'code --wait'
```

### Comandos úteis:


#### git log

_log em uma linha e a branch associada_

```
git log --oneline --decorate
```

_mostra árvore_

```
git log --graph --oneline --decorate
```

_sem merge commits_

```
git log --no-merges --oneline
```

_apenas merge commits_

```
git log --no-merges --oneline
```

#### git revert

_cria um commit que desfaz as alterações do commit selecionado_

```
git revert HASH
```

#### git push

_deleta uma branch remota_

```
git push origin :nome-da-branch
```

#### git fetch

_faz sincronização com todos as remotes_

```
git fetch --all
```

_faz sincronização com com a remote upstream_

```
git fetch upstream
```

#### git reset

_reseta tudo com o último commit salvo na sua branch local_

```
git reset --hard HEAD
```

_reseta tudo com o último commit salvo na origin upstream branch main_

```
git reset --hard upstream/main
```

#### git rebase

_realinha seu histórico de commit colocando os commits locais por cima dos da origin upstream branch main_

```
git rebase upstream/main
```

_realinha seu histórico de commit colocando o commit de hash 5176a1057 por cima dos demais_

```
git rebase 5176a1057
```

_faz rebase interativo permitindo mover, mesclar, remover e entre outras ações aos commits_

```
git rebase -i HEAD~10
```

```
# Commands:
# p, pick <commit> = use commit
# r, reword <commit> = use commit, but edit the commit message
# e, edit <commit> = use commit, but stop for amending
# s, squash <commit> = use commit, but meld into previous commit
# f, fixup <commit> = like "squash", but discard this commit's log message
# x, exec <command> = run command (the rest of the line) using shell
# d, drop <commit> = remove commit
# l, label <label> = label current HEAD with a name
# t, reset <label> = reset HEAD to a label
# m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
# .       create a merge commit using the original merge commit's
# .       message (or the oneline, if no original merge commit was
# .       specified). Use -c <commit> to reword the commit message.
#
# These lines can be re-ordered; they are executed from top to bottom.
```


#### git amend

_mescla todas as alterações no último commit da sua branch local_

```
git commit --amend --no-edit
```

_altera o nome do commit_

```
git commit --amend -m 'Minha nova mensagem de commit'
```

#### git reflog

_monitora as referências atualizadas no repositório local_

```
git reflog
```

_reflog completo de todas as referências_

```
 git reflog show --all 
```

#### git remote

_lista todos os repositórios remotos_

```
 git remote -v
```

_adiciona uma url de um repositório git chamada origin_

```
 git remote add origin git@github.com:vczb/git-playground.git
```

_remove a origin_

```
 git remote remove origin
```

#### git branch

_lista todas as branchs locais_

```
 git branch -v
```

#### git checkout 

_reseta o arquivo orange conforme o mesmo arquivo na branch origin/main_

```
git checkout origin/main -- orange.md
```

_muda para uma branch existente_

```
git checkout nome_da_branch
```

_cria uma nova branch e usa ela_

```
git checkout -b nome_da_branch
```

#### git show

_mostra as alterações_

```
git show
```

_mostra os arquivos alterados_

```
git show --name-only
```

#### git mv

_move um arquivo e preserva o histórico git dele_

```
git mv arquivo destino
```

#### git blame

_Exibe metadados do autor anexados a linhas de commit específicas em um arquivo_

```
git blame README.md
```

#### git stash

_Guarda as alterações na branch sem precisar dar commit_

```
git stash
```

_Lista as alterações guardadas_

```
git stash list
```

_Recupera a última alteração guardada_

```
git stash pop
```

_Recupera a alteração guardada de índice "2"_

```
git stash apply 2
```

---
## Artigos:

- [Convenção de commits](https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/)
- [A Git Workflow Using Rebase](https://medium.com/singlestone/a-git-workflow-using-rebase-1b1210de83e5)
- [Manter repositório do Github forkado sincronizado com o original](https://blog.da2k.com.br/2014/01/19/manter-repositorio-github-forkado-sincronizado-com-o-original/)
- [Guia: Como contribuir em Open Source](https://willianjusten.com.br/guia-como-contribuir-em-open-source/)
- [Mesclagem vs. Rebase](https://www.atlassian.com/br/git/tutorials/merging-vs-rebasing)

## Vídeos:

- [Git e Github para iniciantes](https://www.youtube.com/playlist?list=PLlAbYrWSYTiPA2iEiQ2PF_A9j__C4hi0A)
- [Como usar Git e Github na prática: Guia para iniciantes](https://www.youtube.com/watch?v=2alg7MQ6_sI)

## Interessante:

- [git-flow](https://github.com/petervanderdoes/gitflow-avh)
- [bash-git-prompt](https://github.com/magicmonty/bash-git-prompt)

## Docs:

- [Git](https://git-scm.com/doc)
- [Github](https://docs.github.com/pt)
- [Bitbucket](https://www.atlassian.com/git/tutorials)
- [Emojis](https://gist.github.com/rxaviers/7360908)
