Transportlaget protokollen får dataene til å tro de er direkte koblet sammen. Vi har to typer transportprotokoller: UDP og TCP. Den største forskjellen på disse to er påliteligheten ved sending av data. TCP er den protokollen som har feilfri og pålitelig overføring, mens UDP kan gjøre feil uten engang å si ifra verken til mottaker eller til sender. TCP er **forbindelsesorientert**, det vil si at før selve overføringen skjer, har TCP og mottakeren opprettet en forbindelse/snakket sammen før overføring. På denne måten har sender og mottaker hele tiden kontroll på om alt kommer og om feil skulle oppstå. TCP ber om ny data om data skulle gå tapt på veien. Oppgaven til disse protokollene er å samle og distribuere data til/fra host/applikasjoner.

Tilleggsfunksjoner som kan være med i laget: 
- Feilkontroll (gjelder UDP og TCP). 
- Feilretting (kun TCP) 
- Kvitteringer for å kommunisere om eventuell feil eller alt er bra (kun TCP) 
- Tilpasse senderraten avhengig av nettkapasiteten (TCP). 
- Tilpasse senderrate til mottakerkapasitet - sørge for at mottaker ikke blir overbelastet(TCP) 
 
TCP trenger portnummer og IP adresse for å lage en unik forbindelse. Portnumre fra 0 til 1013 er «well known» som vil si faste porter. 

[[Multiplexing og demultiplexing + litt UDP og TCP]]