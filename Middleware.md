## OS2sofd Middleware
Middleware er de komponenter i OS2sofd som håndterer det meste af arbejdet. Modsat agenter, som altid er simple og "bare" flytter rådata, så udfører middleware dataprocessering, holder forretningslogik og kan udføre komplekse operationer på data.

Hvor muligt udvikles middleware altid som multi-tenant komponenter, så de kan processere data for flere kommuner samtidig, og konfigurationen af middlewaren holdes i SQL, så der kan tages backup af konfigurationen, samt nemt automatisere deployment af en ny kommune i en given middlewarekomponent uden redeploy eller genstart af komponenten.

I forhold til integrationen til eksterne systemer samt kernekomponenterne i OS2sofd, udstyres middlewaren altid med dobbelt-personlige nøgler, forstået på den måde at der oprettes nøgler som er unikke både for kommunen og middlewaren. Dermed kan man unikt identificere hvilken kommune samt hvilken middleware der har forestået en given opdatering i en kernekomponent (i det tilfælde hvor kernekomponent ikke er multi-tenant, er det alene middlewaren der spores på denne måde).

Middleware skrives i hvad end programmeringssprog der er bedst egnet til den givne opgave. Hvis der findes frameworks i et givent sprog som er optimalt i forhold til det givne arbejde, vil det typisk diktere valget af programmeringssprog.
