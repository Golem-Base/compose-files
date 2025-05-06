# Golem Base L3 Node (Holesky)

This repository contains the Docker Compose configuration to run a Golem Base L3 node connected to the Holesky L2 testnet.

## Components

The setup includes the following main components:
- `op-geth`: The execution client for the L3 chain
- `op-node`: The consensus client that connects to L2 and manages the rollup

## Exposed Ports

The following ports are exposed to your host machine:

- `8545`: op-geth HTTP RPC endpoint
  - Supports APIs: debug, eth, txpool, net, engine, web3
- `8546`: op-geth WebSocket endpoint
  - Supports same APIs as HTTP endpoint
  - Allows WebSocket connections with `ws://localhost:8546`
- `9545`: op-node RPC endpoint

## Prerequisites

- Docker
- Docker Compose

## Getting Started

1. Clone this repository
2. Navigate to the `l3-holesky` directory
3. Start the node:
   ```bash
   docker compose up -d
   ```

The setup will automatically:
- Download the necessary genesis files
- Initialize the geth client
- Generate required JWT secrets
- Start synchronizing with the network

## Monitoring

You can monitor the sync status through the RPC endpoints:
- L2 execution client: `http://localhost:8545`
- L2 consensus client: `http://localhost:9545`

## Note

This node connects to Holesky L2 endpoints at:

- Execution: https://execution.holesky.l1.gobas.me
- Consensus: https://consensus.holesky.l1.gobas.me

## Bridge

To transfer funds from Holesky L2 to our L3, send funds to the bridge address `0x54d6c1435ac7b90a5d46d01ee2f22ed6ff270ed3`
