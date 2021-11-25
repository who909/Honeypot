# Honeypot Assignment

**Time spent: 15 hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?

MHN admin machine is hosted on Azure while honeypot is hosted on AWS. The only modification I made to the network settings was to add incoming rules.

<img src="mhn-admin.gif">

### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?

VM was exposed to internet due to Dinoaera's actions; Many ports were discovered to be open and exploitable by an NMAP scan. The goal is to get hackers to provide malware for analysis.

<img src="dionaea-honeypot.gif">

### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?

By creating a backup of MongoDB, we can see a list of attacks. The record consists of IP addresses, ports, and the protocols used for the attack. 

*Be sure to upload session.json directly to this GitHub repo/branch in order to get full credit.*

## Notes

I had a couple of problems that made the assignment longer than it should.

1. Google cloud did not want to take my payment. I used Paypal, debit, and credit cards, but google gave an error every time. 
2. AWS worked fine until I had two machines. The first machine will lose connection after the second machine gets created. The first will still be running and working fine, but SSH or EC2 instance connect will not work at all. The main issue was trying to get the session.json file for the first machine.
3. Azure works fine for the Mhn-admin but not for honeypot since they block all inbound and outbound connections. 

After combing AWS and Azure, I was able to complete the assignment. 

Describe any challenges encountered while doing the assignment.
