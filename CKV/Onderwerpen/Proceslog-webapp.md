# Proceslog — Kunst & Filosofie

Hier houden we bij welke stappen echt zijn gezet, wat keuzes betekenen en wat nog moet gebeuren. Werk dit log bij na volgende projectstappen.

## 05-11-2026 — Idee en eerste versie

1. **Doel bepaald.** De leerling wil een eenvoudige CKV-webapp die via een link met docenten kan worden gedeeld. Twee filosofen geven elk hun perspectief op twee vooraf gekozen kunstwerken. De exacte inhoud volgt later.
2. **Techniek gekozen.** De leerling stelde JSX en TypeScript voor. De opzet gebruikt React met TSX en TypeScript, en Vite om de app lokaal te draaien en te bouwen. Zie [project en uitleg](Kunst-en-filosofie-webapp.md).
3. **Projectmap aangemaakt.** Codex maakte `/Users/nickgrybov/private/GIT/ckv-kunst-filosofie` en stelde de basisbestanden en afhankelijkheden in.
4. **Interactieve basis gebouwd.** Er zijn twee selecteerbare voorbeeldkunstwerken en twee selecteerbare voorbeeldfilosofen. Voor iedere combinatie staat een voorlopige tekst klaar in `src/content.ts`. De pagina is ook voor een kleiner scherm opgemaakt.
5. **Build gecontroleerd.** `npm run build` is geslaagd: TypeScript heeft de code gecontroleerd en Vite heeft de productieversie gemaakt. Een geslaagde build bewijst niet dat alle functies in een browser zijn getest.
6. **Publicatie voorbereid.** Een Sites-project is aangemaakt en een privépublicatie afgerond: [open de eerste versie](https://ckv-kunst-en-filosofie.lucky-boar-3385.chatgpt.site). Die is alleen voor de eigenaar bedoeld; toegang voor de docenten is nog niet geregeld. De definitieve inhoud ontbreekt nog.
7. **Documentatie ingericht.** Op verzoek van de leerling is een aparte CKV-vault ingericht met deze projectnotities en een sessieoverzicht. De leerling wil dat verdere stappen ook worden gedocumenteerd en deels uitgelegd.

## Volgende stappen

- Kunstwerken, filosofen, eventuele schoolinstructies en bronnen verzamelen.
- Samen de standpunten zorgvuldig uitwerken en duidelijk maken of ze interpretaties zijn.
- Afbeeldingen en bronvermelding toevoegen en de app verder controleren.
- Een toegankelijke link voor de docent regelen wanneer de inhoud klaar is.

## 12-11-2026 — Debatkeuzes gekozen

De leerling koos drie extra onderwerpen voor de discussie tussen Kuki en Kant: **Is eenvoud mooier dan perfectie?**, **Kan rust samengaan met beweging?** en **Is kunst om te bekijken of om te beleven?**. Deze zijn toegevoegd naast de drie bestaande onderwerpen: **Wat maakt iets mooi?**, **Hoe belangrijk is de context?** en **Is dit een beslissend moment?**. Alle zes onderwerpen hebben een eigen voorbeeldgesprek over zowel het Japanse theeritueel als de Discobolus. De bezoeker kiest dus eerst het kunstwerk en het onderwerp; de bijbehorende argumenten verschijnen naast elkaar. De dialogen zijn interpretaties voor de opdracht, geen historische citaten.
