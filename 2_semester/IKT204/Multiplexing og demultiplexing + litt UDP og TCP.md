![[Sockets]]

**Demultiplexing** er å levere riktig data i et transportlag segment to riktig socket. Mottakeren kan få mange data fra mange socket, og må se på feltet som bestemmer hvilket socket en skal sendes til. 

**Multiplexing** har med nettverkslaget og gjøre. Denne metoden går ut på å samle datapakker hos source hosten fra forskjellige socket, pakke dataene med header informasjon for å lage segmenter, og deretter sende segmentene til nettverkslaget. 

Et typisk transportlag segment består av source port nummer felt, destinasjon port nummer felt, other header fields, applikasjon/data/melding. Det er disse feltene som blir evaluert når den skal sendes til socket. UDP og TCP. 

