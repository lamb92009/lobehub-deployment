# LobeHub Deployment

Self-hosted LobeHub deployment on Coolify

## Services

This deployment includes:
- **LobeHub**: Main chat application
- **PostgreSQL**: Database with pgvector support (ParadeDB)
- **Redis**: Caching layer
- **RustFS**: S3-compatible object storage
- **SearXNG**: Metasearch engine (optional)

## Configuration

See `.env` file for environment variables. Key settings:

- `APP_URL`: https://your-domain.com
- Database, storage, and authentication secrets are pre-configured

## Deployment

This repository is deployed via Coolify using Docker Compose.

The docker-compose.yaml file contains all service definitions.

## Files

- `docker-compose.yaml`: Main compose configuration
- `.env`: Environment variables (not in repo, configured in Coolify)
- `.env.example`: Example environment variables
- `bucket.config.json`: RustFS bucket configuration
- `searxng-settings.yml`: SearXNG metasearch configuration

## Volumes

- `./data`: PostgreSQL data
- `./redis_data`: Redis persistence
- `./rustfs-data`: Object storage data