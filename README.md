# Gateway Service

This directory contains the configuration for the Kong Gateway used in the HRM-MS platform.

## Structure

- `docker-compose.yml`: Docker Compose file for setting up the gateway.
- `kong/kong.yml`: Configuration file for Kong Gateway.

## Kong Configuration

The `kong/kong.yml` file defines the services and routes for the gateway. For example:

- **Service**: `example_service`
  - Host: `httpbin.konghq.com`
  - Port: `80`
  - Protocol: `http`
- **Route**: `example_route`
  - Path: `/mock`
  - Strip Path: `true`

## Usage

1. Ensure Docker is installed and running.
2. Use `docker-compose` to start the gateway:

   ```bash
   docker-compose up -d
   ```

3. Access the configured routes via the gateway.
