# Postiz — Social Media Scheduling Tool

Postiz is an open-source, all-in-one social media scheduling and management platform.
This deployment runs at **https://psa.innotel.us**.

## Architecture

The Docker Compose stack includes:

| Service | Description |
|---|---|
| `postiz` | Main application (Next.js + NestJS) |
| `postiz-postgres` | PostgreSQL 17 for app data |
| `postiz-redis` | Redis 7 for queues & rate limiting |
| `temporal` | Temporal workflow engine |
| `temporal-postgresql` | PostgreSQL 16 for Temporal |
| `temporal-elasticsearch` | Elasticsearch for Temporal visibility |
| `temporal-ui` | Temporal dashboard (localhost:8080) |

## Quick Start

### 1. Clone & Configure

```bash
cp .env.example .env
```

Then generate strong secrets:

```bash
sed -i "s/change-me-96-char-hex-string/$(openssl rand -hex 48)/" .env
sed -i "s/change-me-password/$(openssl rand -hex 32)/" .env  # runs twice for both passwords
```

Edit `.env` and fill in any social media API keys you need.

### 2. Start

```bash
docker compose up -d
```

### 3. Access

- **App:** `http://localhost:4007` (or your reverse proxy at `psa.innotel.us`)
- **Temporal UI:** `http://localhost:8080`

### 4. First-Time Setup

1. Open the app and create your admin account (first signup only — registrations are locked after).
2. Connect your social media accounts via the dashboard.

## HTTPS / Reverse Proxy

The app is configured to expect `https://psa.innotel.us`. You'll need a reverse proxy (nginx, Caddy, or Traefik) in front to:

- Terminate SSL/TLS for `psa.innotel.us`
- Proxy requests to `localhost:4007`

### Sample Caddy Config

```
psa.innotel.us {
    reverse_proxy localhost:4007
}
```

## Managing Updates

```bash
git pull
docker compose pull
docker compose down && docker compose up -d
```

## Environment Variables

Secrets live in `.env` (gitignored). The Docker Compose file uses `${VAR}` substitution to inject them.

See `.env.example` for all available variables and the official [Postiz Configuration Reference](https://docs.postiz.com/configuration/reference) for full details.
