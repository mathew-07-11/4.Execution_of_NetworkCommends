# 4.Execution_of_NetworkCommands
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

## Program

```
CLIENT
client.py
import socket
from pythonping import ping
s=socket.socket() s.bind(('localhost'8000)) s.listen(5) c,addr=s.accept()
while True: hostname=c.recv(1024).decode() try:
c.send(str(ping(hostname, verbose=False)).encode())
except KeyError:
c.send("Not Found".encode())

SERVER
server.py

import socket s=socket.socket() s.connect(('localhost',8000)) while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode())
print(s.recv(1024).decode())
```
## Output

NESTAT

<img width="802" height="374" alt="image" src="https://github.com/user-attachments/assets/f9260444-b38d-407d-ae17-2c3d38800593" />

IP CONFIGURAION

<img width="923" height="695" alt="image" src="https://github.com/user-attachments/assets/e7f272c9-08dc-471f-9713-6a8b8fc068c9" />

GET MAC

<img width="807" height="166" alt="image" src="https://github.com/user-attachments/assets/122d29de-0a8f-43d6-8cc1-1b684c127337" />

ARP

<img width="803" height="394" alt="image" src="https://github.com/user-attachments/assets/79c8ed3d-c0ee-488a-9658-e1f448ed2005" />

SYSTEM INFO

<img width="1180" height="907" alt="image" src="https://github.com/user-attachments/assets/010a8b67-85ce-4c15-8e6d-30be22fa1819" />

NBSTAT

<img width="1046" height="520" alt="image" src="https://github.com/user-attachments/assets/3a95d148-f496-42fc-979c-4bb2e1b23383" />

HOST NAME

<img width="1038" height="358" alt="image" src="https://github.com/user-attachments/assets/b8e0e418-214a-40ec-a777-5361d1e9125c" />

NS LOOKUP

<img width="693" height="149" alt="image" src="https://github.com/user-attachments/assets/25539a2c-f085-4f13-8e69-cace95a04154" />

PING

<img width="807" height="581" alt="image" src="https://github.com/user-attachments/assets/80c966fb-b39a-48c1-8cb7-36d8c102e687" />

TRACET

<img width="814" height="109" alt="image" src="https://github.com/user-attachments/assets/2bbf666a-3d59-47ff-a9d9-da5b24c5887c" />


## Result
Thus Execution of Network commands Performed 
