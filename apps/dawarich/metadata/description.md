## Dawarich

Dawarich is een self-hosted applicatie voor het verzamelen, opslaan en visualiseren van locatiegegevens.  
De applicatie is bedoeld als privacy-vriendelijk alternatief voor commerciële location-trackingdiensten.

Deze Runtipi-app draait Dawarich met alle vereiste componenten:
- Rails web applicatie
- Sidekiq background worker
- PostGIS (PostgreSQL + geodata)
- Redis voor queues en caching

### Belangrijkste functies
- Opslaan en bekijken van historische locatiegegevens
- Geografische visualisaties en statistieken
- Ondersteuning voor achtergrondverwerking via Sidekiq
- Volledig self-hosted: jouw data blijft op je eigen server

### Architectuur
Deze app bestaat uit meerdere services:
- **Web**: Rails server (poort 3000 intern)
- **Sidekiq**: achtergrondtaken en imports
- **PostGIS**: database met georuimtelijke ondersteuning
- **Redis**: job queues en caching

Runtipi beheert automatisch networking, volumes en lifecycle van alle containers.

### Data & persistentie
Alle data wordt persistent opgeslagen in de app-data directory van Runtipi:
- Database data (PostGIS)
- Geïmporteerde bestanden
- Publieke assets en storage

Bij herinstallatie of update blijft de data behouden.

### Eerste start
De eerste keer opstarten kan enkele minuten duren:
- Database initialisatie
- Migrations
- Eventuele asset-voorbereiding

Controleer bij twijfel de containerlogs van `dawarich_app`.

### Beveiliging
- Secrets (database wachtwoord, Rails secret key) worden **lokaal** door Runtipi gegenereerd of ingevuld
- Er worden **geen gevoelige gegevens** opgeslagen in de app store repository
- Ondersteunt exposure via Runtipi met HTTPS

### Opmerkingen
- Deze setup is bedoeld voor **self-hosted gebruik**
- Zorg voor voldoende geheugen (minimaal enkele GB RAM aanbevolen)
- Locatie- en importtaken kunnen CPU-intensief zijn bij grote datasets
