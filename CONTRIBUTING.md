# Como Contribuir - Seu Passaporte de Entrada

Bem-vindo ao nosso projeto! Este documento é feito para facilitar uma colaboração eficiente e eficaz entre todos os membros da equipe. Aqui você encontrará as informações necessárias para contribuir de forma harmoniosa e produtiva.

## Código de Conduta

Para garantir um ambiente respeitável e inclusivo, leia e siga nosso [Código de Conduta](./CODE_OF_CONDUCT.md).

## Ferramentas e Linguagens utilizadas

Nosso projeto utiliza uma variedade de tecnologias para desenvolvimento e comunicação. Aqui estão algumas das principais tecnologias que você encontrará:

- Visual Studio Code
- Git
- GitHub
- Flask
- Figma
- Discord
- WhatsApp
- Python v3
- MySQL
- HTML, CSS, JS com Bootstrap
- Markdown
- Draw.io

## Como começar

Antes de tudo, relaxe! Aqui não tem bicho de sete cabeças. 🐉 Para começar:

1. Siga o [código de conduta](./CODE_OF_CONDUCT.md) para garantir um ambiente respeitável e inclusivo
2. [**Configure o seu ambiente de desenvolvimento**](#configure-o-seu-ambiente-de-desenvolvimento) com as [tecnologias utilizadas](#ferramentas-para-desenvolvimento) no projeto. Dê uma olhada nas extensões do vscode para manter nosso código limpinho e bonitinho. Isso ajuda todo mundo a seguir o mesmo estilo e facilita a vida de quem for revisar seu código.
3. Clone o projeto e **crie seu branch**: Por favor, **não envie nada direto pro branch principal**. Crie um branch alternativo - ou utilize um existente exclusivo para o desenvolvimento - e mande ver nas modificações. Quando estiver tudo pronto, é só dar um *push* para esse branch.
4. Faça as alterações, *commit* e envie (*push*) para o repo remoto. Dê uma olhada em [Git](#git-help).

Para continuar, garanta que você tem:

- Python3 instalado e configurado no terminal
- `venv` - o pacote de ambiente virtual em Python
- Visual Studio Code
- Git e Git Bash

No final dessa configuração, você terá :

- Uma cópia do projeto
- Um ambiente virtual configurado
- As dependências do projeto instaladas
- Um servidor Flask
- O Visual Studio Code configurado com extensões para facilitar o desenvolvimento

### 1. Instalar extensões do VSCode

Para uma experiência de desenvolvimento mais suave, recomendamos instalar as seguintes extensões do VSCode que vão facilitar nossa vida. São elas:

- [Auto Complete Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-complete-tag) - auto close HTML tags
- [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) - Launch a development local Server with live reload feature
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) - escreva markdown facilmente {markdown-all-in-one}
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) - Markdown linting and style checking
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) - formata código CSS, JS etc.
- [IntelliSense for CSS class names](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion) - autocompleta classes (como do Bootstrap) - autocomplete classes found in your workspace or external files referenced through the link element.
- [CSS Auto prefix](https://marketplace.visualstudio.com/items?itemName=sporiley.css-auto-prefix) - Add propriedades CSS para compatibilidade com outros dispositivos
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) - correct spelling errors
- [Editorconfig](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) - styling
- [Git graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph) - git graph
- [GitHub Pull Request](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) - Facilita a programação com Python - Microsoft's extension
- [Pylint](https://marketplace.visualstudio.com/items?itemName=ms-python.pylint) - Destaca erros de digitação - Microsoft's extension
- [Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter) - formata o código (code styling)
- [isort](https://marketplace.visualstudio.com/items?itemName=ms-python.isort) - sort the Python imports
- [autoDocstring](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring) - Doc string generator
- [Python Indent](https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent) - correct indentation
- [Jinja - Flask](https://marketplace.visualstudio.com/items?itemName=wholroyd.jinja) - Colore sintaxe do Jinja

Para instalar, abra o terminal no vscode e cole os seguintes comandos:

```sh
code --install-extension formulahendry.auto-complete-tag
code --install-extension ritwickdey.LiveServer
code --install-extension yzhang.markdown-all-in-one
code --install-extension DavidAnson.vscode-markdownlint
code --install-extension esbenp.prettier-vscode
code --install-extension Zignd.html-css-class-completion
code --install-extension sporiley.css-auto-prefix
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension EditorConfig.EditorConfig
code --install-extension mhutchie.git-graph
code --install-extension GitHub.vscode-pull-request-github
code --install-extension ms-python.python
code --install-extension ms-python.pylint
code --install-extension ms-python.black-formatter
code --install-extension ms-python.isort
code --install-extension njpwerner.autodocstring
code --install-extension KevinRose.vsc-python-indent
code --install-extension wholroyd.jinja
```

#### Configurar as extensões

Aperte `Ctrl + Shift + P` no vscode, digite "User Settings JSON" e aperte em `Preferences: Open User Settings (JSON)`

Digite no início do arquivo após o símbolo `{`:

```json
    "[html]": {
      "editor.defaultFormatter": "vscode.html-language-features",
      "editor.formatOnSave": true
    },
    "[css]": {
      "editor.defaultFormatter": "vscode.css-language-features",
      "editor.formatOnSave": true
    },
    "[json]": {
      "editor.defaultFormatter": "vscode.json-language-features",
      "editor.formatOnSave": true
    },
    "pylint.lintOnChange": true,
    "[python]": {
      "editor.defaultFormatter": "ms-python.black-formatter",
      "editor.formatOnSave": true
    },
    "[markdown]": {
      "editor.defaultFormatter": "yzhang.markdown-all-in-one"
    },
```

### 2. Fazer uma cópia do projeto

```sh
# Clonar o repo
git clone https://github.com/Fatec-Bug-Busters/scrum-academy.git

cd scrum-academy/
```

### 3. Configurar o ambiente virtual

Dentro do diretório do projeto, na pasta raiz, crie um ambiente virtual usando venv.

```sh
# Criar um ambiente virtual
python -m venv venv


# Ativar ambiente virtual
# Windows - git bash
. /venv/Scripts/activate
# Linux
. /venv/bin/activate

# instalar as dependências
pip install -r requirements.txt
```

### 4. Rodar o servidor Flask

```sh
# rodar o projeto localmente
flask run
# abra http://localhost:5000 no navegador
```

Com esses passos, você deve ter tudo pronto para começar a desenvolver.

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
```

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

    !https://user-images.githubusercontent.com/97056108/184449714-61e8ee51-824a-48c1-9436-2dfd67f2c070.png

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
