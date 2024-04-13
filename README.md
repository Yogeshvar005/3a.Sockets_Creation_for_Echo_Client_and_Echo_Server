# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client.py:
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())  
```
### Server.py:
```python
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
## OUPUT:
### Client.py
<img width="840" alt="image" src="https://github.com/Ganesh23013987/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147473768/1f2354fb-0a34-4612-9f73-caf15a303e55">

### Server.py
<img width="840" alt="image" src="https://github.com/Ganesh23013987/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147473768/5aae1083-1c71-4cbc-9610-7ca057a7b387">





## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
