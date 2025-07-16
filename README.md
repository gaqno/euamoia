# 🌟 Euamoia

Monorepo full-stack com frontend React e backend NestJS, utilizando Supabase para autenticação e banco de dados.

## 🏗️ Estrutura do Projeto

Este repositório é organizado como um monorepo usando submódulos Git:

- 📱 `euamoia_front/` - Frontend React com Vite
- ⚙️ `euamoia_back/` - Backend NestJS
- 🐳 Docker para ambiente de desenvolvimento

## 📋 Pré-requisitos

- 📦 Node.js 18+
- 🐳 Docker e Docker Compose
- 🔄 Git

## 🚀 Como Começar

1. Clone o repositório com submódulos:
   ```bash
   git clone --recursive git@github.com:gaqno/euamoia.git
   cd euamoia
   ```

2. Crie um arquivo `.env` com as variáveis de ambiente necessárias:
   ```bash
   POSTGRES_PASSWORD=sua_senha
   JWT_SECRET=seu_jwt_secret
   ANON_KEY=sua_anon_key
   SERVICE_ROLE_KEY=sua_service_role_key
   SITE_URL=http://localhost:3000
   SUPABASE_URL=sua_supabase_url
   SUPABASE_ANON_KEY=sua_supabase_anon_key
   OPENAI_API_KEY=sua_openai_key  # Opcional
   ```

3. Inicie o ambiente de desenvolvimento:
   ```bash
   docker-compose up
   ```

Os serviços estarão disponíveis em:
- 🌐 Frontend: http://localhost:3000
- ⚡ Backend: http://localhost:3001
- 🛠️ Supabase Studio: http://localhost:8000
- 📦 Redis: localhost:6379
- 🗄️ PostgreSQL: localhost:5432

## 📚 Guia de Desenvolvimento

### 🎨 Componentes React

1. Todos os componentes devem seguir a estrutura de pastas:
   ```
   ComponentName/
   ├── index.tsx         # Apenas template/JSX
   ├── hooks/
   │   └── useComponent.ts  # Toda a lógica
   └── types.ts          # Types & interfaces
   ```

2. Regras:
   - ❌ Nenhuma lógica nos arquivos de componentes (mova para hooks)
   - 🏷️ Prefixe interfaces com `I`
   - 📝 Adicione `displayName` em todos os componentes
   - ✅ Use `zod` para validação de formulários
   - 📋 Use `react-hook-form` para formulários
   - 🔄 Use `react-query` para chamadas API
   - 🌐 Use `axios` para requisições HTTP

### 🔄 Fluxo Git

1. Atualize os submódulos:
   ```bash
   git submodule update --init --recursive
   ```

2. Trabalhe em features nos repositórios dos submódulos
3. Faça commit e push das alterações nos repos dos submódulos
4. Atualize o repo principal para acompanhar as últimas versões dos submódulos

### 🧪 Testes e Qualidade

- 🔍 Execute os testes antes de cada commit
- 📊 Mantenha a cobertura de testes acima de 80%
- 🎯 Siga as regras do ESLint e Prettier
- 📝 Documente todas as funções e componentes

### 🏗️ Arquitetura

#### Frontend
- 🎨 Styled Components para estilização
- 📱 Design responsivo mobile-first
- 🔐 Autenticação via Supabase
- 🌐 Chamadas API centralizadas
- 📦 Estado global com React Query

#### Backend
- 🏗️ Arquitetura limpa
- 🔐 Autenticação JWT
- 📦 Cache com Redis
- 🗄️ Banco de dados PostgreSQL via Supabase
- 📝 Documentação Swagger

## 🤝 Contribuindo

1. 🔀 Faça um fork do projeto
2. 🌿 Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. 📝 Faça commit das alterações (`git commit -m 'feat: Add AmazingFeature'`)
4. 🚀 Faça push para a branch (`git push origin feature/AmazingFeature`)
5. 🔍 Abra um Pull Request

## 📄 Licença

MIT

## 👥 Time

- [@gaqno](https://github.com/gaqno) - Desenvolvedor Full Stack

## 📞 Suporte

Para suporte, envie um email para [seu-email@exemplo.com] ou abra uma issue no GitHub. 