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

## server

~~~
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

## client

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
<img width="1862" height="433" alt="548634274-d466a924-7ec1-4b79-a9d4-8a7f76a36a48" src="https://github.com/user-attachments/assets/83cb12ad-cc72-4187-9096-f393411a8f88" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
