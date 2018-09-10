# securityonion-misp
**Grab NIDS rules and Bro Intel generated from a MISP instance and use them in Security Onion:**   
See: https://www.circl.lu/doc/misp/automation/#nids-rules-export

Prerequisites:   
- Security Onion (installed,configured)
- MISP Instance and API Key   
  

Download and Configure (on Master or Standalone)
- Clone the repo:   
`git clone https://github.com/weslambert/securityonion-misp`   
- Run the setup script:   
`sudo securityonion-misp/so-misp-setup`   
- Update rules (if desired):   
`sudo rule-update`   
- Confirm rules in place:    
`grep -i misp /etc/nsm/rules/downloaded.rules`    
- Confirm Bro Intel in place:    
`cat /opt/bro/share/bro/intel/misp-intel.dat`

A cron job will run every morning at 6:01AM to download new NIDS rules and Intel.
