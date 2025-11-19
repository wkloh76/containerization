# N8N RUN IN Local Machine

- The n8n-io community provides three methods to setup with Docker:
  1. subfolder with SSL cert
  2. with postgres
  3. with postgres and worker

## subfolder with SSL cert

- This n8n setup for https which apply SSL cert into n8n system and work in local network.

## with postgres

- This n8n setup for http which work with postgres database. This setup only work in local network.

## with postgres and worker

This n8n setup for http which work with postgres database and worker.This setup only work in local network.

# Reference

- [n8n-hosting](https://github.com/n8n-io/n8n-hosting.git) is a deployment method released by the n8n-io community.

- To reset the admin password for an n8n instance running in Docker
  ```
  docker exec-it <container id/name> n8n user-management:reset
  ```
