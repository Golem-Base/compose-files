# Golem Network Local Node Docker Compose Files

This repository contains Docker Compose configuration files for running Golem Base nodes locally using Docker containers. These configurations allow you to run and operate your own Golem node in a containerized environment.

## Overview

These docker-compose files enable you to run Golem Base nodes locally in Docker containers. This setup is suitable for running actual nodes that can participate in the Golem Base, process tasks, and interact with other nodes.

## Prerequisites

- Docker Engine installed on your system
- Docker Compose installed on your system
- Basic understanding of Docker and Docker Compose

## Usage

To run your Golem node:

1. Clone this repository
2. Change to the compose-file directory of the network of choice (`l2` or `l3`):
   ```bash
   cd l2-holesky
   ```
3. Run the docker-compose command:
   ```bash
   docker-compose up
   ```

## Configuration

Each docker-compose file is configured with appropriate boot nodes and network settings to ensure proper node operation.

## Important Notes

- Ensure you have enough system resources available for running the node
- Check your Docker daemon is running before starting the containers
