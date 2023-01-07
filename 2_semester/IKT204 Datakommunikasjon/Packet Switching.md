
[[Packets]] are transmitted over each communication link at a rate equal to the full transmission rate of the link. So, if a source end system or a packet switch is sending a packet of L bits over a link with transmission rate R bits/sec, then the time to transmit the packet is L / R seconds.

In contrast to [[Circuit Switching]], consider what happens when one host wants to send a packet to
another host over a packet-switched network, such as the Internet. As with circuit
switching, the packet is transmitted over a series of communication links. But dif-
ferent from circuit switching, the packet is sent into the network without reserving
any link resources whatsoever. If one of the links is congested because other packets
need to be transmitted over the link at the same time, then the packet will have to
wait in a buffer at the sending side of the transmission link and suffer a delay. The
Internet makes its best effort to deliver packets in a timely manner, but it does not
make any guarantees.

## See also:
[[Circuit Switching]]

[[Multiplexing og demultiplexing + litt UDP og TCP]]