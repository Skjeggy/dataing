
![[IKT207_asgmt1_review#Definisjon (chatgpt - about ransomware)]]


# Introduction - what is ransomware
Ransomware is a type of malware that aims to encrypt a victim's files in such a way that their computer, or access to their files, is disabled. A message is then displayed, serving as the ransom note, giving detailed instruction as to how the victim can retrieve their computer or files. Usually this is done by paying a ransom to the criminals behind the attack. [[@okaneEvolutionRansomware2018]]


# A brief history of ransomware
The founder of ransomware, Joseph Popp, originally created a Trojan with a ransomware called "AIDS" in 1989. He used a floppy disc as an attack vector and after it encrypted the victim's C: drive, it demanded 189 USD to be sent to a postbox in Panama. There were a number of problems with this, including a low number of reachable victims, a weak infection method, a weak encryption and the payment method.  Safe to say, the world has moved on since then. 

In modern times, the use of ransomware has exploded with a 600% increase ransomware "families" betewen 2013 and 2018. The internet has created a target rich environment and an easy attack vector for such malware. Furthermore, encryption software has lowered the entry skills required and cryptocurrencies provide easy and anonymous payment methods to the advantage of the attacker. There is also the fact that most businesses, organizations and people now store their data electronically [[@okaneEvolutionRansomware2018]]

# Ransomware in healthcare
A major turning point for cybersecurity in healthcare was in 2016 when the Hollywood Presbyterian Medical Center was targeted by ransomware and ended up paying $17,000 to restore its data. The same year, 44% of all healthcare related cyber incidents were caused by ransomware. Later in 2017, the WannaCry ransomware worm taking advantage of the EternalBlue exploit, ended up shutting down several UK hospitals [[@wassermanHospitalCybersecurityRisks2022]] + (hold the line). In 2020, the allegedly first death caused by a ransomware attack occurred in Germany (wired artikkelen). 

## Consequences 

### Financial
The consequences for the healthcare industry are serious. The financial costs of data breaches in healthcare were estimated to be on average worldwide $7.13 million in 2020, compared to $3.86 million as the world average for all industries worldwide.

### Loss of data
It has been estimated that 21% of attacks cause data breaches. The problem with these breaches is that medical data cannot simply be "reset". The data can also be sold to other malicious actors, even when decrypting it for the victim, making it permanently compromised. In addition, once access is gained by attackers they can  install malware to keep the systems infected for future attacks. Even paying the ransom does not guarantee a return of the data. 

### Reputation and physical harm
Finally, there are consequences related to decreased trust among patients and physical harm caused to them. As seen above, ransomware attacks can at worst be deadly to patients.

[[@wassermanHospitalCybersecurityRisks2022]]

## Why is healthcare especially vulnerable? 
There are several vulnerabilities in healthcare systems that are important to highlight. Interoperability, or the ability to share data between hospitals and other care providers, leads to more potential infiltration points. Out-of-date and unsupported operating systems and other systems, commonly seen in healthcare, also serve as major vulnerabilities. Furthermore, the focus in health organizations is understandably often on medical care and not cybersecurity. This, combined with a lack of resources (money, staff and expertise) provide several vulnerabilities to be exploited.

Practicing modern healthcare also requires a constant accessibility, both creating a vulnerability in terms of a constantly "open" network and increasing the probability that healthcare organizations will pay the ransom because of the urgent need for access to the data. 

Lastly, there is the threat from within. Unaware employees clicking phishing links or failing to adhere to cybersecurity protocols make up a significant part of enabling attacks. 


![[Pasted image 20230114130518.png]]



# Mitigation
In the early stages of an attack, removal of the malware can stop further damage to the data.

Proper backups are critical. Preferably offline, as not to be reached by the ransomware.

- Security updates.
- Education of personell 
- Mitigate spread


## File system defences against ransomware
A good backup is important for protecting against ransomware. For this reason, the ransomware usually targets the backups as well if it can reach them. Measures like limiting user access to backups and software related to backups might be effective measures. 

## File decryption and recovery

It is possible to use tools for decrypting and recovering files through software such as https://www.nomoreransom.org/en/index.html suggested by Nettvett.no.
