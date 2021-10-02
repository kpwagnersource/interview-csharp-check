# Interview Check (C#)
C# project for verifying interview setup

## Open in dev container

1. Clone this repository
2. Open the directory in VS Code
3. Click the "Open a Remote Window" icon on the bottom-left corner of VS Code
4. Select "Reopen in Container"

A development container image will be built according to the configuration in the `.devcontainer` folder. _Nothing is installed on your host OS_. Everything can be cleaned up by deleting the development container and corresponding image.

## Run project

```
dotnet run
```

## Deleting development container and container image

**Assuming you have cloned the repository into a `interview-check-csharp` directory,** you can delete the container and corresponding image by running the following command:

**macOS/Linux:**

```
docker ps -a | grep 'vsc-interview-check-csharp' | awk '{print $1}' | xargs docker rm && \
docker images | grep 'vsc-interview-check-csharp' | awk '{print $1}' | xargs docker image rm
```

**Windows PowerShell:**

```
(docker rm (docker ps -a --format '{{.ID}} {{.Image}}' | Select-String 'vsc-interview-check-csharp').ToString().Split()[0]) -and
(docker image rm ( (docker images | Select-String 'vsc-interview-check-csharp').ToString().Split()[0]))
```
