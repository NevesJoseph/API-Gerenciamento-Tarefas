# Guia de Instalação: Ruby on Rails

## 💻 Instalação do Ruby e Rails no Windows

### 1. Instalando o Ruby Installer

1. Acesse [RubyInstaller](https://rubyinstaller.org/downloads/)
2. Baixe a versão Ruby+Devkit recomendada (WITH DEVKIT - x64)
3. Execute o instalador e siga os passos:
   - Marque todas as opções durante a instalação
   - Escolha a opção de adicionar Ruby ao PATH
   - No final da instalação, mantenha marcada a opção "ridk install"
4. Após a instalação, abra o terminal e execute:
```bash
ruby -v
```
Se aparecer a versão do Ruby, a instalação foi bem-sucedida.

### 2. Instalando o Rails

1. Abra o terminal e execute:
```bash
gem install rails
```

2. Verifique a instalação:
```bash
rails -v
```

### 3. Instalando o SQLite3

1. Instale via Chocolatey (recomendado):
```powershell
# Instale o Chocolatey primeiro se não tiver (PowerShell como Administrador)
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

# Depois instale o SQLite
choco install sqlite
```

## 🍎 Instalação no macOS

### 1. Instalando o Homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Instalando o Ruby
```bash
brew install rbenv ruby-build
rbenv init
rbenv install 3.0.0  # ou versão mais recente
rbenv global 3.0.0
```

### 3. Instalando o Rails
```bash
gem install rails
```

### 4. Instalando o SQLite3
```bash
brew install sqlite3
```

## 🐧 Instalação no Linux (Ubuntu/Debian)

### 1. Instalando o Ruby
```bash
sudo apt-get update
sudo apt-get install ruby-full
```

### 2. Instalando o Rails
```bash
gem install rails
```

### 3. Instalando o SQLite3
```bash
sudo apt-get install sqlite3 libsqlite3-dev
```

## 🚀 Criando e Inicializando um Novo Projeto Rails

### 1. Criar novo projeto
```bash
rails new nome-do-projeto --api
```
O flag `--api` cria uma aplicação Rails otimizada para API.

### 2. Entrar no diretório do projeto
```bash
cd nome-do-projeto
```

### 3. Instalar dependências
```bash
bundle install
```

### 4. Criar banco de dados
```bash
rails db:create
```

### 5. Executar migrações (se houver)
```bash
rails db:migrate
```

### 6. Iniciar o servidor Rails
```bash
rails server
# ou forma abreviada
rails s
```
O servidor iniciará em `http://localhost:3000`

## ⚠️ Problemas Comuns e Soluções

### 1. Erro de Versão do Ruby
Se encontrar erro de versão incompatível:
```bash
rbenv install [versão_necessária]
rbenv global [versão_necessária]
```

### 2. Erro de Permissão no Linux/macOS
```bash
sudo chown -R $USER:$USER .
```

### 3. Erro de SQLite3
Se encontrar erro relacionado ao SQLite:
```bash
# Ubuntu/Debian
sudo apt-get install libsqlite3-dev

# macOS
brew install sqlite3

# Windows
choco install sqlite
```

### 4. Erro de JavaScript Runtime
```bash
# Ubuntu/Debian
sudo apt-get install nodejs

# macOS
brew install node

# Windows
choco install nodejs
```

## 📝 Comandos Rails Úteis

```bash
# Criar um novo modelo
rails generate model Task title:string description:text completed:boolean

# Criar um novo controller
rails generate controller Api::V1::Tasks

# Criar uma nova migration
rails generate migration AddDescriptionToTasks description:text

# Reverter última migração
rails db:rollback

# Abrir console Rails
rails console

# Verificar rotas disponíveis
rails routes
```

## 🔍 Verificando a Instalação

Para garantir que tudo está funcionando corretamente:

1. Verifique as versões instaladas:
```bash
ruby -v
rails -v
sqlite3 --version
```

2. Crie um projeto de teste:
```bash
rails new teste --api
cd teste
rails server
```

3. Acesse `http://localhost:3000` no navegador. Você deverá ver a página padrão do Rails.

## 📚 Recursos Adicionais

- [Ruby Documentation](https://www.ruby-lang.org/en/documentation/)
- [Ruby on Rails Guides](https://guides.rubyonrails.org/)
- [Ruby Gems](https://rubygems.org/)
- [Rails API Documentation](https://api.rubyonrails.org/)

## ❓ Suporte

Se encontrar problemas durante a instalação:

1. Verifique as mensagens de erro no terminal
2. Consulte a [documentação oficial do Rails](https://guides.rubyonrails.org/)
3. Procure por soluções no [Stack Overflow](https://stackoverflow.com/)
4. Verifique as issues no [GitHub do Rails](https://github.com/rails/rails/issues)