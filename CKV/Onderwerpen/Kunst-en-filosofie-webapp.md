# Kunst & Filosofie — project en uitleg

## De opdracht

Voor CKV maken we een eenvoudige interactieve webapp die via een link met docenten gedeeld kan worden. De bezoeker kiest een van twee vooraf bepaalde kunstwerken en klikt op een van twee filosofen om diens mening over dat werk te bekijken. De gebruiker levert de kunstwerken en verdere inhoud later aan. De volledige opdracht en beoordelingscriteria zijn nog niet bekend.

## Wat is er nu?

Er is een eerste werkende opzet met twee voorbeeldkunstwerken, twee voorbeeldfilosofen en vier duidelijk als voorlopig aangeduide meningen. De gebruiker kan tussen kunstwerken en filosofen schakelen; de getoonde tekst verandert mee. De definitieve inhoud en afbeeldingen ontbreken nog. Er zijn nog geen uitspraken aan echte filosofen toegeschreven.

De projectbestanden staan op de Mac in `/Users/nickgrybov/private/GIT/ckv-kunst-filosofie`. De tekst staat bij elkaar in `src/content.ts`. Het bestand `README.md` in de projectmap legt uit hoe je het project start en de inhoud wijzigt.

## Waarom deze technieken?

- **React** helpt de pagina op te delen in onderdelen en de inhoud te verversen wanneer iemand een keuze maakt.
- **JSX/TSX** lijkt op HTML, maar staat in JavaScript of TypeScript. Hiermee beschrijf je hoe de onderdelen van de pagina eruitzien. In dit project staat de pagina in `src/main.tsx`.
- **TypeScript** voegt typecontroles toe aan JavaScript. Daarmee kun je bijvoorbeeld eerder zien als een kunstwerk een verwacht veld mist.
- **Vite** start de ontwikkelomgeving en bouwt de bestanden die op een website kunnen worden geplaatst.
- **CSS** in `src/style.css` bepaalt onder andere kleur, indeling en opmaak voor telefoon en computer.

## Hoe werkt de keuze?

React bewaart welk kunstwerk en welke filosoof zijn geselecteerd. Wanneer je op een knop klikt, verandert die selectie. Vervolgens zoekt de app de mening op die bij die combinatie hoort en toont die op de pagina. De meningen zijn vooraf ingevulde teksten; de app gebruikt geen AI om ze te verzinnen.

In `src/content.ts` heeft elk kunstwerk een `id`. In `opinions` staat per filosoof een tekst bij diezelfde `id`. Zo weet de app welke tekst bij welk kunstwerk hoort.

## Lokaal starten

Open Terminal in de projectmap en voer `npm install` uit om de pakketten te installeren. Start daarna met `npm run dev` en open het adres dat de terminal toont. Stop de server met `Control + C`. Met `npm run build` controleer en bouw je de productieversie.

## Nog uit te zoeken

- Welke twee kunstwerken en filosofen worden gekozen?
- Wat zijn de opdrachtvoorwaarden en welke bronnen zijn geschikt voor de perspectieven?
- Welke afbeeldingen mogen gebruikt worden en welke bronvermelding is nodig?
- Hoe moet de uiteindelijke website toegankelijk worden voor de docenten? De eerste implementatie wordt privé gepubliceerd; toegang voor docenten is daarmee nog niet geregeld.

Zie ook het [proceslog](Proceslog-webapp.md).
