# Dev Container + Vite + Svelte

This project intends to provide a development environment for Svelte applications using Vite and Docker.

## Requirements

- [Docker](https://www.docker.com/)
- [VS Code](https://code.visualstudio.com/)
- [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Usage

### Running dev container
1. Clone this repository
2. Open the project in VS Code.
3. If the Dev Container extension did not suggest to reopen the project in a container, press `F1` and type and select `Dev Containers: Reopen in Container`.
4. The container will be built and the project will be opened in the container. The first time you open the project, the dependencies will be installed. This may take a while.
5. After the container is ready, a post start comand will run the `docker compose up` and the frontend application container will install the dependencies and run `npm run dev`.
6. The application will be available by default at [http://localhost:5173](http://localhost:5173).
7. You can now edit the project files in VS Code and the application will be reloaded automatically.

### Interact with the application container
1. Open a terminal in VS Code.
2. To access the container terminal type `docker exec -it <app-container-id> sh`.
3. You can now interact with the application and run its scripts like test, build and install dependencies.

### Stop de application container
1. The container will stop if the dev script stops
3. To stop the container manually, run `docker container stop <app-container-id>`
2. Execute `docker compose down` will terminate the container. To resume the container, run `docker compose up`.

### Interact with application outside the container
1. You can run the application outside the container by running `npm run dev` in the project root folder.
2. Other scripts like `npm run build` and `npm run test` can be executed outside the container.
3. Dependencies can be installed outside the container by running `npm install`.