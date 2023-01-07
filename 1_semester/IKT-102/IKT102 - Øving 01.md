## Hva er et system call ? 
[[System call]]
Et system call er en måte for programmer i user-space å interface med kernel space for å "obtain services". Det er altså en procedure call som har muligheten til å bytte fra user mode til kernel mode.  



## Hva er POSIX ? 
[[POSIX]]

POSIX henviser til et standard sett med system calls (International Standard 9945-1). Denne standarden spesifiserer et sett med "procedures that a conformant system must supply". Det bemerkes at alle disse "procedures" trenger ikke å være system calls eller library calls dersom man kan gjøre en procedure i user-space for av performance reasons. I de fleste tilfeller vil dog POSIX procedures være system calls. 

Kapittel 1.6 System calls (s.50-53)


## Hva er multiprogramming ? 
[[multiprogramming]]

Monoprogramming er når en CPU kjører et og et program om gangen, og kun holder et program i minnet om gangen. Til forskjell fra dette er multiprogramming når en CPU laster inn flere programmer i minnet og deretter kjører dem paralellt og bytter mellom dem slik at CPU'en kan unngå idle time. 


## Difference between user and kernal space ? 

User space er den delen av systemet hvor brukere fritt kan gjøre endringer, kjøre programmer osv.

Kernel space er den delen av systemet som tilhører operativsystemet. Her har ikke brukere (aka users) tilgang til å gjøre endringer eller bruke ressurser uten spesifik tillatelse fra operativsystemet. Disse tillatelsene får man som bruker gjennom å bruke system calls. Det er gjerne programmene som gjennomfører system calls. 