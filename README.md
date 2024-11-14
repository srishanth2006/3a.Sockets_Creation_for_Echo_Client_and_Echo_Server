# EX.NO:3a             CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## NAME: SRISHANTH J
## REG.NO:212223240160
## AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python</br>
2. Create a socket connection to using the socket module.</br>
3. Send message to the client and receive the message from the client using the Socket module in
 server.</br>
4. Send and receive the message using the send function in socket.</br>

## PROGRAM:
### Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server
```
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
### Client
<img width="514" alt="image" src="https://github.com/user-attachments/assets/b61c9476-6150-45dc-8496-dc711f3666a8">


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
