# Comandos que mais utilizo no GIT.

Testando Suas Configurações:
```bash
git config --list
```
---

configuração do nome de usuário:
```bash
git config --global user.name "Nome-usuário"
```

---

Configuração de e-mail:
```bash
git config --global user.email "seu-email.com.br"
```
---
Gerar Key pro github
```bash
ssh-keygen -t ed25519 -c "seu-email-do-github"
```
---
Gerar uma key:
```bash
ssh-keygen
```
---

Permite ver as atuzalizações feitas:
```bash
git log
```
---
### Git init
O principal comando para inicializar o git é o git init. Ao executar esse comando uma pasta chamada .git é criada no diretório onde ele foi executado e nessa pasta você pode fazer o link para a origem (origin) remota, que pode ser o GitHub, GitLab, Bitbucket ou qualquer outra plataforma que utilize o Git,ele é utilizado para iniciar um novo repositório.
```bash
git init
```
---

Verifica o status das alterações realizadas no repositório:
```bash
git status
```
---
Adiciona arquivos ao histórico do projeto, na staging:
```bash
git add <. ou arquivo ou pasta>

# Adicionando todos os arquivos e pastas
git add .

# Adicionando um arquivo
git add index.html

# Adicionando uma pasta
git add assets

# Desfaz o comando git add .
git reset
```
---
### Registra/salva a alteração no repositório:
```bash
git commit -m "escolha um nome pro Commit"
```
ou
```bash
# Exemplo
git commit -m "feat(auth): create login screen"
```
---
#### Informa a pasta remota:
```bash
git remote add origin https://github.com/sua-pasta/de-exemplo.git
```
---
### Git push
Esse comando faz com que todos os nossos commits sejam empurrados (tipo um upload) na origem do repositório, poe exemplo, dentro do GitHub. Ao executar com o `-u` você está dizendo que essa branch faz parte de um repositório remoto, o `-u` é uma abreviação para o `--set-upstream`.

Não será necessário utilizar o -u o tempo todo, apenas quando novas branches forem criadas para joga-las no provedor Git.

Caso o git push seja executado sem o -u será necessário sempre informar a origem e o nome da branch para que as alterações sejam levadas ao provedor Git.

```bash
git push -u origin master
```
ou
```bash
# Na primeira vez
git push -u origin <nome_da_branch>
```
ou
```bash
# Quando executado sem -u
git push origin <nome_da_branch>
```
---
### Permite visualizar informações sobre qualquer commit:
```bash
git show número-do-commit
```
---
### Permite visualizar o repositório remoto:
```bash
git remote -v
```
---
### Baixa as alterações no repositório remoto:
```bash
git pull
```
ou
```bash
# Se precisar buscar na origin, quando não foi feito `git push -u`
git pull origin <nome_da_branch>
```
### Git checkout
O git checkout acessa branches, ou seja, ramificações existentes (locais ou remotas) e também cria uma nova branch a partir de outra que você já esteja, quando acompanhado do -b em sua execução.

As branches normalmente são utilizadas para criar novas features sem precisar afetar a principal, ou seja, a branch main (na maior parte dos casos), Como utilizar:
```bash
git checkout <nome_da_branch>

# Para criar uma nova branch
git checkout -b <nome_da_branch>
```
Lista todas as branches locais ou remotas, também delete branches locais.

Como utilizar:
```bash
git branch

# Para deletar uma branch local
git branch -D <nome_da_branch>

# Para deletar uma branch remota
git push --delete origin <nome_da_branch>
```
### Git rebase
Esse comando alinha todos os commits de uma branch, seja a principal ou qualquer outra que você escokher na branch atual em que você está localizado, porém sem criar um novo commit, como faz o git merge, mantendo o histórico linear.
```bash
git rebase <nome_da_branch>

# Exemplo, você atualmente está na branch "tela-de-login"
git rebase main
```
### Se precisar buscar na origin, quando não foi feito `git push -u`
```bash
git pull origin <nome_da_branch>
```
---
Desfazer commit:
```bash
git reset HEAD~1
```
---
apagar um repo:
```bash
rm -rf .git
```
---
Renomear commit:
```bash
git commit --amend

```
---
listar conflitos:
```bash
git diff --base
```
---

Apagar último Commit do repositório, encontre o hash do commit que deseja reverter:
```bash
git log
```

Use o comando git revert seguido pelo hash do commit:
```bash
git revert <hash_do_commit>
```

Faça o push das mudanças para o repositório remoto:

```bash
git push origin <nome_da_branch>

```


Apagar o último commit no repositório local:

```bash
git reset --hard HEAD~1

```

Atualizar o repositório remoto


```bash
git push origin <nome_da_branch> --force
```

---
