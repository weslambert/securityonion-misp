# securityonion-misp
**Grab NIDS rules generated from a MISP instance and use them in Security Onion:**   
See: https://www.circl.lu/doc/misp/automation/#nids-rules-export

- Clone the repo:   
`git clone https://github.com/weslambert/securityonion-misp`   
- Run the setup script:   
`sudo securityonion-misp/setup-misp`   
- Update rules (if desired):   
`sudo rule-update`   
- Confirm rules in place:    
`grep -i misp /etc/nsm/rules/downloaded.rules`    
