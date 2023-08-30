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
O comando git add é usado para adicionar mudanças no seu diretório de trabalho ao índice (staging area) do Git. O índice é uma área intermediária onde você prepara as alterações antes de criar um commit. Basicamente, o git add sinaliza ao Git que você deseja incluir as alterações específicas em seu próximo commit.

```
git add <arquivo1> <arquivo2>...
git add arquivo.txt
git add .
git add diretorio/`

```
O comando git commit é usado para criar um novo commit (ou registro) no repositório Git. Um commit no Git é uma "foto" ou instantâneo de todas as alterações que foram preparadas no índice (staging area) com o comando git add. Esse commit é então adicionado ao histórico do projeto.

```
git commit -m <"Mensagem de commit aqui">

```
O comando git log é usado para visualizar o histórico de commits de um repositório Git. Quando você executa git log, o Git exibe uma lista de commits em ordem cronológica reversa (do commit mais recente para o mais antigo), juntamente com informações sobre cada commit, como autor, data, hora e mensagem de commit.

```
git log

```
O arquivo .gitignore é usado para especificar arquivos e diretórios que você deseja que o Git ignore quando estiver rastreando alterações em um projeto. Isso significa que quaisquer arquivos ou diretórios listados no arquivo .gitignore não serão incluídos no controle de versão do Git e não aparecerão como alterações não rastreadas quando você executa comandos como git status.

A principal finalidade do .gitignore é evitar que arquivos e diretórios irrelevantes ou sensíveis ao contexto (como arquivos de configuração local, arquivos de compilação, arquivos temporários, arquivos de log e diretórios de saída) sejam acidentalmente incluídos em um commit.

``` 
echo <nome_da_pasta>/ > .gitignore
echo > .gitignore

```
| Aulas | Resumos |
|-------|---------|
| Desfazendo Alterações no Repositório Local | [Resumos]()|

Suponhamos que inicializamos um repositório na pasta errada, ou seja, com git init.

```
rm -rf .git

``` 
O comando git restore é usado no Git para desfazer ou restaurar alterações nos arquivos do seu repositório para um estado anterior. Esse comando é usado para gerenciar o estado dos arquivos no seu diretório de trabalho e pode ser útil em várias situações.

```
git restore <arquivo>

``` 
Correção da mensagem do commit, onde podemos ver o relatário dos commits com o comando git log

```
git commit --amend -m <"nova mensagem">
git commit --amend OBS: este abre um editor!!!

``` 
O comando git reset é usado para desfazer ou reverter commits no Git. Ele é uma ferramenta poderosa, mas também pode ser arriscado, pois pode alterar o histórico de commits. Portanto, é importante usá-lo com cuidado.

```
git reset --soft <commit>
git reset <commit>
# ou
git reset --mixed <commit>
git reset --hard <commit>
git reset HEAD~1

``` 
| Aulas | Resumos |
|-------|---------|
| Enviando e baixando alterações com o repositório remoto | [Resumos]()|

Em Git, git remote é um comando usado para gerenciar repositórios remotos. 

git remote add: Este comando é usado para adicionar um novo repositório remoto ao seu projeto Git.

``` 
git remote add origin <URL_do_repositorio_remoto>
git remote remove origin
git remote rm origin
git remote rename origin novo-origin
git remote show origin
git remote -v

```
O comando git push é usado no Git para enviar as alterações locais em um repositório Git para um repositório remoto.

```
git push -u origin main

```
Alterações do repositório remoto para o repositório local:

O comando git pull é usado para atualizar seu repositório local com as alterações do repositório remoto. Em essência, ele combina dois outros comandos do Git: git fetch e git merge.

```
git pull

```

| Aulas | Resumos |
|-------|---------|
|Trabalhando com Branches, Criando, Mesclando, Deletando e Tratando Conflitos | [Resumos]()|

De maneira simplista, uma Branch (em tradução, "Ramo"), é uma ramificação do seu projeto.
É um ponteiro móvel para um commit no histórico do repositório;
Quando você cria uma nova Branch a partir de outra existente, a nova se inicia apontando para um mesmo commit da Branch que estava quando foi criada.

O comando git checkout -b é usado para criar e mudar para uma nova branch em um repositório Git. Ele combina duas operações: criação de uma nova branch e a mudança imediata para essa nova branch.

```
git checkout -b <nome_da_nova_branch>

```

Obs: Quando nos criamos uma branch dentro de uma já existente, essa nova passa a apontar para o mesmo commit da onde ela originou.

```
git checkout <nome_da_branch_de_"origem">

```
Obs: Criada o arquivo na branch nova, ela não vai aparecer na branch de origem.
Caso queira que as alterações da branch nova apareram na branch de origem, precisamos MESCLAR elas.

```
git merge <nome_da_nova_branch>

```

Para deletar uma branch:

```
git branch -d <nome_da_branch>

```

| Aulas | Resumos |
|-------|---------|
|Trabalhando com Branches - Comandos Úteis no Dia a Dia | [Resumos]()|

git fetch: Ele busca todas as atualizações do repositório remoto, mas não as mescla em seu repositório local. Isso atualiza suas referências locais para as branches remotas, permitindo que você veja o que mudou no repositório remoto sem fazer nenhuma alteração em seu trabalho atual.

git merge (ou git rebase, dependendo das configurações padrão): Após o git fetch, o git pull faz uma mesclagem automática das alterações buscadas com a branch em que você está trabalhando atualmente. Ele tenta fundir as alterações do repositório remoto em sua branch local.

```
git fetch origin <nome_do_repositório_remoto>

git merge origin <branch_para_a_mesclagem>

```
Clonando um repositório selecionando apenas uma branch especifica:

```
git clone <URL> --branch <nome_da_branch> --single-branch

```

O comando git stash é usado para temporariamente armazenar mudanças não comprometidas (alterações no código que você ainda não confirmou usando git commit). Isso pode ser útil quando você precisa alternar rapidamente entre branches, mas não deseja comprometer suas alterações em andamento.

```
git stash
git stash list
git stash pop
git stash apply

```




## Referências
- [Digital Innovation One]().
- [https://github.com/elidianaandrade/dio-curso-git-github/blob/main/materiais-de-apoio/04-dicas-e-materiais-de-apoio.md]().
