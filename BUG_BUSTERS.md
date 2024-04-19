# Bug Busters - Scrum Team

Garantir uma colaboração eficaz e eficiente entre a equipe.

## Integrantes

| Função |Nome | GitHub |
| :----: | :-- | -----: |
| Product Owner |   Diego Castilho        |      [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/DigoCast)              |
| Scrum Master  | Wesley Gonçalves |       [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/WesleyGoncalves)     |
| Team Member   | Davi Miyake             |          [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/DaviMBDev)        |
| Team Member   | Gabriel Viell           |          [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/GabrielViellCastilho)        |
| Team Member   | Vinicius Elias             |          [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/ViniElias)        |
| Team Member   | Allan Couto             |          [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/allancouto)        |

![Bug Busters](./assets/bug-busters-logo-black.jpg)

## Como contribuir

### Fazer uma cópia do repo

```sh
# Clonar o repo
git clone https://github.com/Fatec-Bug-Busters/scrum-academy.git

cd scrum-academy/
```

### Branches

```sh
# Ver branch ativo
git branch
# irá aparecer os branches existentes. O branch ativo é aquele que tiver marcado com * e estiver em verde (no Git bash).

# Troca para o branch 'dev'
git checkout dev
```

### Executar localmente

```sh
# Ativar ambiente virtual
# Windows - git bash
. /venv/Scripts/activate
# Linux
. /venv/bin/activate

# instalar as dependências
cd src/
pip install -r requirements.txt

# rodar o projeto localmente
flask run --debug
```

### Fazer Commit

Envie sempre para o branch `dev`. Ver [Branches](#branches)

```sh
# Garanta que você está na pasta do projeto
pwd
# resposta esperada:  ......../scrum-academy

# Add as modificações
git add .     # add todas as modificações para serem comitadas
# ou
git add src/file1 src/file2  # add file1 e file2 presentes em 'src' para serem comitados

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

### Enviar suas modificações

Envie sempre para o branch `dev`. Ver [Branches](#branches)

Há dois repos com os quais estamos trabalhando:

1. O repo remoto (no GitHub) que centraliza as modificações que todos fazem. Funciona como um servidor
2. O repo local (na sua máquina) que é uma cópia do repo remoto.

```sh
# Garanta que você está no branch 'dev'
# ver Branches

# Atualiza o repo local - puxa do repo remoto os últimos commits
git pull
# se aparecer uma mensagem sobre conflito, grita.

# Envia seus novos commits para o repo remoto
git push
```

### Resumo

1. Ter uma cópia do repositório do projeto na sua máquina
2. Faz as suas modificações
3. Navegar para o diretório raiz do projeto
4. Add modificações ao stage
5. Commit essas modificações
6. Git pull para trazer modificações do repo remoto
7. Git push seus commits para o repo remoto

## Ferramentas que iremos utilizar

- Visual Studio Code
- Git
- GitHub
- Python v3
- Figma
- Discord

### Visual Studio Code

No Visual Studio Code, utilizaremos algumas extensões para facilitar na organização e desenvolvimento do projeto em equipe. São elas:

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

#### Instalação das extensões no vscode

Abra o terminal no vscode e cole os seguintes comandos de instalação das extensões:

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

### Configurar a extensão Black Formatter

Apertar `Ctrl + Shift + P` no vscode, digitar "User Settings JSON" e apertar em `Preferences: Open User Settings (JSON)`

Digita no início do arquivo após `{`:

```json
"python.formatting.provider": "black",
"editor.formatOnSave": true,
```

## Code Styling

### Python

[Python official guidelines - PEP8](https://peps.python.org/pep-0008/).

Algumas extensões indicadas lá em cima auxiliam na formatação do código.

Alguns atalhos do vscode:

- `Ctrl + Shift + M`: abre a aba do relatório de Problemas
- `Shift + alt + O`|`Ctrl + Shift + I` - formata o código

## Markdown

Veja o [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/).

Instale as extensões de Markdown para facilitar o uso no [vscode - *clique aqui*](#visual-studio-code).
