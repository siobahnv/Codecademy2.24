# Codecademy Coursework

## User Authentication & Authorization in Express
authentication <br>
authorization <br>
OWASP, Open Web Application Security Project, https://owasp.org/ <br>
encrytion <br>
_penetration testing_, or pen testing, or ethical hacking <br>
CIA triad, Confidentiality, Integrity, and Availability <br>

### OWASP Top Ten
1. _injection_ <br>
sanitizing and validation <br>

2. "_Broken Authentication_ is a broad term for vulnerabilities that allow attackers to impersonate other users." <br>
data breach <br>
_fullz_, collection resold stolen information, including personal information <br>

3. "_Sensitive Data Exposure_ refers to insufficient protections being put in place for" sensitive data. <br>

4. XML External Entities (XXE), "is a type of vulnerability that allows maliciously crafted data to produce unintended behavior on the backend of a website." <br>
XML is a markup language <br>
XML file <br>
XML processor <br>
"the simplest solution is to not use XML" <br>

5. "_Broken Access Control_ is when authorization is improperly enforced, allowing users access to privileges they should not have." <br>

6. _Security Misconfiguration_ <br>
Intrusion Detection Systems (IDSs) <br>

7. "_Cross-Site Scripting (XSS)_ is a web vulnerability that targets the browser-side of the website, rather than the server-side." <br>

8. "_Insecure Deserialization_ is when *this* process can be exploited to cause unintended behavior." <br>
serialization: "turning an object within a program into formatted data" <br>
deserialization: "turning formatted data into an object within code" <br>
"the easiest and most reliable way is to just not deserialize external data" <br>

9. "_Using Components with Known Vulnerabilities_ means using software or package versions that are known to be vulnerable." <br>
Common Vulnerabilites and Exposures systems, https://cve.mitre.org/ (redirects...) >> https://www.cve.org/ <br>
"Usually, this can be prevented by keeping software...up to date." <br>

10. "_Insufficient Logging and Monitoring_ refers to an overall lack of tools that monitor, record, and report events within a system." <br>

### Authentication vs Authorization vs Encryption
"Authentication is the verification of _who you are_." <br>
Three Factors: Knowledge, Possession, Inherence <br>
_Single-Factor Authentication_, relies on a single factor, vs _Multi-Factor Authentication_ <br>
_Multi-Factor Authentication_ vs _Multi-Step Authentication_ <br>

"Authorization is the verification of _what you are allowed to do_." <br>

"Encryption is the process of transforming data into a format that is unreadable unless you have the correct _key_ to decrypt it." <br>
Two main types: Symmetrical vs Asymmetrical Data Encryption <br>
"Symmetric encryption uses the same key to encrypt and decrypt data." <br>
"Asymmetric encryption uses separate keys for encryption and decryption." <br>

#### Evolution of Authentication
Been around a long time, such as passphrases (*knock knock* Who goes there?); from passwords and printed IDs to complex systems. <br>

#### Basic Authentication 
Pattern: challenges and responses <br>
Catergories: knowledge-based, possesion-based, inherence-based <br>
Knowledge: something you know <br>
Possesion: something you have <br>
Inherence: something you are <br>

#### Usernames and Passwords
Early systems password-based in plain text. <br>
Current systems are more complex and the current standard for password storage is to use salted hashes. <br>
Cryptography <br>

#### One-Time Passwords & MFA
The One-Time Password, or OTP, possession-based <br>

#### PKI: Authenticating the Authenticator
Public-Key Infrastructure, or PKI, is a system that designates trusted authorities; verification <br>

#### Single Sign-On & OAuth2
Single Sign-On, also known as SSO, can auttenticate with one service and use to authenticate to other services <br>
The current standard for SSO is OAuth 2.0. <br>

### Session Authentication in Express
