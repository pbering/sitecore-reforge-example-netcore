# Sitecore Reforge .NET Core Rendering Host example

For more details, see the main repository [Sitecore Reforge](https://github.com/sitecoreops/sitecore-reforge).

## Features

- Develop on Windows, macOS or Linux
- Use the Sitecore CLI on any of the above platforms
- .NET Core 6.0 hot reload just works

## Run

Clone and open on host or in WSL (adjust `--auth` and `--cm` urls accordingly) and then:

1. `dotnet tool restore`
1. `dotnet sitecore login --insecure --cm http://host.docker.internal:47080 --auth http://host.docker.internal:47080 --client-credentials true --allow-write true --client-id "sitecore\admin" --client-secret "b" --trace`
1. `dotnet sitecore ser push --publish`

Run on Docker (Linux):

1. `docker-compose up --build` (hot reload works here as well)

Or if you wish to run on host or in WSL:

1. `export DOTNET_ENVIRONMENT=Development` OR `$env:DOTNET_ENVIRONMENT="Development"` depending on your shell.
1. `dotnet watch --project ./src/ReforgeExample.RenderingHost/`
