# n8n + postgresql docker-compose

Run a Postgresql database in addition to n8n and Traefik included in [the n8n doc docker-compose](https://docs.n8n.io/hosting/installation/server-setups/docker-compose/#5-create-docker-compose-file).

Add some configuration tweaks to n8n too.

## Usage

- Review docker-compose.yml
- Install docker and docker compose
- Fill-in the .env file
- Point a A-record with your domain and subdomain towards the server

Run :
```bash
docker volume create db
docker volume create ssl
docker volume create n8n
docker volume create n8n-files
set -a
source .env
docker compose up -d
```
