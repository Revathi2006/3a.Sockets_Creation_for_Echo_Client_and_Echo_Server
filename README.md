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

## server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8080))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

```
## OUPUT
## client.py
<img width="602" height="267" alt="image" src="https://github.com/user-attachments/assets/921cd3b6-97f4-4d6c-92c9-3820149725ce" />

## server.py
<img width="638" height="153" alt="image" src="https://github.com/user-attachments/assets/b5563be8-f83f-4b6e-9dd2-fe3c3a61abe1" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
