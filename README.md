# VULNHUB-kioptrixLevel1-
kioptrix Level 1 beginner level

             ENUMERATION 
............................................
As always we start by doing ENUMERATION of Machines
.........
nmap -sC -sV --script vuln -oN NMAP.txt 192.168.221.130

https://github.com/DAVINDOdavidOLEX/VULNHUB-kioptrixLevel1-/blob/main/NMAP.txt


nikto -h 192.168.221.130 2>/dev/null |tee nikto.txt

https://github.com/DAVINDOdavidOLEX/VULNHUB-kioptrixLevel1-/blob/main/nikto.txt

dirbuster 2>/dev/null |tee dirbuster.txt


https://github.com/DAVINDOdavidOLEX/VULNHUB-kioptrixLevel1-/blob/main/dirbuster.txt


gobuster dir -u http://192.168.221.130 -w /usr/share/wordlists/dirb/common.txt 2>/dev/null |tee gobuster.txt

https://github.com/DAVINDOdavidOLEX/VULNHUB-kioptrixLevel1-/blob/main/gobuster.txt

gobuster dir -u http://192.168.221.130 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt 2>/dev/null |tee gobuster1.txt

https://github.com/DAVINDOdavidOLEX/VULNHUB-kioptrixLevel1-/blob/main/gobuster1.txt

enum4linux -a 192.168.221.130

https://github.com/DAVINDOdavidOLEX/VULNHUB-kioptrixLevel1-/blob/main/enum4linuxENUMERATErpcANDsmbANDnmbANDnet.txt

FINAL DOCUMENT FROM ENUMERATION 


https://github.com/DAVINDOdavidOLEX/VULNHUB-kioptrixLevel1-/blob/main/Enumeration.txt



RESEARCH FOR VULNERABILITIES 



This research can be done in two ways which are offline and online research 
           OFFLINE RESEARCH 

Here a tool called searchsploit become useful

From my directory 
    searchsploit 

https://github.com/DAVINDOdavidOLEX/VULNHUB-kioptrixLevel1-/blob/main/ResearchVULNERABILITY.txt

Other versions of this ip address(192.168.221.130) seem not interested 

       ONLINE RESEARCH 
I didn't use this but here you can just Google your version of service for vulnerabilities 
      two things that are useful in online research are exploitdb(https://www.exploit-db.com/) and github resources 
           Others are cve(https://cve.mitre.org/) and so on.




EXPLOITATION STAGE





in this stage we test what we research if we fail we have to repeat to research or even to repeat/look deep into this ENUMERATION or loo
 
  From our research we have 2 exploitation 
First that it bring success is through samba 2.2.1a vulnerabilities in which it is exploited through the use of msfconsole as searchsploit, it shows(extension. rb)
      



Other exploitation, it seems you have to setup some few things 





