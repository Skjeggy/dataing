---
alias: "IKT204 Assignment 1"
---

- [ ] Finish assignment 1 📅 2023-02-02

## Ch. 1.1. (10 points)  
Suppose there is exactly one packet switch between a sending host and a receiving host. The transmission rates between the sending host and the switch and between the switch and the receiving host are **_R_1** and **_R_2**, respectively. Assuming the switch uses store-and-forward packet switching, what is the total end-to-end delay to send a packet of length _L_? (Ignore queuing, propagation delay, and processing delay.

### Svar
Packet switches : 1
Transmission rates between sending host and switch: R_1
Transmission rates between sending host and switch: R_2
Store-and-forward packet switching. 

What is the total end-to-end delay to send a packet of length L ?

$$ d_{\text{end to end}} = N \cdot \frac{L}{R} $$
Where d = delay, N = number of links, L = number of bits in packets and R = rate. 
$$\text{Total end-to-end delay} = \frac{L}{R_1} + \frac{L}{R_2}  $$

## Ch. 1.2. (15 points) 
What are the five layers in the Internet protocol stack? What are the principal responsibilities of each of these layers?

### Svar
![[The five layers of the internet]]

## Ch. 1.3. (10 points)
What do encapsulation and de-encapsulation mean? Why are they needed in a layered protocol stack?

### Svar
![[Encapsulation and dencapsulatioon#Svar]]


## Ch. 1.4. (10 points)
**Which layers in the Internet protocol stack does a router process? Which layers does a link-layer switch process? Which layers does a host process?**

Routers process network, link and physical layers (layers 1 through 3). (This is a little bit of a white lie, as modern routers sometimes act as firewalls or caching components, and process Transport layer as well.) Link layer switches process link and physical layers (layers 1 through2). Hosts process all five layers.



## *Ch. 1.5. (10 points) 
**Describe how a botnet can be created, and how it can be used for a DDoS attack.

Creation of a botnet requires an attacker to find vulnerability in some application or system (e.g. exploiting the buffer overflow vulnerability that might exist in an application). After finding the vulnerability, the attacker needs to scan for hosts that are vulnerable. The target is basically to compromise a series of systems by exploiting that particular vulnerability. Any system that is part of the botnet can automatically scan its environment and propagate by exploiting the vulnerability. An important property of such botnets is that the originator of the botnet can remotely control and issue commands to all the nodes in the botnet. Hence, it becomes possible for the attacker to issue a command to all the nodes, that target a single node (for example, all nodes in the botnet might be commanded by the attacker to send a TCP SYN message to the target, which might result in a TCP SYN flood attack at the target).

## Ch. 1.6. (10 points)  
Propagation delay and transmission delay are two central concepts in data networking. Consider two hosts, A and B, connected by a single link of rate **_R_** bps. Suppose that the two hosts are separated by **_m_** meters, and suppose the propagation speed along the link is **_s_** meters/sec. Host A is to send a packet of size **_L_** bits to Host B.

Sjekk ut https://kopimi.datapor.no/DAT204%20-%20Datakommunikasjon/networkFormulas.pdf som har mye av svarene.

### **a)** Express the propagation delay, **_d_prop**, in terms of **_m_** and **_s_**. 

#### Svar:
Host A sends a packet of size L (bits) to Host B which is m meters away, using a link of rate R (bps) with propagation speed along the link being s (meters/second). What is the propagation delay in terms of m and s ? 

Since the propagation delay is $$ d_\text{prop} = \frac{d}{s} $$ where d is the distance between Host A and Host B, in other words m, and s is the propagation speed of the link, in other words s. Thus,

$$ d_\text{prop} = \frac{m}{s} $$

### **b)** Determine the transmission time of the packet, **_d_trans**, in terms of **_L_** and **_R_**.  

### Svar

L = packet length in bits
R = link bandwith in bps.

$$ d_{trans} = \frac{L}{R} $$


### **c)** Ignoring processing and queuing delays, obtain an expression for the end-to-end delay.  

### Svar

The total delay is given by accumulating the nodal processing delay, queuing delay, transmis-
sion delay, and propagation delay. That gives the following formula:

$$ d_{total} = d_{procg} + d_{queue} + d_{trans} + d_{prop} $$

Ignoring the processing and queuing delays, we get the following:

$$ d_{modified} = d_{trans} + d_{prop} $$


### **d)** Suppose Host A begins to transmit the packet at time **_t_ = 0**. At time **_t_ = _d_trans**, where is the last bit of the packet?  

### Svar
The bit is just leaving Host A. 

### **e)** Suppose **_d_prop** is greater than **_d_trans**. At time **_t_ = _d_trans**, where is the first bit of the packet?  

### Svar
The first bit is in the link and has not reached Host B.

### **f)** Suppose **_d_prop** is less than **_d_trans**. At time **_t_ = _d_trans**, where is the first bit of the packet?  

### Svar
The first bit has reached Host B.

### **g)** Suppose **_s_** = 2.5 **.** 108 m/s, **_L_** = 1500 bytes, and **_R_** = 20 Mbps, where M is SI standard (base 10) 106 and not binary (base 2) 220 = 10242. Find the distance **_m_** so that **_d_prop** equals **_d_trans**.

### Svar
$$ m = \frac{L}{R} \cdot s = \frac{1500 \cdot 8}{20 \cdot 10^{6}} \cdot 2.5 \cdot 10^{8} = 150 \: \text{km} $$

## **Ch. 1.7. (10 points)  
**Consider the network illustrated in Figure 1.16. Assume the two hosts on the left of the figure start transmitting packets of 1500 bytes at the same time towards Router B. Suppose the link rates between the hosts and the Router A is 4 Mbps, where M is SI standard (base 10) 106 and not binary (base 2) 220 = 10242. One link has a 2 milliseconds propagation delay and the other has a 3 milliseconds propagation delay. Link rate between Router A and Router B is 100 Mbps. Assume neglectable processing delay at Router A (**_dprocRouterA_ ≈ 0**) and its outbound queue towards Router B is currently empty. Will queuing delay occur in Router A? Support your answer with calculations.

![Chapter1_Figure_1.16.PNG](https://files.transtutors.com/book/qimg/a3b868b1-2e82-465e-858e-54da5c20781a.png)

### Svar
To know if queuing delay will occur at router A, we would need to inspect the factors that would cause a queuing delay in router A. 
- Both hosts send 1500 bytes in the direction of router B. 
- Using link speeds of 4Mbps, the expected arrival times of the packets would be 3ms. (1500 * 8 to turn to bits, divide by 4,000,000 Mb/s to get seconds and then multiply by 1000 to get milliseconds). 
- One link has a propagation delay of 2ms and the other has a propagation delay of 3ms. This means that the first packets of data arrive after 5ms and the next packets of data arrive after 6ms.
- According to p.64 of the textbook, processing delay typically has values on the order of microseconds or less. Since the difference in time between the two arrival times of the packets of data are of the order of milliseconds and milliseconds are much larger than microseconds, it means that the first set of packets should finish processing well before the second set arrives. Therefore, there will be no queuing delay occurring at router A.

Converting bytes to bit:
$$ 1500 \: \text{bytes} \cdot 8 = 12000 \: \text{bits}$$
$$ d_{prop} = \frac{L}{R} = \frac{12000}{(4 \cdot 10^{6})} = 0.003 \: \text{s} = 3 \: \text{ms} $$
$$ \text{Time it takes for packet 1 to arrive} =  2 \: \text{ms} + 3 \: \text{ms} = 5 \: \text{ms} $$
$$ \text{Time it takes for packet 2 to arrive} = 3 \: \text{ms} + 3 \: \text{ms} = 6 \: \text{ms} $$

Since the difference in time between the two arrival times of the packets of data are of the order of milliseconds and milliseconds are much larger than microseconds, it means that the first set of packets should finish processing well before the second set arrives. Therefore, there will be no queuing delay occurring at router A.

## **Ch. 1.8. (15 points)  
**Consider a user who needs to upload 1 GB of data to a server, where G is SI standard (base 10) 109 and not binary (base 2) 230 = 10243. The user lives in a small town where only 56 kbps dial-up access is available. A bus visits the small town once a day from the closest city 150 km away and stops in front of the user’s house. The bus has a 100 Mbps Wi-Fi connection. It can collect data from users in rural areas and transfer them to the Internet through a 1 Gbps link once it gets back to the city. Suppose average speed of the bus is 60 km/h.

### **a)** How long is the upload time when using dial-up internet access?  
### Svar


### **b)** How long is the upload time when using the bus?  
### Svar

$$ \text{The time  taken by **bus** from Users house to **Town** is} = \frac{150 \: km}{60 \: km/h} = 2.5 \: hours = 9000 \: \text{seconds} $$

Since The users data to be **transmitted** over to the server = 1 GB

$$ 1 \: \text{GB} = 1024 \: \text{MB} $$
$$
1024 \: \text{MB} \cdot 8 = 8192 \: \text{Mbits}
$$
$$ \frac{8192 Mb}{100 Mbps} =  81.92 \: \text{seconds} = 1 \: \text{Minute} \: 21.92 \: \text{seconds}$$

### **c)** What is the fastest way for the user to transfer the data to the server?
### Svar



## **Ch. 1.9. (10 points)  
**A few questions from the history of the Internet.

### **a)** What historical event took place on January 1, 1983?  
Første gang internet ble "skrudd på" (IPS protokollen kjørte) via ARPANET, av US Department of Defence. 

January 1, 1983 saw the official deployment of TCP/IP as the new standard host protocol for ARPAnet (replacing the NCP protocol). The transition [RFC 801] from NCP to TCP/IP was a flag day event—all hosts were required to transfer over to TCP/IP as of that day. 

### **b)** Who is known as the inventor of the World Wide Web (WWW).  

### **c)** Which protocols did this person specify?
