# Develop By : DHINESH.P
# Reg No : 212222043001
# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
## CLIENT
![cn pic11](https://github.com/dhinesh00406/3b_CHAT_USING_TCP_SOCKETS/assets/147149471/0d1a4f31-1a7e-4322-8a92-301e9a1d7a39)


## SERVER
![cn pic13](https://github.com/dhinesh00406/3b_CHAT_USING_TCP_SOCKETS/assets/147149471/9fb8d869-cbf1-418a-8179-03f6764c5bcb)

## RESULT

Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
