# Verificatie van de starter

Datum: 20 september 2026. Omgeving: Windows; de doelomgeving is een Mac.

## Statische controle

- Controle van JSON, YAML-frontmatter en skill-UI-metadata.
- Controle van zes skillnamen, beschrijvingen, bestandsnamen en verwijzingen in startprompts.
- Controle van lokale Markdown-links en Obsidian-vaultlinks tegen bestaande bestanden.
- Controle van vier vaults zonder .obsidian-map in de repositoryroot.
- Git-diffcontrole op whitespace en onbedoelde bestanden.

Uitkomst: geslaagd. Zes skills en 39 links gecontroleerd; JSON en YAML zijn parseerbaar. `git diff --cached --check` geeft geen fouten. De ignore-regels voor pluginbestanden, indexes, vensterindeling en lokale Codex-configuratie zijn gecontroleerd.

De Python-interpreter is niet beschikbaar op de uitvoerende machine. Daarom zijn de skillbestanden rechtstreeks aangemaakt en zijn init_skill.py en quick_validate.py niet uitgevoerd. Een tijdelijke Node-controle met een YAML-parser controleert de relevante metadataregels en links. Deze statische controle bewijst geen tutoringgedrag.

## Nog uitvoeren op de Mac

Alle functionele controles in [Acceptatiecheck.md](Acceptatiecheck.md) staan open: vaults openen, skills ontdekken, een sessie bewaren/hervatten, MCP starten, Nederlandse semantische zoekkwaliteit en indexupdates.
De MCP-package-identiteit en versie 2.0.1 zijn via de npm-registry gecontroleerd; de server is hier niet geïnstalleerd of gestart.
Geen embeddings gemaakt, geen persoonlijke leergegevens ingevoerd, geen repositoryzichtbaarheid veranderd.

## Volgende sessie

Bekijk en merge de pull request wanneer de indeling akkoord is. Haal de wijzigingen op de Mac binnen met behoud van lokaal werk. Volg [Mac-setup.md](Mac-setup.md), begin met Wiskunde-B en leg de acceptatieresultaten vast.
