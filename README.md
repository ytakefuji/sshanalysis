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

The following graphs show the number of attacks and top 10 IPs. 
The larger circle, the more number of attacks.
Although, country names were embedded on each graph.
No one knows whether IPs are true, spoofed, or springboarded.

sshanalysis can generate all IPs with the number of recorded attacks.
sshanalysis can generate top 10 IPs associated with locations (country names).

<img src='https://github.com/ytakefuji/sshanalysis/raw/main/neuro.png' width=640 height=480>
<img src='https://github.com/ytakefuji/sshanalysis/raw/main/gpu1.png' width=640 height=480>
<img src='https://github.com/ytakefuji/sshanalysis/raw/main/gpu2.png' width=640 height=480>
<img src='https://github.com/ytakefuji/sshanalysis/raw/main/gpu3.png' width=640 height=480>
<img src='https://github.com/ytakefuji/sshanalysis/raw/main/gpu4.png' width=640 height=480>

# sshanalysis.py
sshanalysis.py consists of three modules. 
The first module generates a csv file containing the number of recorded attacks 
against the sorted IP addresses by using a /var/log/auth.log file. 
The second module is for generating the country names associated with the captured IP addresses in auth.log. 
And the last module is for drawing a graph.

The graph contains top 10 IPs with country names where the radius of circles indicate the number of attacks. The larger the circle, the more attacks against a ssh server.

We don't know whether captured IPs are true, spoofed, or springboarded.

