# Diretrizes de Contribuição para o Projeto

Para garantir uma colaboração eficaz e eficiente, pedimos que siga estas diretrizes.

## Configurando seu Ambiente de Desenvolvimento

Antes de começar a contribuir, é necessário configurar seu ambiente de desenvolvimento. Aqui estão os passos para a instalação e configuração das principais ferramentas que usaremos no projeto.

- Visual Studio Code
- Git
- Python v3
- GitHub (online)

No Visual Studio Code, utilizaremos algumas extensões para facilitar na organização e desenvolvimento do projeto.

### Editorconfig

> EditorConfig helps maintain consistent coding styles for multiple developers working on the same project across various editors and IDEs. - [https://editorconfig.org/](https://editorconfig.org/)

#### Install EditorConfig

Abra o VS Code Quick Open (`Ctrl+P`), cole o seguinte comando e pressione Enter.

`ext install EditorConfig.EditorConfig`

[Link da extensão no VScode](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

## Contribuindo com o Projeto

### Clonando o Repositório

Para começar a trabalhar no projeto, você primeiro precisa clonar o repositório. Use o seguinte comando no terminal:

```sh
# via SSH
git clone git@github.com:Fatec-Bug-Busters/api.git

# via HTTPS
git clone https://github.com/Fatec-Bug-Busters/api.git
```

### Criando uma Branch

Navegue até o diretório do projeto clonado.
Antes de criar uma nova branch, assegure-se de que está na branch principal e que ela está atualizada com o seguinte comando:

```sh
git checkout master  # "abre" o branch 'master'
git pull origin master # "puxa as mudanças do repositório principal"
```

Crie uma nova branch para sua tarefa:

```sh
git checkout -b [nome-da-sua-branch]
```

### Fazendo Commit das suas Mudanças

Adicione suas mudanças ao stage do Git com `git add .` ou `git add [arquivo]`.
Faça o commit de suas mudanças com uma mensagem clara e concisa que explique o que você fez:

```sh
git commit -m "Uma breve descrição das mudanças"
```

### Enviando suas Mudanças para Revisão

Faça push da sua branch para o repositório remoto:

```sh
git push origin [nome-da-sua-branch]
```

Abra um **Pull Request** no GitHub explicando as mudanças realizadas.

## Boas Práticas

- Certifique-se de seguir as convenções de código e documentação adotadas pelo projeto.
- Teste suas mudanças localmente antes de enviar o Pull Request.
- Participe das discussões no Pull Request e faça as alterações sugeridas pela equipe, se aplicável.

Agradecemos sua contribuição para o nosso projeto! Juntos, podemos construir algo incrível.
