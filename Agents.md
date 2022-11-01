## OS2sofd Agenter
OS2sofd har en mindre række agenter - agenter anvendes alene i de scenarier hvor der kræves adgang til et on-premise system (fx Active Directory) hos kommunen. I alle scenarier hvor integrationer kan afvikles udenfor kommunens it-infrastruktur, anvendes middleware-komponenter, da disse nemmere kan overvåges og opdateres.

Da agenter typisk ikke opdateres i samme kadance som middleware-komponenter, holdes kodelogikken i agenterne så simpel som muligt. Data-processering og logik kobles altid sammen med en middleware-komponent. I praksis må en agent aldrig kommunikere direkte med en kernekomponent, men skal blot skubbe rå-data til en middlewarekomponent der tager alle beslutningerne.

Agenter er altid skrevet i C#, deployes som Windows Services, og følger den samme standardopbygning, så et højt niveau af kodegenbrug kan anvendes når der udarbejdes og vedligeholdes agenter. Hermed sikres det også at installation og opdatering følger standardprocedurer som er kendte i kommunen.
