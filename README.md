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
Permite ver as atuzalizações feitas:
```bash
git log
```
---
Iniciar um novo repositório:
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
git add .
```
---
Registra/salva a alteração no repositório:
```bash
git commit -m "escolha um nome pro Commit"
```
---
Informa a pasta remota:
```bash
git remote add origin https://github.com/sua-pasta/de-exemplo.git
```
---
Publica as alterações no repositório remoto:
```bash
git push -u origin master
```
---
Permite visualizar informações sobre qualquer commit:
```bash
git show número-do-commit
```
---
Permite visualizar o repositório remoto:
```bash
git remote -v
```
---
Baixa as alterações no repositório remoto.:
```bash
git pull
```
---
Gerar uma key:
```bash
ssh-keygen
```
---
Desfazer commi:
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