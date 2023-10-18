# About

DevContainers in VSCode allows us to set up local containers to run workloads and test them out locally without having to deploy to dev/sandbox environments in the cloud.

# Config

Here's a sample of the devcontainers.json content. This config file can do the following examples:

- Set container name
- Direct VSCode to start DevContainer
- Use the DockerFile or Docker-Compose yml to define the build
- Expost Ports from within the container
- Set Runtime Arguements
- Define local volume mounts if needed
- Define custom env variables to be set within the container
- Define custom commands to run when container is created
- Define custom commands to run when container is started
- Define custom commands to run when container is connected to
- Define behavior when VSCode session is closed

```json
// For format details, see https://aka.ms/devcontainer.json. For config options, see the
// README at: https://github.com/devcontainers/templates/tree/main/src/docker-existing-dockerfile
{
  "name": "TimeTracker-API",
  "build": {
    // Sets the run context to one level up instead of the .devcontainer folder.
    "context": "..",
    // Update the 'dockerFile' property if you aren't using the standard 'Dockerfile' filename.
    "dockerfile": "../Dockerfile"
  },
  // Expose port using appPort
  "appPort": [3300],
  "runArgs": ["--name", "TimeTracker-API"],
  "mounts": [
    "source=${localWorkspaceFolder},target=/api,type=bind,consistency=cached"
  ],
  "containerEnv": {
    "AZURE_CLIENT_ID": "968b3c9c-4296-4746-a71d-161ff7dbd4df",
    "AZURE_CLIENT_SECRET": "rB-8Q~z4tZ~Qk44FEYe8NwcYF6GKJnD~AFLL-ccz",
    "AZURE_TENANT_ID": "2e319086-9a26-46a3-865f-615bed576786",
    "PORTALADDRESS": "http://localhost:3000"
  },
  "onCreateCommand": {
    "git-name": [
      "git",
      "config",
      "--global",
      "user.name",
      "Siddharth Shanbhogue"
    ],
    "git-mail": [
      "git",
      "config",
      "--global",
      "user.email",
      "siddharth.shanbhogue@providence.org"
    ]
  },
  // Features to add to the dev container. More info: https://containers.dev/features.
  // "features": {},
  // Use 'forwardPorts' to make a list of ports inside the container available locally.
  // "forwardPorts": [3300]
  // Uncomment the next line to run commands after the container is created.
  "postCreateCommand": "nodemon ./server.js",
  "postStartCommand": "nodemon ./server.js",
  "shutdownAction": "stopContainer"
  // Configure tool-specific properties.
  // "customizations": {},
  // Uncomment to connect as an existing user other than the container default. More info: https://aka.ms/dev-containers-non-root.
  // "remoteUser": "devcontainer"
}
```
