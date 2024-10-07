# 4.Execution_of_NetworkCommands
### NAME: KARTHIKEYAN R
### REG.NO:212222240046

## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>


## Output
### ipconfig
![Ipconfig](https://github.com/user-attachments/assets/0b63a53c-9a95-4a8c-842c-166d209ad9f6)
### ping
![ping](https://github.com/user-attachments/assets/f2c5105a-ca6e-4dda-946c-3d036f8d8e04)
### netsat
![Netstat](https://github.com/user-attachments/assets/b0b22150-6f1d-437b-8166-bce24d6e2613)
### nbtstat
![Nbtstat](https://github.com/user-attachments/assets/2876e79f-6f27-4d04-9375-3bc158d2ee3b)
### nslookup
![nslookup](https://github.com/user-attachments/assets/0d000055-65df-4b4b-8ef8-0424f2aba222)
=======
## PROGRAM

## Ping command
## Client
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
## Server
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
## Tranceroute command
```
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
## OUTPUT
## Ping command
## Client
![image](https://github.com/Yuvasreemuthusamy/4.Execution_of_NetworkCommends/assets/144870887/a71fd251-4981-4a47-895e-397385132009)

## Server
![image](https://github.com/Yuvasreemuthusamy/4.Execution_of_NetworkCommends/assets/144870887/798a1a24-2784-46a9-916a-ec8552ecd907)

## Tranceroute command
![image](https://github.com/Yuvasreemuthusamy/4.Execution_of_NetworkCommends/assets/144870887/ce4aa790-9cc7-427a-8860-e4a5f40b1076)

## Result
Thus Execution of Network commands Performed 
