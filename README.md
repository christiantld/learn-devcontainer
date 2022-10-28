# Dev Container + Vite + Svelte

This project intends to provide a development environment for Svelte applications using Vite and Docker.

## Requirements

- [Docker](https://www.docker.com/)
- [VS Code](https://code.visualstudio.com/)
- [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Usage

1. Clone this repository
2. Open the project in VS Code.
3. If the Dev Container extension did not suggest to reopen the project in a container, press `F1` and type and select `Dev Containers: Reopen in Container`.
4. The container will be built and the project will be opened in the container. he first time you open the project, the dependencies will be installed. This may take a while.
5. After the container is ready, you can start the development server by running `npm run dev` in the terminal. The application will be available at [http://localhost:5173](http://localhost:5173).
6. You can now edit the project files in VS Code and the application will be reloaded automatically.
7. To stop the application, press `F1` and type and select `Docker Compose: Down` or run `docker compose down` in the terminal.
