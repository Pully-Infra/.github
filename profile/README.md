# .github

This repo holds major information on the pully infrastructure.

## Pully CLI

- Manages communication to the pully infrastructure through a CLI.
- Has commands to:
  - Deploy and destroy the pully infrastructure.
  - Create JWT Tokens to authenticate server connections.
  - Update the relationships.json file.
  - Create, update, delete and deploy changes to pully middleware functions.
  - View the status of pully functions.

## Pully Server

- Manages the websocket server that handles realtime communication.
- Important Information:
  - Makes use of the socket.io library for websocket connections.
  - Makes use of redis for synchronising the updated relationships.json file across multiple servers.
  - Deployed to ECS using fargate launch type.
  - Auto scales based on CPU and memory usage.

## Pully Deployment

- Manages the deployment of pully infrastructure using AWS CDK.
- You can clone this repo and run `cdk deploy` to deploy the infrastructure to your AWS Account.

## Pully Client

- A simple JS Class that manages the communication with the pully server from the client side.
- Installable from npm by running `npm install pully-client` or using the [CDN](https://d2zbaqxz7kg7nk.cloudfront.net/).
