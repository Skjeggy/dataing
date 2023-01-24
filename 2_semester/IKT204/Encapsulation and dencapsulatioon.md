Kapittel 1.5.2 i boka. Sett av litt tid til å lese og forstå. 

# Svar
Når en message (fra application layer) reiser gjennom internettets 5 lag blir den "pakket" inn i forskjellige "konvolutter" som beskriver hva de forskjellige lagene skal gjøre med den - altså hvor den skal sendes. Encapsulation er altså instruksjoner til hvert lag av internett på hvordan de skal behandle pakken og hvor de skal sende den. 

Når beskjeden (message) beveger seg nedover i internettet-lagene, og den pakkes inn i disse konvoluttene kaller vi det for "encapsulation". Når den så på mottagersiden beveger seg oppover i lagene, blir den da pakket ut av konvoluttene, noe vi kaller for "decapsulation".


## Engelsk

When a message travels down through the different layers, it gets information appended to it known as headers. This is known as encapsulation. When the message goes through the transport layer, the message gets transport-layer header information appended. This header together with the original message is what constitutes a transport-layer segment. The same happens when the segment goes through the network layer (forms a datagram), and when the datagram goes through the link layer (forms a frame). As the the now encapsulated message travels upwards through the layers en route to its destination, the headers are stripped off one by one. As for example a datagram moves from the network layer to the transport layer, the respective header is removed and the datagram becomes a segment. This process is called decapsulation.



