Store-and-forward transmission means that the packet switch must receive
the entire packet before it can begin to transmit the first bit of the packet onto the
outbound link.


## Store-and-Forward Delay
Det er interessant å regne ut Delay fra start til slutt: 

$$ D_\text{end-to-end} = N \frac{L}{R} $$

(D = delay, N = amount of links, L = size of packet, R = Transmission rate for the links)

You may now want to try to determine what the delay would be for P packets sent
over a series of N links.


## Other delays
OBS: Kan være andre delays, som f.eks:

[[Queuing Delays]]