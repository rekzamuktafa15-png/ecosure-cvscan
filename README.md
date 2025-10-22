ECOSURE — Fullstack CV Analyzer (Next.js + Express + PostgreSQL + OpenAI)

This scaffold is production-ready and includes:
- Frontend (Next.js) in /frontend
- Backend (Express + Prisma) in /backend
- PostgreSQL service and docker-compose for local deployment
- OpenAI integration (server-side)

Quick start (docker-compose):
1. Copy .env files and fill secrets:
   - backend/.env (see .env.example)
   - frontend/.env (see .env.example)
2. Run:
   docker-compose up --build
3. In another shell run Prisma push to create schema:
   docker exec -it <backend-container> npx prisma db push
4. Create a user via POST /api/auth/register
5. Use the frontend at http://localhost:3000

Security:
- Set strong JWT_SECRET
- Configure OPENAI_API_KEY on the backend
- For production, use S3 for file storage and HTTPS
