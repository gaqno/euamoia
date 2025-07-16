# Euamoia

Full-stack monorepo with React frontend and NestJS backend, using Supabase for authentication and database.

## Project Structure

This repository is organized as a monorepo using Git submodules:

- `euamoia_front/` - React frontend with Vite
- `euamoia_back/` - NestJS backend
- Docker services for development environment

## Prerequisites

- Node.js 18+
- Docker and Docker Compose
- Git

## Getting Started

1. Clone the repository with submodules:
   ```bash
   git clone --recursive git@github.com:gaqno/euamoia.git
   cd euamoia
   ```

2. Create a `.env` file with the required environment variables:
   ```bash
   POSTGRES_PASSWORD=your_password
   JWT_SECRET=your_jwt_secret
   ANON_KEY=your_anon_key
   SERVICE_ROLE_KEY=your_service_role_key
   SITE_URL=http://localhost:3000
   SUPABASE_URL=your_supabase_url
   SUPABASE_ANON_KEY=your_supabase_anon_key
   OPENAI_API_KEY=your_openai_key  # Optional
   ```

3. Start the development environment:
   ```bash
   docker-compose up
   ```

The services will be available at:
- Frontend: http://localhost:3000
- Backend: http://localhost:3001
- Supabase Studio: http://localhost:8000
- Redis: localhost:6379
- PostgreSQL: localhost:5432

## Development Guidelines

### React Components

1. All components must follow the folder structure:
   ```
   ComponentName/
   ├── index.tsx         # Only template/JSX
   ├── hooks/
   │   └── useComponent.ts  # All logic
   └── types.ts          # Types & interfaces
   ```

2. Rules:
   - No logic in component files (move to hooks)
   - Prefix interfaces with `I`
   - Add `displayName` to every component
   - Use `zod` for form validation
   - Use `react-hook-form` for forms
   - Use `react-query` for API calls
   - Use `axios` for HTTP requests

### Git Workflow

1. Update submodules:
   ```bash
   git submodule update --init --recursive
   ```

2. Work on features in submodule repositories
3. Commit and push changes to submodule repos
4. Update main repo to track latest submodule versions

## License

MIT 