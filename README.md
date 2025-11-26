# 3b.CREATION FOR CHAT USING TCP SOCKETS
# AIM
To write a python program for creating Chat using TCP Sockets Links.
# ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
# PROGRAM
## Server.py
~~~py
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
~~~

## Client.py
~~~py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
~~~
## OUPUT

<img width="1025" height="244" alt="image" src="https://github.com/user-attachments/assets/4b05d0f2-8c69-4abc-8313-51b1c9e01432" />

<img width="1065" height="216" alt="image" src="https://github.com/user-attachments/assets/40b88bad-1e07-4dbf-a9ac-9b7c4ab86608" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
