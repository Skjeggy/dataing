
Modellen består av følgende fag: 

1. [[Applikasjonslaget]] Dette er laget brukeren/hosten befinner seg i. Data fra applikasjonen blir sendt som message. 
2. [[Transportlaget]] Dette laget sørger for å transportere data til applikasjonen eller neste lag under ved å benytte seg av to transportprotokoller kalt UDP(User datagram protocol) og TCP (transmission Control protocol). Det som skiller disse protokollene fra hverandre, er hvordan de håndterer overføring og pålitelighet. Datapakker fra dette laget blir sendt som et segment. 
3. [[Nettverkslaget]] Dette laget befinner IP protokollen seg i. IP blir mye brukt når pakker oppgir adressen den blir sendt fra og adressen den skal til. Pakker sendt fra dette laget blir kalt for datagram. 
4. [[Ethernet]] Dette laget kan relateres til rutere og dens adresser. Adresser her blir kalt for MAC adresser, dette er ikke det samme som IP adresse. Dette laget kan både lese IP og MAC adresser mens lag 3 kun leser IP adresser. Pakker sendt fra dette laget kalles for frame. 
5. [[Fysisk]] Sender data ut som en bitstrøm. Generelt kan man si at en protokoll er sett med regler som må følges når enheter kommuniserer med hverandre over nett.


