# Rascunho do Produto

## Estrutura dos arquivos para conexão com o Banco de Dados

Cada arquivo conterá funções para conexão com o BD

```
/databases
    __init__.py
    users.py
    iterations.py
    quizzes.py
    exams.py
```

## Fluxos de Dados

### Reconhecimento do usuário

1. Usuário envia o seu e-mail
   1. A aplicação identifica se o usuário possui cadastro
      1. Se sim:
         1. Retorna seu ID, nome e e-mail
      2. Senão
         1. Solicita seu nome
2. O usuário envia o seu nome e e-mail
   1. A aplicação identifica se o usuário possui cadastro
      1. Se sim:
         1. Retorna seu ID, nome e e-mail
      2. Senão
         1. O sistema cadastra o usuário
         2. Cria uma *iteration* para o usuário com valores:
            1. `iterations.is_finished` = `false`
         3. Retorna o seu ID, nome e e-mail

### Usuário abre um Quiz

1. Usuário envia seu ID e o número (`quizzes.index`) do quiz
2. O sistema identifica se o usuário possui uma iteração (`iterations`) não completa (utilizando `iterations.is_finished`)
   1. Se sim, verifica se o usuário já possui o quiz respondido (`quizzes.index` com `iterations.id`)
      1. Se sim:
         1. Retorna as respostas registradas (`quizzes.users_answer`), sua nota (`quizzes.score`) e a data em que foi respondido (`quizzes.created_at`)
      2. Senão
          1. Retorna nada

### Usuário envia uma resposta de Quiz

1. Usuário envia seu ID, o número do quiz (`quizzes.index`), a sua resposta (`quizzes.users_answer`), e a sua nota (`quizzes.score`)
2. O sistema identifica se o usuário possui uma iteração (`iterations`) não completa (utilizando `iterations.is_finished`)
   1. Se sim
      1. O sistema registra a resposta do quiz em `quizzes`
         1. Retorna nada
   2. Se não
      1. O sistema retorna erro

### Usuário envia uma resposta de exame

1. Usuário envia seu ID, a sua resposta (`exams.users_answer`), sua nota (`exams.score`)
2. O sistema identifica se o usuário possui uma iteração (`iterations`) não completa (utilizando `iterations.is_finished`)
   1. Se sim
      1. O sistema registra a resposta do exame
      2. Calcula a média das notas do usuário
      3. Registra a média das notas (`iterations.total_score`), a data de conclusão (`iterations.finished_at`), a iteração como conluída (`iterations.is_finished` = `true`)
      4. O sistema pede a avaliação/review do usuário
      5. O usuário envia o seu ID, a sua nota de avaliação (`iterations.review_score`) e o seu comentário de avaliação (`iterations.comment`)
      6. O sistema registra a avaliação em `iterations`
      7. Retorna a pontuação total (`iterations.total_score`)
      8. Verifica se usuário foi aprovado nas avaliações:
         1. Se sim
            1. O sistema permite a impressão do certificado de conclusão
         2. Senão
            1. Mostra mensagem ao usuário para estudar e refazer as avaliações
   2. Se não
      1. O sistema retorna erro

### Usuário abre a página de resultados de exames

1. O sistema retorna todas as linhas da entidade `iterations` contendo
   1. os nomes dos usuários (`users`),
   2. os e-mails dos usuários (`users`),
   3. as suas respectivas notas (`quizzes.score`) dos quizzes responsdidos,
   4. as notas dos exames (`exams.score`),
   5. a data de finalização, se houver, das iterações (`iterations.is_finished`)
   6. a média das avaliações (`iterations.total_score`)

### Usuário abre as avaliações/review de um usuário

1. Usuário envia o ID do usuário
2. O sistema retorna as review de todas as iterações do usuário (`iterations.review_score` e `iterations.review_comment`), a data de finalização da iteração (`iterations.finished_at`), a nota final (`iterations.total_score`), e o nome do usuário (`users.name`)

### Usuário abre a página de reviews

*Add ao Sprint Backlog*.

1. O sistema retorna
   1. todas as reviews feitas (`iterations.review_score` e `iterations.review_comment`),
   2. o nome do usuário (`users.name`),
   3. o e-mail do usuário (`users.email`),
   4. a data de conclusão da iteração (`iterations.finished_at`)
   5. a média das notas (`iterations.total_score`)

---

## Rascunho do produto

- Breadcrumbs e botões **próximo** e **anterior** para navegação no conteúdo
- Ter uma seção para o **Quiz** que irá validar o conhecimento adquirido pelo usuário
- Exames no final de todo o contéudo onde tirando a nota mínima, a pessoa receberá o badge
- Mascote para o nosso curso:
  - Com esse mascote nós podemos conversar com os usuários em um tom de formá-los em mula
  - Podemos implementar conceitos de gamificação onde nossos usuários irão  ganhar títulos/badges ao terminar certas seções do curso. Por exemplo, ao terminar o Cap 1 ele ganha um título/badge **Mula Noobie**. Ao teeminr todo o curso ele ganha o título de **Mula Buster** (remetendo a Bug Busters). Isso vai mostrar inclusive que nós pensamos na jornada do usuário tanto falado em UX.
    - Ao começar a ler a introdução o usuário irá ganhar um badge Jornada da Mula Ágil por ter começado a sua jornada Agile
    - Na Introdução da página principal, na seção que explica do que se trata esse site, podemos brincar dizendo que somos uma Academia de Scrum para Mulas onde temos o objetivo de transformá-las em experiente Scrum Busters (brincando com o nosso nome e os papéis de Scrum como Scrum Team, Scrum Master)
    - E usamos um método chamado Mule-Driven Development (MDD) no ensino das técnicas avançadas de Scrum, uma metodologia ágil....
      - Mule-Driven Development (MDD) - um jogo de palavras com "Test-Driven Development" e "Behavior-Driven Development", focando no desenvolvimento orientado por "mulas"
