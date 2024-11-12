#### `3` Source Code
```bash
git clone https://github.com/BeriffaGroup/seek0.com
cd next-whois-ui

npm install -g pnpm
pnpm install
pnpm dev
```

## Envs

### SEO
- `NEXT_PUBLIC_SITE_TITLE`: Site Title
- `NEXT_PUBLIC_SITE_DESCRIPTION`: Site Description
- `NEXT_PUBLIC_SITE_KEYWORDS`: Site Keywords

### WHOIS
- `NEXT_PUBLIC_HISTORY_LIMIT`: History Limit (Default: 6)
- `NEXT_PUBLIC_MAX_WHOIS_FOLLOW`: Max Domain Whois Follow (Default: 0)
- `NEXT_PUBLIC_MAX_IP_WHOIS_FOLLOW`: Max IP Whois Follow (Default: 5)

### CACHE
- `REDIS_HOST`: Redis Host (CACHE DISABLED WHEN EMPTY)
- `REDIS_PORT`: Redis Port (Default: 6379)
- `REDIS_PASSWORD`: Redis Password (OPTIONAL)
- `REDIS_DB`: Redis DB (Default: 0)
- `REDIS_CACHE_TTL`: Redis Cache TTL Secs (Default: 3600)

