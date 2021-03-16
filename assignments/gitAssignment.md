# Git Assignment

**INDIVIDUAL**

**Entrega**: 18-Mar-21

## Como entregar
Copie o arquivo em um repositorio que seja seu e coloque as respostas nas caixas abaixo

Abra uma issue nesse repositório aqui indicando o link para o arquivo no seu repo.

### Entenda o repositorio
Baixe o arquivo [handson.zip] (handson.zip) e descompacte-o
A pasta handson é um repositório git. Usando a linha de comando, altere o diretório para "handson/"

As caixas vazias
```

```
representam o conteúdo que você precisa preencher e postar em seu repositório privado

1. Descreva qual é a saída dos seguintes comandos
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
git branch: Lista as duas branches do repositório: 'feature-foo' e 'master', e mostra que a branch atual é a master.
git checkout feature-foo: O retorno é "Switched to branch 'feature-foo'", indica que estou na branch descrita.
git log --decorate: Lista os últimos commits feitos com todas as referências do commit, como branch, autor, data, hash e descrição do commit.
```

2. Tente usar `git log --graph --all`. O que acontece?
```
Retornou uma representação gráfica do histórico dos commits baseada em texto, assim como todas as referências dos commits, junto com o HEAD.
```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

```
Diferença entre as duas branches nos arquivos: a/A.java e a/B.java, listando as linhas diferentes.
```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```
git checkout master
git merge feature-foo
```


5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
git checkout -b math
```
   
6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```
git add B.java
git commit -m "Update B.java"
```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
git merge math
```
   
10. Escreva um conjunto de comandos para abortar a mesclagem
```
git merge --abort
```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento
```
git merge math
nano B.java
(No arquivo, apague a linha que contém "<<<<<<< HEAD", a linha que contém "=======" e a linha que contém ">>>>>>> math")
ctrl+o pra salvar
ctrl+x pra sair
```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
git add B.java
git commit -m "Merge branch math"
git push origin master
```



