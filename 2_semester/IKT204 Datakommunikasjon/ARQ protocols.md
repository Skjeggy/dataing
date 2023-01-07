(Automatic Repeat reQuest) protocolls. Se [[ACK]]. 

Before developing a protocol for reliably communicating over such a channel,
first consider how people might deal with such a situation. Consider how you yourself might dictate a long message over the phone. In a typical scenario, the message taker
might say “OK” after each sentence has been heard, understood, and recorded. If the
message taker hears a garbled sentence, you’re asked to repeat the garbled sentence.
This message-dictation protocol uses both **positive acknowledgments** (“OK”) and
**negative acknowledgments** (“Please repeat that.”). These control messages allow
the receiver to let the sender know what has been received correctly, and what has
been received in error and thus requires repeating. In a computer network setting,
reliable data transfer protocols based on such retransmission are known as [[ARQ protocols]].

Fundamentally, three additional protocol capabilities are required in ARQ pro-
tocols to handle the presence of bit errors:

### Error detection. 
First, a mechanism is needed to allow the receiver to detect when
bit errors have occurred. Recall from the previous section that UDP uses the Inter-
net checksum field for exactly this purpose. In Chapter 6, we’ll examine error-
detection and -correction techniques in greater detail; these techniques allow the
receiver to detect and possibly correct packet bit errors. For now, we need only
know that these techniques require that extra bits (beyond the bits of original data
to be transferred) be sent from the sender to the receiver; these bits will be gath-
ered into the packet checksum field of the rdt2.0 data packet.

### Receiver feedback. 
Since the sender and receiver are typically executing on dif-
ferent end systems, possibly separated by thousands of miles, the only way for
the sender to learn of the receiver’s view of the world (in this case, whether or not
a packet was received correctly) is for the receiver to provide explicit feedback
to the sender. The positive (ACK) and negative (NAK) acknowledgment replies
in the message-dictation scenario are examples of such feedback. Our rdt2.0
protocol will similarly send ACK and NAK packets back from the receiver to
the sender. In principle, these packets need only be one bit long; for example, a 0
value could indicate a NAK and a value of 1 could indicate an ACK.

### Retransmission. 
A packet that is received in error at the receiver will be retrans-
mitted by the sender.