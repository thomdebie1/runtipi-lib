## Scanopy

Scanopy is een krachtige self-hosted netwerk visualisatie tool die automatisch je netwerk scant, hosts en services identificeert, en interactieve diagrammen genereert die laten zien hoe alles met elkaar verbonden is.

### Belangrijkste functies

- **Automatische ontdekking**: Scant netwerken om hosts, services en hun relaties te identificeren
- **200+ Service definities**: Detecteert automatisch databases, webservers, containers, netwerkinfrastructuur, monitoring tools en enterprise applicaties
- **Interactieve topologie**: Genereert visuele netwerkdiagrammen met uitgebreide aanpassingsmogelijkheden
- **Gedistribueerd scannen**: Deploy daemons over netwerksegmenten om complexe topologieën in kaart te brengen
- **Docker integratie**: Ontdekt gecontaineriseerde services automatisch
- **Organisatiebeheer**: Multi-user ondersteuning met rol-gebaseerde permissies
- **Geplande ontdekking**: Geautomatiseerd scannen om documentatie actueel te houden

### Perfect voor

- **Home Lab enthousiastelingen**: Documenteer je groeiende infrastructuur
- **IT Professionals**: Onderhoud accurate netwerkinventaris zonder handmatige spreadsheets
- **Systeembeheerders**: Visualiseer complexe multi-VLAN omgevingen
- **DevOps Teams**: Breng gecontaineriseerde services en hun afhankelijkheden in kaart
- **MSPs**: Beheer meerdere klantnetwerken met je team

### Architectuur

Deze Runtipi app bevat:
- **Scanopy Server**: Hoofdapplicatie met web UI (poort 60072)
- **Scanopy Daemon**: Achtergrondproces voor netwerk scanning
- **PostgreSQL**: Database voor opslag van alle data

### Eerste start

1. Open Scanopy op de geconfigureerde URL (standaard poort 60072)
2. Maak je account aan
3. Wacht tot de eerste discovery voltooid is
4. Bekijk je automatisch gegenereerde netwerkdiagram

### Data & persistentie

Alle data wordt persistent opgeslagen:
- **Database**: PostgreSQL data
- **App data**: Configuratie en scans

### Netwerk toegang

Scanopy heeft netwerktoegang nodig om je infrastructuur te kunnen scannen. De daemon draait in host network mode om volledige netwerktoegang te hebben.

### Beveiliging

- Alle secrets worden lokaal door Runtipi gegenereerd
- Ondersteunt HTTPS via Runtipi's reverse proxy
- Multi-user met rol-gebaseerde toegangscontrole
- OIDC ondersteuning voor SSO

### Resources

- [Documentatie](https://scanopy.net/docs)
- [GitHub](https://github.com/scanopy/scanopy)
- [Discord Community](https://discord.gg/scanopy)
- [Showcase](https://scanopy.net/showcase)
