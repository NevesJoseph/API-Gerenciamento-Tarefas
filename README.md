# API de Gerenciamento de Tarefas (Tasks)

Uma API RESTful desenvolvida com Ruby on Rails para gerenciamento de tarefas. Esta API permite criar, listar, atualizar e deletar tarefas (CRUD completo), com diversas melhorias implementadas.

## 🚀 Tecnologias Utilizadas

- Ruby 3.0.0
- Rails 7.0.0
- SQLite3
- Devise (Autenticação de Usuários)
- Kaminari (Paginação)
- RSpec (Testes Automatizados)
- Swagger UI Rails (Documentação da API)

## 📋 Pré-requisitos

Para executar este projeto, você precisará ter instalado em sua máquina:

- Ruby (versão 3.0.0 ou superior)
- Rails (versão 7.0.0 ou superior)
- SQLite3

## 💻 Instalação e Configuração

Siga as instruções de [Instalação do Ruby e Rails](https://github.com/NevesJoseph/ToDoList-Ruby/blob/main/Install-Ruby-Rails.md) para configurar o ambiente de desenvolvimento.

## 🔥 Endpoints da API

### Autenticação
- **POST** `/api/v1/users/sign_in`: Realizar login do usuário
- **POST** `/api/v1/users/sign_out`: Realizar logout do usuário

### Tarefas
- **GET** `/api/v1/tasks`: Listar todas as tarefas do usuário autenticado
- **GET** `/api/v1/tasks/:id`: Buscar uma tarefa específica
- **POST** `/api/v1/tasks`: Criar uma nova tarefa
- **PATCH/PUT** `/api/v1/tasks/:id`: Atualizar uma tarefa
- **DELETE** `/api/v1/tasks/:id`: Deletar uma tarefa

### Filtros e Paginação
- Filtrar tarefas por `title` e `completed` status
- Paginar a listagem de tarefas, retornando 10 itens por página

## 🎯 Documentação da API

A documentação completa da API, incluindo exemplos de uso, está disponível em `/api-docs` após iniciar o servidor.

## 🧪 Testes Automatizados

Foram implementados testes unitários usando RSpec para validar o comportamento dos endpoints da API.

Para executar os testes:
```bash
rspec spec/controllers/api/v1/tasks_controller_spec.rb
```

## 🚀 Iniciando o Projeto

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

O servidor iniciará na porta 3000 - acesse `http://localhost:3000/api-docs` para visualizar a documentação da API.

## 🔄 Principais Recursos Implementados

- **Autenticação de Usuários**: Usando a gem Devise, a API requer autenticação para acessar os endpoints.
- **Paginação**: A listagem de tarefas é paginada, retornando 10 itens por página.
- **Filtros de Busca**: É possível filtrar as tarefas por título e status de conclusão.
- **Testes Automatizados**: Foram implementados testes unitários para validar o comportamento da API.
- **Documentação com Swagger**: A documentação da API é gerada automaticamente usando a gem Swagger UI Rails.

## 🔍 Melhorias Futuras

- [ ] Implementar atualização em lote de tarefas
- [ ] Adicionar suporte a upload de arquivos nas tarefas
- [ ] Implementar autenticação via OAuth
- [ ] Integrar com sistema de notificações

## 👨‍💻 Como Contribuir

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Faça commit das suas alterações (`git commit -m 'Add some AmazingFeature'`)
4. Faça push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT - veja o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

## ✒️ Autor

* **Joseph Neves** - *Desenvolvedor* - [NevesJoseph](https://github.com/NevesJoseph)

---
