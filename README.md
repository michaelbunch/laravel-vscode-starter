# Laravel VSCode Starter Project

This is starter project for Laravel development using Visual Studio Code's Remote Container development.

## Requirements

This project is intended to need minimal environment setup. Meaning the host machine doesn't need  get a developer started. Any software needed by the developer will be installed in the container, including VSCode extensions.

- [Visual Studio Code](https://code.visualstudio.com/) with [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension installed.
- [Docker Desktop](https://www.docker.com/products/docker-desktop)


**Optional**

- Git *for pulling this repository*
- SSH *for pushing this repository via Git*

## Getting Started

To start using this project, following these steps:

1. Clone this repository to your system.
2. Open the project folder in VSCode.
3. In VSCode press `command+shift+p` and type "Open in Container" and press `enter`.

The project containers will build and you will be up and running in a jiffy.

## How It Works

VSCode has an extension call "Remote - Containers" that allows a user to open their workspace within a Docker container. Once inside the container all VSCode will treat the container environment as if it is the host machine. This means extensions like Git, terminal, etc. all run in the container, rather than the host. 

### `.devcontainer.json`

To configure the "Remote - Containers" extension we use a `.devcontainer.json` file that defines how to run the containers (docker-compose), the container to load as the workspace, VSCode settings and extensions specific to the project. For more information on configuring this extension read the article [Developing inside a Container](https://code.visualstudio.com/docs/remote/containers).

