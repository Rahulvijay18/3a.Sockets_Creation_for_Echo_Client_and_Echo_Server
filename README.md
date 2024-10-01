# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### Name : RAHUL VIJAY V
### Register No : 212223040164
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
### CLIENT:
~~~
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
~~~
### SERVER:
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
~~~
## OUPUT
### CLIENT:
![image](https://github.com/user-attachments/assets/678c965e-dcc1-4b91-9850-70050afb6ab8)

### SERVER:
![image](https://github.com/user-attachments/assets/4a069d3c-ce94-4c24-91e9-547d10ca0fea)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
