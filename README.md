# SSH Brute Force Detection — Home SOC Lab

## Objective
Simulate a real-world SSH brute force attack and perform log analysis 
and incident response in a home lab environment.

## Tools Used
- VMware
- Kali Linux (Attacker)
- Ubuntu (Victim)
- Hydra
- UFW Firewall

## What I Did

### 1. Lab Setup
- Configured two virtual machines — Kali Linux as attacker 
  and Ubuntu as victim
- Connected both machines on isolated network in VMware

### 2. Attack Simulation
- Used Hydra on Kali Linux to simulate 1000+ SSH brute force attacks
- All attempts failed due to strong password

### 3. Log Analysis
- Analyzed /var/log/auth.log on Ubuntu
- Used grep to filter failed login attempts
- Identified repeated failed attempts from single IP

### 4. Incident Response
- Blocked attacking IP using UFW firewall
- Verified block by attempting SSH connection again
- Access denied even with correct credentials

## Key Learnings
- How brute force attacks work in real environment
- How to analyze auth.log for suspicious activity
- How to use UFW for incident response
