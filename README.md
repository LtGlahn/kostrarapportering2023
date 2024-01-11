# KOSTRA-leveranse 2023 

Årets KOSTRA-rapport fra Nasjonal vegdatabank (NVDB) bruker samme metodikk som vi har brukt siden 2020, ref [fjorårets leveranse](https://github.com/LtGlahn/kostrarapportering2022). 

På grunn av regionreform 2024, der tre av fylkene fra 2020-reformen ble delt i mindre fylker, har vi fått littegrann ekstraarbeid med 
å "regne om" fra de 15 nye fylkesnumrene (gyldig fra 1.1.2024) til de 11 gamle. Dette er heldigvis et trivielt tabelloppslag. 

Tabellen "KOSTRA 01 - Vegnett hele landet" har et par faner med detaljert veglengde per kommune. I denne tabellen har vi 
konsekvent brukt de nye kommunenumrene, og altså IKKE regnet bakover til det kommunenummeret som var gyldig før 31.12.2023. 
Dette ut fra en kost/nytte vurdering - hovedfokus for denne KOSTRA-rapporteringen er tall for fylkesveg, ikke kommunalveg. 

> Vi antar at dem som er interessert fint klarer å finne sitt kommunenummer.
>
> Eneste unntak er 1508 Ålesund og 1580 Haram kommune: For å få riktige tall for 2023-kommunen 1507 Ålesund må man 
> legge sammen data for 1508 Ålesund og 1580 Haram. (Som kjent var Haram en del av Ålesund før 1.1.2024). 

# Nedlasting 

_Ikke ferdigskrevet, kommer snart - i mellomtiden kan du se på [fjorårets bruksanvnisning](https://github.com/LtGlahn/kostrarapportering2022#nedlasting)_


### Filstruktur 

| Navn formell bestilling                                              |  Nummerering | Filnavn                                                    |
|--------------------------------------------------------------------------------|----|------------------------------------------------------------|
| Riks-, fylkes-, kommune-, privat- og skogsbilveg                               |  1 | Kostra 01 - Vegnett hele landet.xlsx                       |
|                                                                                |    | Kostra 01 - Vegnett hele landet 2024 fylker.xlsx           |
|                                                                                |  2 | Kostra 02 - Fylkesveg med motorveg og motortrafikkveg.xlsx |
| Fylkesveg uten fast dekke                                                      |  3 | Kostra 03 - Fylkesveg uten fast dekke.XLSX                 |
| Fylkesveg med 4 felt                                                           |  4 | Kostra 04 - Fylkesveg med 4 felt.XLSX                      |



# Merknader til de enkelte rapportene 

Konnekteringslenker knytter sammen en sideveg og en hovedveg i et kryss, og utgjør typisk 5-15 meter mellom det punktet der sideveg møter hovedvegenes vegkant og senterlinja på hovedveg. Disse 5-15 metrene skal ikke regnes med når vi teller veglenger. De utgjør i snitt mindre enn 0.05% av vegnettet, men de er ujevnt fordelt. Konnekteringslenker inngår ikke når vi teller lengder av vegnett, men noen av lengdene nedenfor er opptelling av såkalte _fagdata_, dvs NVDB objekttyper som er _"limt oppå"_ vegnettet i NVDB. For disse klarer vi p.t. ikke skille ut konnekterinngslenkene når vi jobber med fagdata. 

### Kostra 01 - Vegnett hele landet

Rapport nummer 1, _"Vegnett hele landet"_, teller lengden av kjørbart vegnet i Norge. Merk at lengdene her oppgis i kilometer, til forskjell fra øvrige rapporter, som har meter som lengdeenhet. 

Her teller vi ikke gang- og sykkelveger, kun trafikantgruppe K (kjørende). Av typeVeg så teller vi med verdiene _kanalisertVeg, enkelBilveg, rampe, rundkjøring_ og _gatetun_ Vi teller ikke med sideanlegg, strekninger med _adskilte løp=Mot_ og konnekteringslenker. Derimot teller vi alle kryssdeler. 

Som en ekstraservice lager vi også en rapporversjon med den nye fylkesinndelingen `Kostra 01 - Vegnett hele landet 2024 fylker.xlsx`. 

Rapporten har også en oppsummering per kommune. Ut fra en kost/nytte vurdering har vi her valgt å bruke 2024-kommunenumrene, og altså IKKE regne om til de kommunenumrene som gjaldt i 2023. 

> Vi antar at dem som er interessert fint klarer å finne sitt kommunenummer.
>
> Eneste unntak er 1508 Ålesund og 1580 Haram kommune: For å få riktige tall for 2023-kommunen 1507 Ålesund må man 
> legge sammen data for 1508 Ålesund og 1580 Haram. (Som kjent var Haram en del av Ålesund før 1.1.2024). 

    Årets rapport har 16 km mindre riksveg enn i fjor. Dette skyldes at gamle europaveg-traséer er omklassifisert til fylkesveg i Agder og Vestland fylke. Slike omklassifiseringsprosesser er politisk styrt, og det kan gå både måneder og år før gamlevegen er omklassifisert etter at nyvegen er åpnet.


### Kostra 02 - Fylkesveg med motorveg og motortrafikkveg

Her teller vi lengden av objektet _Motorveg (595)_ langs fylkesvegnettet. Det er såpass få (4 strekninger) at vi ramser dem opp per fylke og vegnummer. Vi teller med eventuelle kryssdeler, men ikke med sideanlegg eller strekninger med _adskilte løp=Mot_. 

### Kostra 03 - Fylkesveg uten fast dekke

Her finner vi lengden av objekttypen _Vegdekke (241)_ langs fylkesveg med egenskapfilteret _massetype = Grus_, og skiller tall for vanlig bilveg (trafikantgruppe K) fra tall for gående og syklende (trafikantgruppe G) i egne faner. Vi teller ikke med sideanlegg og _adskilte løp = Mot_. 

### Kostra 04 - Fylkesveg med 4 felt

Her teller vi lengden av vegnett som har fire eller flere felt. Vi regner ikke med kjørefelt av typene sykkelfelt, fergeoppstillingsplass og ekstra felt ved bomstasjoner. Vi teller heller ikke med kryssdeler, sideanlegg og konnekteringslenker, og heller ikke _adskilte løp = Mot_. 

Denne rapporten er laget med applikasjonen ["NVDB rapporter for KOSTRA"](https://nvdb-kostra.atlas.vegvesen.no/ ) med [disse valgene](https://raw.githubusercontent.com/LtGlahn/kostrarapportering2021/master/bilder/lastned04-firefeltsfylkesveg.png) 


### Kostra 05 Fylkesveg med maks aksellast under 10 tonn

Her finner vi lengden av objekttypen _Bruksklasse, normaltransport (904)_ med de egenskapverdiene som tilsier maks aksellast under 10 tonn, langs fylkesveg for trafikantgruppe _kjørende_. Vi tar ikke med data for sideanlegg og _adskilte løp = Mot_. 

### Kostra 06 Fylkesveg med maks totalvekt under 50 tonn

Her finner vi lengden av _Bruksklasse, normaltransport (904)_ langs fylkesveg med de egenskapverdiene som tilsier maks totalvekt under 50 tonn, for trafikantgruppe _kjørende_. Vi tar ikke med data for sideanlegg og _adskilte løp = Mot_.


### Kostra 07 Fylkesveg med fartsgrense under 50 km/t. 

Her finner vi lengden av _Fartsgrense (105)_ langs fylkesveg med de egenskapverdiene som tilsier fartgrense 50 kilometer i timen eller lavere, for trafikantgruppe _kjørende_. Vi tar ikke med data for sideanlegg og _adskilte løp = Mot_.


### Kostra 08 Fylkesveg med begrensing på kjøretøylengde mindre enn 19,5 meter

Her finner vi lengden av _Bruksklasse, normaltransport (904)_ langs fylkesveg med de egenskapverdiene som tilsier maks kjøretøylengde kortere enn 19.5 meter, for trafikantgruppe _kjørende_. Vi tar ikke med data for sideanlegg og _adskilte løp = Mot_. 

### Kostra 09 Undergang med høyde lavere enn 4 meter. 

Her teller vi antall av _Høydebegrensning (591)_ med egenskapsfilteret _Type Hinder = Undergang/bru_ og _Skilta høyde < 4_ langs fylkesveg.

### Kostra 10 - IKKE I DENNE LEVERANSEN (fylkesveg med dårlig dekketilstand)

_Disse dataene finnes ikke i nasjonal vegdatbank, men i eget system for forvaltning av vegdekke. Vi forstår at dette er en separat leveranse; denne leveransen har kun data fra NVDB._

### Kostra 11 Fylkesveg uten fast dekke med ÅDT høyere enn 5000 kjøretøy per døgn 

Vi har ingen forekomster med fylkesveger uten fast dekke (dvs objekttypen _Vegdekke (241)_ med egenskapfilteret _Massetype = Grus_) som overlapper med objekttypen  _Trafikkmende (540)_ med egenskapen  _ÅDT, total_ større enn 5000 kjøretøy per døgn. (I NVDB vil du sagtens finne et par hundre meter med den metoden vi har brukt, men det er datafeil). 

### Kostra 12

Her teller vi objekttypen _Trafikkmengde (540)_ med egenskapverdien _ÅDT, total_ større enn 5000 kjøretøy per døgn langs fylkesveger. 

### Kostra 13 og 14 Tunneller på fylkesveg, antall og lengde

Her teller vi antall og samlet lengde for tunneler på fylkesveg. Analysen er en sammenstilling av objekttypene _Tunnelløp (67)_ og _Tunnel (581)_. Hvis _tunnel_ - objektet har egenskapen _Lengde, offisiell_ så bruker vi denne for å regne ut lengdene. Hvis ikke henter vi lengden fra tunnelløpet, enten fra tunnelløpets egenskap _Lengde_ eller fra tunnelløpets utstrekning langs vegnettet. 

### Kostra 15 Tunneller lengre enn 500 meter på fylkesveg 

Samme metodikk som for kostra 13 og 14, men nå teller vi kun antall og lengde for de tunnellene som er lengre enn 500 meter.

### Kostra 16 Tunneller på fylkesveg med høyde under 4 meter

Her finner vi objekttypene _Tunnel (581)_ og _Tunnelløp (67)_ som overlapper med objekttypen _Høydebegrensning (591)_ som har egenskapverdi _Skilta høyde_ lavere enn 4 meter. For å finne lengden av tunneller bruker vi samme metode som Kostra 13, 14 og 15. 

