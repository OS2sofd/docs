## OS2sofd Arkitektur
OS2sofd er en samling af forskellige kompoenenter, som hver løser sin egen isolerede opgave. Disse komponenter er indelt i 3 kategorier

- **Kernekomponenter**. Disse komponenter holder data og udstiller typisk en brugergrænseflade. Der er en interaktion mellem brugere og løsningen, og der skabes, anvendes og vedligeholdes data i disse systemer.
- **Middleware**. Disse komponenter håndterer integrationer til/fra eksterne systemer. Det kan være simple integrationer der blot flytter data fra A-Z eller det kan være mere komplekse integrationer der fletter data fra flere kilder, og på baggrund af disse udfører bestemte opdaterende handlinger fx i nogle af kernekomponenterne.
- **Agenter**. Disse komponenter er typisk simple, og udfører handlinger på baggrund af ordre der kommer fra en kernekomponent. Agenter installeres lokalt i kommunens infrastruktur, og er designet til at kræve mindst mulig konfiguration, opdatering og overvågning

Nedenfor er vist en mindre illustration af interaktionen mellem kernekomponenter, middleware og agenter

![Screenshot from 2022-11-01 09-58-46](https://user-images.githubusercontent.com/9005414/199197713-63987b9e-45ba-42d6-a711-5224f24a201e.png)

Et givent deployment for en kommune, vil indeholde en samling af middleware og agenter, og mindst én kernekomponent (OS2sofds primære kernekomponent kaldet SOFD Core).

Eksempler på andre kernekomponenter er

- Vikarmodulet (også kaldet OS2vikar)
- Brugertjek
- Ledersiden

