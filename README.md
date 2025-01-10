# photo-spotter-gateway-service

## Table of Contents
- [Overview](#overview)
- [Planned Features](#planned-features)
- [Environment and Dependencies](#environment-and-dependencies)
- [API Endpoints](#api-endpoints)
- [Deployment and Usage](#deployment-and-usage)
- [Tasks](#tasks)

## Overview
This service functions as an API gateway or reverse proxy, offering a single entry point for external clients. It handles request routing, potential aggregation of data from multiple services, and can enforce rate limits or authentication checks.

## Planned Features
- Reverse proxy or API gateway routing for each microservice
- Authentication checks (propagating JWT or tokens)
- Request aggregation from multiple services
- Basic rate limiting and monitoring

## Environment and Dependencies
- C# or Go for gateway logic
- Optional frameworks like Ocelot (C#) for an API gateway pattern
- Docker for container deployment

## API Endpoints
- `/api/*` forwarding requests to the appropriate microservice
- `/gateway/health` for gateway health checks

## Deployment and Usage
- Run locally with `dotnet run` or `go run`
- Build Docker image: `docker build -t photo-spotter-gateway-service .`
- Deploy using Kubernetes (deployment.yaml, service.yaml, or Helm charts)

## Tasks
- Initialize the gateway scaffold
- Define routing rules to each microservice
- Integrate with CI for build/test
- Provide a unified `/health` or `/status` check
