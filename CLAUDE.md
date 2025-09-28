# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Structure

This is a Bun-based TypeScript monorepo with two main packages:

- **packages/client**: React + Vite frontend application
- **packages/server**: Express.js backend server with OpenAI integration

## Commands

### Installation

```bash
bun install  # Install all dependencies for the monorepo
```

### Development

**Client (Frontend)**:

```bash
cd packages/client
bun run dev     # Start Vite dev server with hot-reload
bun run build   # Build for production
bun run lint    # Run ESLint
bun run preview # Preview production build
```

**Server (Backend)**:

```bash
cd packages/server
bun run dev   # Start server with hot-reload (uses --watch)
bun run start # Start server normally
```

### Running from root

```bash
bun run packages/client/dev   # Run client dev server
bun run packages/server/dev   # Run server in dev mode
```

## Architecture

### Backend (packages/server)

- Express.js server running on port 3000 (or PORT env variable)
- Main entry: `index.ts`
- Uses dotenv for environment variables (OPENAI_API_KEY)
- Routes:
   - GET `/` - Basic hello world
   - GET `/api/hello` - JSON API endpoint

### Frontend (packages/client)

- React 19 with TypeScript
- Vite for build tooling
- Standard React app structure in `src/`
- Entry point: `src/main.tsx`
- Main component: `src/App.tsx`

## Key Technologies

- Runtime: Bun (fast JavaScript/TypeScript runtime)
- Package management: Bun workspaces
- Frontend: React 19, Vite, TypeScript
- Backend: Express 5, TypeScript
- Linting: ESLint (client only)
