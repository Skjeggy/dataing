

Modellen består av følgende fag: 

1. [[Applikasjonslaget]] Dette er laget brukeren/hosten befinner seg i. Data fra applikasjonen blir sendt som message. 
2. [[Transportlaget]] Dette laget sørger for å transportere data til applikasjonen eller neste lag under ved å benytte seg av to transportprotokoller kalt UDP(User datagram protocol) og TCP (transmission Control protocol). Det som skiller disse protokollene fra hverandre, er hvordan de håndterer overføring og pålitelighet. Datapakker fra dette laget blir sendt som et segment. 
3. [[Nettverkslaget]] Dette laget befinner IP protokollen seg i. IP blir mye brukt når pakker oppgir adressen den blir sendt fra og adressen den skal til. Pakker sendt fra dette laget blir kalt for datagram. 
4. [[Ethernet]] Dette laget kan relateres til rutere og dens adresser. Adresser her blir kalt for MAC adresser, dette er ikke det samme som IP adresse. Dette laget kan både lese IP og MAC adresser mens lag 3 kun leser IP adresser. Pakker sendt fra dette laget kalles for frame. 
5. [[Fysisk]] Sender data ut som en bitstrøm. Generelt kan man si at en protokoll er sett med regler som må følges når enheter kommuniserer med hverandre over nett.



## Application layer
The application layer is the topmost layer of the protocol hierarchy. It is the layer where actual communication is initiated. It's also the layer that both the client and the server are in. An example of a protocol in this layer is the **HyperText Transfer Protocol (HTTP)**. HTTP is an application layer protocol used for transferring information between computers on the World Wide Web.

Packets in this layer are called **messages**.

## Transport layer
This layer consists of two protocols: Transmission Control Protocol (TCP) and user datagram protocol (UDP). Both protocols break up a message that an application wants to send into packets to the intended recipient. At the recipient end of the communication, both take the payload from the received packets and pass those to the application layer. Example: an email client and server communicate over a reliable TCP connection. The server acknowledges a request and a TCP connection is established. Using this connection, the client and server can exchange data.

Packets in this layer are called **segments**.

## Network layer
The network layer is responsible for transmitting and routing data packets on the network. The internet uses the internet protocol (IP) as it's network layer. Each node on the network has an IP address of which data is sent as IP packets. When a client sends its TCP connection request, the network layer puts the request in a number of packets and transmits each of them to the server. Each packet can take different routes and some packets may get lost along the way. If the all make it, the transport layer at the server is able to reconstruct the request and prepare a response confirming that the TCP connection was established. This response is sent back in a number of IP packets that will hopefully make it back to the client.

Packets in this layer are called **datagram**.

## Data Link Layer
The data link layer provides a network connection between hosts on a particular local network. Some examples are Ethernet, WiFi, switches, etc. The internet protocol basically assumes all computers are part of one large "web" of nodes that can all pass packets to other nodes. There is always a route from one node to another; even if there are sometimes a large number of intermediate nodes get involved. The datalink layer makes this assumption true.

Packets in this layers are called **frames**.

## Physical Layer
The lowest layer of the five-layer network model that defines how the cables, network cards, wireless transmitters connect to the networks and the networks to the internet.

physical layer is to move the individual
bits within the frame from one node to the next.