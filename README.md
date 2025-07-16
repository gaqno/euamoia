# Euamoia

Full-stack monorepo with React frontend and NestJS backend, using Supabase for authentication and database.

## Structure

- `euamoia_front/` - React frontend (submodule)
- `euamoia_back/` - NestJS backend (submodule)

## Development

1. Clone the repository with submodules:
```bash
git clone --recursive git@github.com:gaqno/euamoia.git
cd euamoia
```

2. Create `.env` file with required variables:
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
docker-compose up -d
```

## Architecture

- Frontend: React + Vite
- Backend: NestJS
- Database: Supabase (PostgreSQL)
- Cache: Redis
- Authentication: Supabase Auth
- Storage: Supabase Storage
- Realtime: Supabase Realtime 