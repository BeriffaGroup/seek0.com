<div align="center">


#### `3` 🔨 Source Code
```bash
git clone https://github.com/zmh-program/next-whois-ui
cd next-whois-ui

npm install -g pnpm
pnpm install
pnpm dev
```

## 📏 Envs

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

## 📝 API Reference
`GET` `/api/lookup?query=google.com`

<details>
<summary><strong>Response</strong> OK (200)</summary>

```json
{
  "time": 1.547,
  "status": true,
  "cached": false,
  "result": {
    "domain": "GOOGLE.COM",
    "registrar": "MarkMonitor Inc.",
    "registrarURL": "http://www.markmonitor.com",
    "ianaId": "292",
    "whoisServer": "whois.markmonitor.com",
    "updatedDate": "2019-09-09T15:39:04.000Z",
    "creationDate": "1997-09-15T04:00:00.000Z",
    "expirationDate": "2028-09-14T04:00:00.000Z",
    "status": [
      {
        "status": "clientDeleteProhibited",
        "url": "https://icann.org/epp#clientDeleteProhibited"
      },
      {
        "status": "clientTransferProhibited",
        "url": "https://icann.org/epp#clientTransferProhibited"
      },
      {
        "status": "clientUpdateProhibited",
        "url": "https://icann.org/epp#clientUpdateProhibited"
      },
      {
        "status": "serverDeleteProhibited",
        "url": "https://icann.org/epp#serverDeleteProhibited"
      },
      {
        "status": "serverTransferProhibited",
        "url": "https://icann.org/epp#serverTransferProhibited"
      },
      {
        "status": "serverUpdateProhibited",
        "url": "https://icann.org/epp#serverUpdateProhibited"
      }
    ],
    "nameServers": [
      "NS1.GOOGLE.COM",
      "NS2.GOOGLE.COM",
      "NS3.GOOGLE.COM",
      "NS4.GOOGLE.COM"
    ],
    "registrantOrganization": "Unknown",
    "registrantProvince": "Unknown",
    "registrantCountry": "Unknown",
    "registrantPhone": "+1 2086851750",
    "registrantEmail": "Unknown",
    "rawWhoisContent": "..."
  }
}
```
</details>

<details>
<summary><strong>Error Response</strong> Internal Server Error (500)</summary>

```json
{
  "time": 0.609,
  "status": false,
  "error": "No match for domain google.notfound (e.g. domain is not registered)"
}
```
</details>

<details>
<summary><strong>Error Response</strong> Bad Request (400)</summary>

```json
{
  "time": -1,
  "status": false,
  "error": "Query is required"
}
```
</details>

## 🧠 Tech Stack
- Next.js
- Shadcn UI & Tailwind CSS
- Whois Core Lib (@[whois-raw](https://www.npmjs.com/package/whois-raw))

## 💪 TLDs Support
👉 [TLDs Whois Parser Lib Source Code](./src/lib/whois/lib.ts)

❤ TIP: The Whois Parser for some TLDs may not be currently compatible, thanks for contributing your [Pull Request](https://github.com/zmh-program/next-whois-ui/pulls) to make this project support more TLDs!
