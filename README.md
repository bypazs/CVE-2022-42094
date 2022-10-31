# Backdrop CMS version 1.23.0

### Vulnerability Explanation:
Backdrop CMS version 1.23.0 was discovered to contain a stored cross-site scripting (XSS) vulnerability via the `Card` content.

### Attack Vectors:
The attacker must post something on the "Card content" and insert the XSS payload at the "Body" input, and pick the Raw HTML Editor in order to exploit the stored XSS. The XSS payload will be launched immediately after save.

### Affected: 
- http://ip_address/backdrop/node/add/card

- POST /backdrop/node/add/card 

### Payload :
- `<img src=x onerror=confirm('Grim-The-Ripper-Team-by-SOSECURE-Thailand')>`

### Tested on: 
1. Backdrop CMS version 1.23.0 (https://github.com/backdrop/backdrop/releases/tag/1.23.0)

2. Firefox version 105

### Steps to attack:
1. Enter your username and password; the account must have admin privileges
2. Select Content > add content > Card
3. Enter information into the form provided.
4. Enter the XSS payload in the Body field.
5. Choose "Raw HTML" Editor and Save.
5. The XSS payload will run immediately.

### Discoverer:
:shipit: Grim The Ripper Team by SOSECURE Thailand

### Medium:
- 

### Disclosure Timeline:
- 2022–09–27: Vulnerability discovered.
- 2022–09–27: Vulnerability reported to the MITRE corporation.
- 2022–10–15: CVE has been reserved.
- 2022–10–31: Public disclosure of the vulnerability.

Reference:

1. 

2.

3. https://github.com/backdrop/backdrop/releases/tag/1.23.0

4. https://backdropcms.org

