---
title: Develop with Docker
description: Overview of developer resources
keywords: developer, developing, apps, api, sdk
---
This page lists resources for application developers using Docker.

## Develop new apps on Docker

If you're just getting started developing a brand new app on Docker, check out these resources to understand some of the most common patterns for getting the most benefits from Docker.

- Learn to [build an image from a Dockerfile](/get-started/part2.md){: target="*blank" class="*"}
- Use [multistage builds](/engine/userguide/eng-image/multistage-build.md){: target="*blank" class="*"} to keep your images lean
- Manage application data using [volumes](/engine/admin/volumes/volumes.md) and [bind mounts](/engine/admin/volumes/bind-mounts.md){: target="*blank" class="*"}
- [Scale your app](/get-started/part3.md){: target="*blank" class="*"} as a swarm service
- [Define your app stack](/get-started/part5.md){: target="*blank" class="*"} using a compose file
- General application development best practices

## Learn about language-specific app development with Docker

- [Docker for Java developers](https://github.com/docker/labs/tree/master/developer-tools/java/){: target="*blank" class="*"} lab
- [Port a node.js app to Docker](https://github.com/docker/labs/tree/master/developer-tools/nodejs/porting){: target="*blank" class="*"}
- [Ruby on Rails app on Docker](https://github.com/docker/labs/tree/master/developer-tools/ruby){: target="*blank" class="*"} lab
- [Dockerize a .Net Core application](/engine/examples/dotnetcore/){: target="*blank" class="*"}
- [Dockerize an ASP.NET Core application with SQL Server on Linux](/compose/aspnet-mssql-compose/){: target="*blank" class="*"} using Docker Compose

## Advanced development with the SDK or API

When you're comfortable developing apps by writing Dockerfiles or compose files and using the Docker CLI, you can take it to the next level by using the Docker Engine SDK for Go or Python or using the HTTP API directly.