# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server.
4. Send and receive the message using the send function in socket.
## PROGRAM:
## Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## Server:
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
## OUTPUT:
## Client:
![Screenshot 2024-04-03 103549](https://github.com/HEMAKESHG/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870552/5d0ca1cc-a24b-4ae7-90ad-8ed58a196a53)
## Server:
![Screenshot 2024-04-03 103530](https://github.com/HEMAKESHG/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870552/30dd1910-38f4-43ed-af31-6837aed9feac)

## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
