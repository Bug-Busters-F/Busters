# Como Contribuir - Seu Passaporte de Entrada

Bem-vindo ao nosso projeto! Este documento é feito para facilitar uma colaboração eficiente e eficaz entre todos os membros da equipe. Aqui você encontrará as informações necessárias para contribuir de forma harmoniosa e produtiva.

## Código de Conduta

Para garantir um ambiente respeitável e inclusivo, leia e siga nosso [Código de Conduta](./CODE_OF_CONDUCT.md).

## Mão na Massa - Como Contribuir

Depois de [configurar](#como-começar) tudo direitinho, você vai estar pronto para colocar a mão na massa e fazer suas próprias contribuições. Aqui vai um guia simples de como levar isso para o nosso projeto:

### 1. Branching

Lembre-se de não enviar commits diretamente para o branch principal. Isso é essencial para manter a organização e integridade do nosso projeto. Ao iniciar um novo trabalho, crie um branch separado a partir do branch de desenvolvimento - ou utilize um já existente apropriado para o desenvolvimento. Você pode seguir as seguintes sugestões de nomes:

#### Quais nomes para os novos branches?

`feature/<nome-do-recurso>` para criar um novo recurso

More Examples:

- `feat` or `feature`: (new feature for the user, not a new feature for build script)
- `fix`: (bug fix for the user, not a fix to a build script)
- `docs`: (changes to the documentation)
- `style`: (formatting, missing semi colons, etc; no production code change)
- `refactor`: (refactoring production code, eg. renaming a variable)
- `test`: (adding missing tests, refactoring tests; no production code change)
- `chore`: (updating grunt tasks etc; no production code change)

```sh
# Ver branch ativo
git branch
# irá aparecer os branches existentes. O branch ativo é aquele que tiver marcado com * e estiver em verde (no Git bash).

# Troca para o branch 'dev'
git checkout dev

# Criar um novo branch e troca para ele
git checkout -b <nome-do-branch> # Ex: feature/quizzes

# JIRA issue
git checkout -b JRA-123-<branch-name>
```

Tem um template que você pode baixar nesse [GitHub Gist](https://gist.github.com/WesleyGoncalves/c4d6799f26931e478e1b74a05c7f0a5a).

Depois de baixar é só rodar esse comando pra configurar o git.

```sh
git config --global commit.template caminho-para-o-arquivo/.git-commit-template
```

Esse arquivo não pode ser excluído.

### 2. Fazer Commit

Faça suas modificações e, em seguida, o seu commit.

```sh
# Garanta que você está na pasta do projeto
pwd
# resposta esperada:  ......../scrum-academy

# Add as modificações
# add todas as modificações para serem comitadas
git add .
# ou
# add file1 e file2 presentes em 'src' para serem comitados
git add src/file1 src/file2

# Mostra modificações no repo desde o último commit, e os arquivos que estão em Stage
git status
# Resultado:
#   On branch dev - indica que vc está no branch dev
#   Changes to be committed - o que vc add ao stage
#   Changes not staged for commit - o que NÃO será commitado
#   Untracked files - arquivos novos que não serão commitados

# Faz o commit
git commit -m "O que o meu commit está modificando/adicionando."
# altere a mensagem. Tente explicar suscintamente o que o seu commit está adicionando ou alterando
# obs.: você pode commitar uma coisa de cada vez. Por ex.: primeiro commita o Header, depois commita o Footer, em 2 commits.

# JIRA
git commit -m "JRA-123 <commit message>"
```

### 3. Enviar suas modificações

Lembre-se de não enviar para o branch principal do projeto. Por isso, garanta que você está no branch 'dev'. Dê uma olhada em [Branching](#branching), se precisar.

Há dois repos com os quais estamos trabalhando:

1. O repo remoto (no GitHub) que centraliza as modificações que todos fazem. Funciona como um servidor
2. O repo local (na sua máquina) que é uma cópia do repo remoto.

```sh
# Garanta que você está no branch que você criou
# ver Branches

git push -u origin <nome-do-branch>
```

### GitHub integrado com Jira

Assim, nós podemos criar coisas no Git que serão sincronizadas automaticamente no Jira. Para isso, precisa colocar o código da Tarefa do Jira (por ex.:  ALP-12) nos nomes/mensagens no Git.

Isso é feito relacionadas a essas 3 ações do Git:

1. Nome do Branch `git checkout -b ALP-123-<branch-name>`
2. Mensagem de commit `git commit -m "ALP-123 <commit message>"`
3. Nome de um PR

Referência: https://support.atlassian.com/jira-software-cloud/docs/reference-issues-in-your-development-work/

Existe também a possibilidade de realizar ações no Jira pela sua mensagem no commit, chamados Smart Commits. Por exemplo, para fechar uma tarefa através da sua mensagem do commit.

```sh
git commit -m "ALP-12 Add.....

ALP-12 #close
```

O Jira irá fechar a tarefa automaticamente por causa da última linha

### 4. Criar um Pull Request (PR)

Se tudo estiver pronto para fazer merge no branch de desenvolvimento, abra o GitHub e crie um **Pull Request**.

1. Abra o repositório pela interface do GitHub
2. Clica na aba **Pull Request**
3. Aperta no botão  **New Pull Request**
4. Seleciona o branch `dev` à esquerda e **o seu branch** à direita
5. Aperta em **Create Pull Request**
6. Escreve uma mensagem sobre as modificações feitas e aperta em **Create Pull Request**
7. Agora, alguém irá validar as suas modificações
8. Após a aprovação de outro integrante, você poderá fazer Merge
9. Se tiver confilitos, você pode resolver apertando em **Resolve conflicts**

#### 4.1. VALIDAR UM PULL REQUEST

Se outro integrante criar um Pull Request, você pode **aprovar** (se estiver pronto para fazer merge) ou **sugerir melhorias** (para o autor aprimorar o projeto). Os dois tópicos a seguir indicam como realizar essas operações.

##### REVIEW A PULL REQUEST

1. On the pull request, click Files changed.
2. Click Review changes.
3. Add a comment on your initial thoughts
4. Select comment, approve or request changes on the pull request.
5. Click Submit review.

##### SUGGEST CHANGES

1. On the pull request, click **Files changed**.
2. Find the `index.html` changes.
3. Hover your cursor next to the line numbers on the left side of the page.
4. Click the blue plus icon.
5. After the comment form appears, click the **Add a suggestion** button.

    ![Ícone para add suggestion](https://user-images.githubusercontent.com/97056108/184449714-61e8ee51-824a-48c1-9436-2dfd67f2c070.png "Índice para add suggestion")

6. Edit the suggestion.
7. Click **Add a single comment**.

### 5. Após merge, excluir os branches

Se tudo deu certo e você não vai mais precisar do branch que você criou, você pode apagar do repo remoto e do seu repo local.

```sh
# excluir branch do local
git branch -d <nome-do-branch>

# excluir branch do remote repo
git push -d origin <nome-do-branch>

# Se precisar excluir o branch sem ter feito o merge, use `-D` ao invés de `-d`. Mas CUIDADO porque isso irá apagar todos os commits dele.
```

### Resumo

1. Crie um novo branch
2. Faça suas modificações
3. Pelo terminal, navegue até o diretório raiz do projeto
4. Add modificações ao stage
5. Commit essas modificações
6. Push seu branch para o repo remoto
7. Cria um PR
8. Espera a Review de um membro da equipe
9. Faça modificações, se forem sugeridas
10. Faça o merge, quando tudo estiver pronto
11. Exclua os branches do repo remoto e local, se não for mais os usar

## Code Styling

Isso garante que todos os contribuidores sigam as mesmas normas de formatação, o que resulta em um código mais limpo e fácil de manter.

Algumas extensões indicadas lá em cima auxiliam na formatação do código. Como exemplos, a Editorconfig e a Black Formatter.

No VSCode, alguns atalhos facilitam a formatação do código:

- `Shift + alt + F` (Windows) |`Ctrl + Shift + I` (Linux) - formata o código
- `Ctrl + Shift + M`: abre a aba do relatório de Problemas

- Python Guideline: [Python official guidelines - PEP8](https://peps.python.org/pep-0008/).

## Mais sobre as tecnologias

### Markdown

Veja o [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/).

Instale as extensões de Markdown para facilitar o uso no [vscode - *clique aqui*](#visual-studio-code).

---
---

## Commit de Gratidão

Ninguém faz nada sozinho, e cada contribuição importa! 🌟 A colaboração de cada um é essencial para avançarmos de forma sólida e construtiva. Vamos manter o bom trabalho e reconhecer cada passo que nos leva adiante.

![Bug Busters](./assets/bug-busters-logo-black.jpg)
