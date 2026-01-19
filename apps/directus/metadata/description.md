## Directus

Directus is een krachtige open-source headless CMS en data platform dat elke SQL database omzet naar een volledig functionele API met een moderne admin interface.

### Belangrijkste functies

- **REST & GraphQL API**: Instant toegang tot je data via beide API-formaten
- **Geen migraties nodig**: Werkt direct met bestaande of nieuwe SQL databases
- **Moderne dashboard**: No-code admin interface gebouwd met Vue.js
- **Volledig uitbreidbaar**: White-label en modulair platform
- **Real-time updates**: WebSocket ondersteuning voor live data synchronisatie
- **Geavanceerde permissies**: Granulaire rol-gebaseerde toegangscontrole

### Ondersteunde databases

Directus werkt met:
- PostgreSQL (standaard in deze Runtipi app)
- MySQL / MariaDB
- SQLite
- MS-SQL
- OracleDB
- CockroachDB

### Architectuur

Deze Runtipi app bevat:
- **Directus**: Hoofdapplicatie met API en admin dashboard (poort 8055)
- **PostgreSQL**: Database voor opslag van alle content en configuratie
- **Redis**: Caching voor betere performance

### Use cases

- **Headless CMS**: Beheer content voor websites, apps en IoT
- **Admin panels**: Bouw interne tools zonder code
- **Data management**: Beheer en visualiseer elke SQL database
- **API gateway**: Unified API voor meerdere databronnen

### Eerste start

1. Open Directus op de geconfigureerde URL
2. Log in met het admin e-mailadres en wachtwoord dat je hebt ingesteld
3. Begin met het definiëren van je datamodel of verbind met een bestaande database

### Data & persistentie

Alle data wordt persistent opgeslagen:
- **Database**: PostgreSQL data in `/db`
- **Uploads**: Bestanden en media in `/uploads`
- **Extensions**: Custom extensies in `/extensions`

### Beveiliging

- Alle secrets worden lokaal door Runtipi gegenereerd
- Ondersteunt HTTPS via Runtipi's reverse proxy
- Granulaire permissies voor gebruikers en API toegang
- Ondersteuning voor SSO en externe authenticatie providers

### Resources

- [Documentatie](https://docs.directus.io)
- [GitHub](https://github.com/directus/directus)
- [Discord Community](https://directus.chat)
