# sshanalysis
In 2021, 100% of the world’s top 500 supercomputers run on Linux.

96.3% of the world’s top 1 million servers run on Linux.

90% of all cloud infrastructures operate on Linux.

There are well over 1 billion sites on the world wide web.

According to wappalyzer.com, world wide web servers run on Apache 41%, Nginx 39%, IIS 7%, 
and LiteSpeed 5% respectively.

Apache and Nginx are based on open-source software.

Without Linux and open source software, the Internet would not exist.

SSH is now used by almost every data center in the world and more than half of the world's Web servers are managed using SSH.

Malicious attackers have been using true IP (internet protocol) addresses, spoofed IPs, and
springboard hosts's IPs.

Using the mixed IPs can cause DDoS (Distributed Denial of Service) attacks.

Currently it is hard to distinguish true IPs and spoofed IPs.

Therefore, it is hard to mitigate a DDoS attack.

A botnet (short for "robot network") is a network of computers infected 
with malware and under the control of a single attacking party.

This repository introduces a visualization tool for investigating IPs 
that are attacking a ssh server via ssh.

sshanalysis is a new tool that visualizes all the IPs and countries that are 
making ssh attacks against a ssh server.

In Debian and Ubuntu, /var/log/auth.log is a log file of attacks.

# auth.log analysis
With /var/log/auth.log read permission, any user can analyze IPs attacking against 
a ssh server.

<img src='' width= height=>

