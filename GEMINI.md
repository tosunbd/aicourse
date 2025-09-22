# Gemini Project Context: my-app

## Project Overview

This is a TypeScript monorepo project managed with Bun workspaces. The project is structured into two main packages: a client-side application and a server-side application.

*   **`packages/client`**: A React single-page application built with Vite. It serves as the frontend of the project.
*   **`packages/server`**: A backend server built with Express.js.
*   **`bun`**: Used as the package manager and for script execution. It's configured to manage dependencies for the entire monorepo.

## Building and Running

### Root
*   **Install all dependencies**:
    ```bash
    bun install
    ```

### Client (`packages/client`)

*   **Run the development server**:
    ```bash
    bun run packages/client/dev
    ```
*   **Build for production**:
    ```bash
    bun run packages/client/build
    ```
*   **Lint the code**:
    ```bash
    bun run packages/client/lint
    ```
*   **Preview the production build**:
    ```bash
    bun run packages/client/preview
    ```

### Server (`packages/server`)

*   **Start the server**:
    ```bash
    bun run packages/server/start
    ```
*   **Run the server in development mode (with hot-reload)**:
    ```bash
    bun run packages/server/dev
    ```

## Development Conventions

*   **Monorepo Structure**: The project follows a standard monorepo structure with shared dependencies managed by Bun workspaces. All packages are located in the `packages` directory.
*   **TypeScript**: The entire codebase is written in TypeScript, with strict type checking enabled.
*   **React**: The frontend is built with React and Vite, using modern features like JSX and hooks.
*   **Express**: The backend is a simple Express.js server.
*   **Linting**: ESLint is configured for the client-side code to maintain code quality.
