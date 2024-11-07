# API de Gerenciamento de Tarefas (Tasks)

Uma API RESTful desenvolvida com Ruby on Rails para gerenciamento de tarefas. Esta API permite criar, listar, atualizar e deletar tarefas (CRUD completo).

## 🚀 Tecnologias Utilizadas

- Ruby 3.0.0
- Rails 7.0.0
- SQLite3

## 📋 Pré-requisitos

Para executar este projeto, você precisará ter instalado em sua máquina:

- Ruby (versão 3.0.0 ou superior)
- Rails (versão 7.0.0 ou superior)
- SQLite3

## 💻 Instalação

1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```

2. Entre no diretório do projeto
```bash
cd nome-do-repositorio
```

3. Instale as dependências
```bash
bundle install
```

4. Crie o banco de dados e execute as migrations
```bash
rails db:create db:migrate
```

5. Inicie o servidor
```bash
rails server
```

O servidor iniciará na porta 3000 - acesse `http://localhost:3000`

## 🔥 Endpoints da API

### Listar todas as tarefas
```http
GET /api/v1/tasks
```

### Buscar uma tarefa específica
```http
GET /api/v1/tasks/:id
```

### Criar uma nova tarefa
```http
POST /api/v1/tasks
```
Corpo da requisição:
```json
{
  "task": {
    "title": "Nova Tarefa",
    "description": "Descrição da tarefa",
    "completed": false
  }
}
```

### Atualizar uma tarefa
```http
PATCH/PUT /api/v1/tasks/:id
```
Corpo da requisição:
```json
{
  "task": {
    "title": "Tarefa Atualizada",
    "description": "Descrição atualizada",
    "completed": true
  }
}
```

### Deletar uma tarefa
```http
DELETE /api/v1/tasks/:id
```

## 📦 Estrutura do Projeto

```
app/
├── controllers/
│   └── api/
│       └── v1/
│           └── tasks_controller.rb
├── models/
│   └── task.rb
└── config/
    └── routes.rb
```

## 🎯 Exemplos de Uso

### Criando uma nova tarefa
```bash
curl -X POST http://localhost:3000/api/v1/tasks \
  -H "Content-Type: application/json" \
  -d '{
    "task": {
      "title": "Estudar Ruby on Rails",
      "description": "Aprender sobre APIs RESTful",
      "completed": false
    }
  }'
```

### Listando todas as tarefas
```bash
curl http://localhost:3000/api/v1/tasks
```

### Atualizando uma tarefa
```bash
curl -X PATCH http://localhost:3000/api/v1/tasks/1 \
  -H "Content-Type: application/json" \
  -d '{
    "task": {
      "completed": true
    }
  }'
```

## 📝 Estrutura do Banco de Dados

### Tabela: tasks
| Campo | Tipo | Descrição |
|-------|------|-----------|
| id | Integer | Identificador único da tarefa |
| title | String | Título da tarefa |
| description | Text | Descrição detalhada da tarefa |
| completed | Boolean | Status de conclusão da tarefa |
| created_at | DateTime | Data de criação do registro |
| updated_at | DateTime | Data da última atualização |

## 🔄 Status das Respostas

- 200: Sucesso
- 201: Criado com sucesso
- 204: Sem conteúdo
- 404: Não encontrado
- 422: Entidade não processável

## 💡 Melhorias Futuras

- [ ] Adicionar autenticação de usuários
- [ ] Implementar paginação
- [ ] Adicionar filtros de busca
- [ ] Implementar testes automatizados
- [ ] Adicionar documentação com Swagger

## 👨‍💻 Como Contribuir

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Faça commit das suas alterações (`git commit -m 'Add some AmazingFeature'`)
4. Faça push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT - veja o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

## ✒️ Autor

* **Joseph Neves** - *Desenvolvedor* - (https://github.com/NevesJoseph)

## 🎁 Expressões de Gratidão

* Compartilhe este projeto com outros desenvolvedores 📢

---
