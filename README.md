# DIO | Resumos Git e Github

Repositório para armezenar resumos sobre Git e Github do curso Versionamento de Código com Git e Github da [Digital Innovation One](https://www.dio.me/).

## 📚 Documentação
- [Documentação Git](https://git-scm.com/docs/git/pt_BR)
- [Documentação GitHub](https://docs.github.com/pt)

## 💻 Resumos das Aulas

| Aulas | Resumos |
|-------|---------|
| Configurando do Git | [Resumos]()|

```
git config

```
```
git config --global user.name <nome>
git config --global user.email <e-mail>"
git config --global --list

```
Para verificar qual o nome e o usuário foram cadastrados
```
git config --global user.name
git config --global user.email

```
Para verificar e mudar o nome da Branch
```
git config init.defaultBranch
git config --global init.defaultBranch main

```
| Aulas | Resumos |
|-------|---------|
| Criando e Clonando Repositórios | [Resumos]()|

Inicializando um novo repositório GIT e cria uma subpasta oculta chamada .git

```
git init

```
No contexto do Git, o arquivo "config" está localizado no diretório .git de um repositório Git e armazena as configurações específicas desse repositório. Isso inclui informações como o nome do autor, endereço de e-mail, configurações de alias, configurações de rastreamento de branches remotos e muito mais. (Dentro da pasta .git)

```
cat config

```
O comando git clone é usado para criar uma cópia completa de um repositório Git existente em um novo diretório local.
```
git clone <URL do repositório remoto>
git clone <URL do repositório remoto> <novo nome>

``` 
O comando git remote é usado para gerenciar os repositórios remotos associados ao seu repositório Git local.

```
git remote -v
git remote add origin <URL>
git remote remove <nome>
git remote show <nome>


``` 

| Aulas | Resumos |
|-------|---------|
| Salvando alterações no Repositório Local | [Resumos]()|

O comando git status é usado para verificar o estado atual do seu repositório Git local. O comando git status é frequentemente usado para revisar o estado do seu repositório antes de fazer commits.

```
git status

``` 




## Referências
- [Digital Innovation One]().
