## OS2sofd Arkitektur
OS2sofd er en samling af forskellige kompoenenter, som hver løser sin egen isolerede opgave. Disse komponenter er indelt i 3 kategorier

- **Kernekomponenter**. Disse komponenter holder data og udstiller typisk en brugergrænseflade. Der er en interaktion mellem brugere og løsningen, og der skabes, anvendes og vedligeholdes data i disse systemer.
- **Middleware**. Disse komponenter håndterer integrationer til/fra eksterne systemer. Det kan være simple integrationer der blot flytter data fra A-Z eller det kan være mere komplekse integrationer der fletter data fra flere kilder, og på baggrund af disse udfører bestemte opdaterende handlinger fx i nogle af kernekomponenterne.
- **Agenter**. Disse komponenter er typisk simple, og udfører handlinger på baggrund af ordre der kommer fra en kernekomponent. Agenter installeres lokalt i kommunens infrastruktur, og er designet til at kræve mindst mulig konfiguration, opdatering og overvågning

Nedenfor er vist en mindre illustration af interaktionen mellem kernekomponenter, middleware og agenter
