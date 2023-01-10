

If an arriving packet needs to be transmitted onto a link but
finds the link busy with the transmission of another packet, the arriving packet must
wait in the [[Output Buffer]]. Thus, in addition to the [[Store-and-Forward Transmission|store-and-forward delays]], packets
suffer output buffer queuing delays. These delays are variable and depend on the
level of congestion in the network. Since the amount of buffer space is finite, an
arriving packet may find that the buffer is completely full with other packets waiting
for transmission. In this case, **packet loss** will occur—either the arriving packet or
one of the already-queued packets will be dropped.