# cyber_defense
# Cryptographic Techniques

The technique used by the attack gang in the article ["49 Busted in Europe for Man-in-the-Middle Bank Attacks"](https://www.example.com) is content injection. According to MITRE ATT&CK, by injecting malicious content into systems through online network traffic, adversaries can gain access and maintain a continuous communication channel with victims. Alternatively, adversaries may initially access victims through compromised data-transfer channels where they can manipulate traffic and/or inject their own content. These compromised online network channels may also be utilized to lure victims to malicious payloads hosted on a compromised system (MITRE ATT&CK®, n.d.).

## TLS and SSL Protocols

One of the protocols responsible for securing data is TLS (and SSL). This protocol transmits data to the transport layer, allowing client and server applications to detect security risks like message tampering, interception, and forgery. Therefore, it helps protect the integrity, availability, and confidentiality of data, ensuring accuracy and trust in an ethical organization. 

In the article, it’s assumed the attack gang used man-in-the-middle techniques, including phishing and social engineering, to plant malware on the network, granting access to communications. They then sent phishing attacks to bank clients, using a fake webpage to transmit payments to an unintended location.

## Man-in-the-Middle and Compromised Website Attacks

The attackers were able to compromise the network using social engineering tactics, successfully injecting malware into the system. Since the gang gained access to all data and internal communications, they were able to recreate the website, representing the concept of a "man-in-the-middle" attack. They used existing website code but injected malicious elements such as JavaScript, iframes, and cross-site scripting, among other techniques frequently employed in such attacks. Per MITRE ATT&CK, this can be leveraged through credential access and collection. For example, by stealing access tokens, attackers can use a tactic called AADInternals, which is a PowerShell-based framework for enumerating and exploiting Active Directory and is publicly available on GitHub (MITRE ATT&CK®, n.d.).

The site would appear legitimate to customers unfamiliar with adversarial websites, allowing bad actors to intercept payments and redirect them for their ill-gotten gains. 

### Bank Client Education

In response to lessons learned from this case study, many banks and financial institutions now send periodic emails to educate clients. According to the article ("49 Busted in Europe for Man-in-the-Middle Bank Attacks", 2015), these emails include warnings about:

- Grammar errors and spelling mistakes in emails
- Avoiding email links; instead, going directly to the website’s URL
- Incorrect domain names, such as ".uk" or ".au" instead of the expected country code
- Login pages that appear altered or unfamiliar
- Login pages that are not encrypted, often indicated by a missing padlock or a red line through the browser’s icon

Although these measures are not foolproof, they provide a good starting point for customer education. It's important to take a moment to verify that things are correct, and if something seems off, always call the number on the back of your card. Many bad actors or career cybercriminals are constantly trying to steal personal information for data brokers and the black market.

## Preventative Solutions

There are many preventative solutions that could have been implemented, looking back retrospectively, such as monitoring for file creation, network traffic content, and process creation. For example, capturing socket information with a source/destination IP and port(s). Mobile security products can potentially detect rogue Wi-Fi access points if the adversary is attempting to decrypt traffic using an untrusted SSL certificate. Monitoring for newly constructed network connections that are sent or received by abnormal or untrusted hosts is another method (MITRE ATT&CK®, n.d.). Unfortunately, this information was not readily available for organizations at the time.

## Conclusion

In conclusion, the MITRE ATT&CK kill chain was not invented or fully developed and released to the public until May 2015. However, taking a closer look at previous attacks and conducting incident postmortems throughout an organization’s tenure could have been common practice to understand what went wrong and how to follow up on lessons learned. Cybersecurity is a dynamic field, constantly evolving, and lessons build on our understanding of the CIA Triad, as well as the growth of the Internet of Things (IoT).
