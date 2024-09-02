# DevContainer Base template

This repository contains a DevContainer base configuration for a development environment. It provides a consistent, reproducible setup for developers working on projects that involve these technologies.

## Features

- Common development utilities
- Pre-configured VS Code settings and extensions
- Zsh with Oh My Zsh
- Neovim configuration

## How It Works

The DevContainer is defined by several configuration files:

1. `.devcontainer/devcontainer.json`: The main configuration file that specifies:
   - Base image and build instructions
   - Ports to forward
   - Features to install
   - VS Code extensions and settings
   - Commands to run on container creation

2. `.devcontainer/Dockerfile`: Defines the custom Docker image.

3. `.devcontainer/on-create.sh`: A script that runs when the container is created, installing additional packages and configuring git.

4. `.devcontainer/post-create.sh`: A script that runs after the container is created, setting up Neovim configuration.

## Usage

1. Ensure you have Docker and VS Code with the Remote - Containers extension installed.
2. Clone this repository.
3. Open the repository in VS Code.
4. When prompted, click "Reopen in Container" or run the "Remote-Containers: Reopen in Container" command.
5. VS Code will build the Docker image and start the container. This may take a few minutes the first time.
6. Once the container is running, you'll have a fully configured development environment for Node.js and Python.

## Customization

You can customize the DevContainer by modifying the configuration files:

- Add or remove VS Code extensions in `devcontainer.json`
- Modify container features or settings in `devcontainer.json`
- Add additional software or configuration in the `Dockerfile`
- Modify the setup scripts (`on-create.sh` and `post-create.sh`) to add your own initialization steps

## Benefits

- Consistent development environment across team members
- Easy onboarding for new developers
- Isolation from the host system

## License

Copyright © 2024 [tooniez](https://github.com/tooniez). <br />
This project is [MIT](https://github.com/tooniez/devcontainer-base/blob/main/LICENSE) licensed.
