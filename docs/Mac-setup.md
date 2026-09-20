# Installeren op de Mac

## 1. Bestaand werk behouden

Sluit Obsidian voordat je de nieuwe indeling binnenhaalt. Controleer lokale wijzigingen met `git status`.
Bewaar eigen wijzigingen eerst; reset of overschrijf ze niet.
Deze branch verplaatst de bestaande vaultinstellingen en Welcome.md naar Studiecentrum.
Na samenvoegen van de pull request haal je de nieuwe main op in de bestaande checkout.
Voor een eerste clone:

```sh
git clone https://github.com/nickgrybov-netizen/obsidian-vault.git
cd obsidian-vault
```

De repository was op 20 september 2026 openbaar. Maak hem privé vóór het pushen van persoonlijke notities.
Deze starter verandert de zichtbaarheid niet. Kies één afgesproken Git/sync-werkwijze en voorkom gelijktijdige bewerkingen op meerdere apparaten.

## 2. Vier vaults openen

Open in Obsidian via “Open folder as vault” afzonderlijk Studiecentrum, Wiskunde-B, Scheikunde en Biologie.
Open de repositoryroot niet als vault. Gebruik de exacte mapnamen voor de dashboardlinks.
Verwijder eventueel de oude root uit de lijst met vaults; verwijder niet de map op schijf.
Open Start.md in Studiecentrum en Overzicht.md in het vak.
Voorkeuren zijn per vault; Smart Connections moet dus per vault worden geïnstalleerd.
Sjablonen staan in Templates. Vul de schoolboeken en huidige leerdoelen in Overzicht.md in.

Obsidian raadt vaults binnen een open vault af wegens linkupdates:
https://obsidian.md/help/Files+and+folders/How+Obsidian+stores+data

## 3. Codex-projecten

Open de repository in Codex. Voor een vakgerichte sessie kun je de betreffende vakmap als project/werkmap kiezen.
De root bevat gedeelde instructies en .agents/skills; elke vakmap bevat aanvullende AGENTS.md-instructies.
Vraag in een nieuwe sessie: “Welke studie-instructies en skills heb je geladen?”
Laat Codex bij starten vanuit de root expliciet de gekozen vakinstructies lezen.
Als de app alleen toegang tot de vakmap geeft, open de root om de centrale planning bij te werken.
De leerworkflow werkt ook zonder MCP met gewone bestanden.
Gebruik de prompts in Studiecentrum/prompt-vault; kopieer een ChatGPT-overdracht expliciet naar Codex.
Een lokale MCP-server in Codex is niet automatisch gekoppeld aan elke ChatGPT-chat.

## 4. Smart Connections voorbereiden

Installeer via Obsidian Community plugins Smart Connections in iedere vault en laat de Markdown-notities indexeren.
Kies een lokale embeddingconfiguratie die door de MCP-server ondersteund wordt en Nederlands goed terugvindt.
Gebruik bij voorkeur hetzelfde ondersteunde model in alle vaults. De MCP-server moet zoekvragen met een passend model verwerken.
Noteer pluginversie en embeddingmodel in de acceptatiecheck.

We gebruiken als kandidaat de communityserver:
https://github.com/msdanyg/smart-connections-mcp

Npm-package: smart-connections-mcp, vastgezet op 2.0.1 (registry gecontroleerd 20 september 2026).
De README vermeldt Node.js 20+ en Smart Connections 3.x-data als getest.
Compatibiliteit met de daadwerkelijk geïnstalleerde plugin/modelcombinatie is nog niet bewezen.
Bij incompatibiliteit: gebruik voorlopig bestandszoeken en onderzoek een passende versie; pas caches niet handmatig aan.

De server gebruikt lokale embeddings. Opgehaalde notitie-inhoud die aan Codex wordt gegeven, valt wel onder de gegevensverwerking van de gebruikte AI-dienst.
Pluginbestanden en gegenereerde indexes worden niet via deze repository verspreid.

## 5. MCP toevoegen aan Codex

Controleer in Terminal `node --version` en `npx --version`. Node.js 20 of hoger is vereist door de server.
Als Codex CLI beschikbaar is, voer vanuit de repositoryroot uit:

```sh
study_root="$(pwd -P)"
codex mcp add smart-connections --env "SMART_VAULT_PATH=$study_root/Studiecentrum,$study_root/Wiskunde-B,$study_root/Scheikunde,$study_root/Biologie" -- npx -y smart-connections-mcp@2.0.1
codex mcp list
```

Gebruik geen komma in de repositorypadnaam: de server gebruikt komma's om vaultpaden te scheiden.
Dit installeert/downloadt het npm-pakket bij starten; de eerste modeldownload kan extra tijd kosten.

Zonder CLI: gebruik de MCP-instellingen van Codex of voeg het blok uit
[het configuratievoorbeeld](codex-mcp.example.toml) samen met de bestaande lokale `~/.codex/config.toml`.
Vervang ALLE voorbeeldpaden door absolute Mac-paden. Overschrijf de bestaande configuratie niet.
Als smart-connections al bestaat, werk die bestaande registratie bij in plaats van een tweede aan te maken.
Start Codex opnieuw. Als npx in de app niet gevonden wordt, gebruik de absolute uitkomst van `command -v npx`.
De voorbeeldconfiguratie is bewust niet automatisch actief in de repository.

Officiële Codex-configuratie:
https://learn.chatgpt.com/docs/extend/mcp?surface=cli

## 6. Controleren

Doorloop [Acceptatiecheck.md](Acceptatiecheck.md).
list_vaults/get_stats moeten alle vier vaults en eventuele fouten tonen.
Test zoekmodus, Nederlandse parafrases, bestandsinhoud en updates; “server verbonden” alleen is onvoldoende.
Bewaar wijzigingen aan notities lokaal en commit/push bewust. Semantische indexes bouw je per machine opnieuw op.
