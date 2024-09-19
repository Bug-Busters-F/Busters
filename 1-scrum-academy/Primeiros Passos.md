# Primeiros Passos

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
