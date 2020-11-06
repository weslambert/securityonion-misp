# securityonion-misp
**Grab NIDS rules and Zeek Intel generated from a MISP instance and use them in Security Onion:**   
See: https://www.circl.lu/doc/misp/automation/#nids-rules-export

Prerequisites:   
- Security Onion (installed,configured)
- MISP Instance and API Key   
  

Download and Configure (on Master or Standalone)
- Clone the repo:   
`git clone -b so2 https://github.com/weslambert/securityonion-misp`   
- Run the setup script:   
`sudo securityonion-misp/so-misp-setup`   
- Update rules (if desired):   
`sudo rule-update`   
- Confirm rules in place:    
`grep -i misp /opt/so/rules/nids/all.rules`    
- Confirm Zeek Intel in place:    
`cat /opt/so/conf/zeek/policy/intel/misp-intel.dat`

A cron job will run every morning at 6:01AM to download new NIDS rules and Intel.
