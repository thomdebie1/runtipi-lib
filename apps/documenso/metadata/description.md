## Documenso

Documenso is het open-source alternatief voor DocuSign. Het stelt je in staat om documenten digitaal te ondertekenen met volledige controle over je data en privacy.

### Belangrijkste functies

- **Digitale handtekeningen**: Onderteken documenten veilig en rechtsgeldig
- **Self-hosted**: Volledige controle over je data en privacy
- **Open source**: Transparante code die je kunt inspecteren en aanpassen
- **Modern UI**: Gebruiksvriendelijke interface gebouwd met React en Next.js
- **API toegang**: Integreer document ondertekening in je eigen applicaties
- **Multi-signer support**: Stuur documenten naar meerdere ondertekenaars

### Use cases

- **Contracten**: Laat klanten en partners contracten digitaal ondertekenen
- **HR documenten**: Onboarding, arbeidsovereenkomsten en beleidsacceptatie
- **Juridische documenten**: Overeenkomsten en verklaringen met rechtsgeldige handtekening
- **Verkoop**: Offertes en bestellingen snel laten goedkeuren
- **Interne processen**: Goedkeuringen en autorisaties digitaliseren

### Architectuur

Deze Runtipi app bevat:
- **Documenso**: Hoofdapplicatie voor document ondertekening (poort 3000)
- **PostgreSQL**: Database voor opslag van documenten en gebruikers
- **Inbucket**: Lokale mailserver voor ontwikkeling (optioneel, vervangbaar door echte SMTP)

### Eerste start

1. Open Documenso op de geconfigureerde URL
2. Registreer een nieuw account via `/signup`
3. Upload je eerste document en stuur het ter ondertekening

### E-mail configuratie

Standaard wordt een lokale Inbucket mailserver meegeleverd voor testen. Voor productie kun je je eigen SMTP server configureren via de form velden:
- SMTP Host (bijv. `smtp.gmail.com`)
- SMTP Port (meestal `587` voor TLS)
- SMTP Username en Password

### Data & persistentie

Alle data wordt persistent opgeslagen:
- **Database**: PostgreSQL data in `/db`
- **Uploads**: Documenten en handtekeningen in `/uploads`
- **Certificaten**: Signing certificaten in `/certs`

### Beveiliging

- Alle secrets worden lokaal door Runtipi gegenereerd
- Ondersteunt HTTPS via Runtipi's reverse proxy
- Documenten worden veilig opgeslagen en versleuteld
- Open source: volledige transparantie over dataverwerking

### Resources

- [Documentatie](https://documen.so/docs)
- [GitHub](https://github.com/documenso/documenso)
- [Discord Community](https://documen.so/discord)
