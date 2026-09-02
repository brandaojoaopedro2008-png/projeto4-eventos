# Sistema de Inscricao em Eventos

## Como rodar

### Banco de dados (Postgres via Docker)
```
cd backend
docker compose up -d
```

### Backend (Spring Boot + Gradle + Java 25)
```
cd backend
./gradlew bootRun
```
API em `http://localhost:8083`.

### Frontend (React + Vite)
```
cd frontend
npm install
npm run dev
```
Frontend em `http://localhost:5176`.

## Atividade

Cadastrem um evento, inscrevam alguns participantes ate perto do limite de vagas,
cancelem uma inscricao e tentem inscrever de novo. Reparem no numero de "vagas
restantes" mostrado nas telas.
