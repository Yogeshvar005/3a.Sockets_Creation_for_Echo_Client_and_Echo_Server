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
![image](https://github.com/Yogeshvar005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113497367/021a651f-b8ed-45fd-a633-d88edbba5423)


### Server.py
![image](https://github.com/Yogeshvar005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113497367/578187f7-1eb6-44b2-b059-05fc57945c2d)






## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
