# Partner Power Hour # 3 - 2/6/2021 

**Presenter: Alex Gounares**
**Topic: Cyber Security - Zero Trust**

Alex Gounares is the CEO of Polyverse Corporation - a cybersecurity company. He talks about Zero Trust Everything - assume cybersecurity is imperfect. There are more and more people work from home because of pandemic and this makes more computers become the target.

- Polymorphic Principle
  - Assume imperfections and make exploiting flaws more difficult.
  - Security = entropy > information leakage
  - Example: Password and Multi-Factor Auth
- Zero Trust Networking
  - Leakage: with a traditional perimeter firewall, one breach gives access to the corporate network - often the entire network
  - Entropy: individually authenticate and route every user for every service
- Zero Trust Data
  - Leakage: Encryption is only as good as the key management system. Stolen keys = stolen data
  - Entropy: Blockchains and similar approaches created auditable, distributed "chains of trust". One compromised key cannot break the full chain.
- Zero Trust Software 
  - Leakage: Attackers know every single bit in every binary of your software - including the buts.
  - Entropy: Change the software! Polymorphic binaries and script engines change faster than can be discovered. Attacks fail, even on unpatched systems.

Every API call leaks information and that's where it's easy to hack computers. A system can be taken over in as few as 4000 API calls.