# 3b.CREATION FOR CHAT USING TCP SOCKETS
### NAME : CHOLIMGAPURAM SAI LIKITHA [212224230046]
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

### SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```

## OUPUT
### CLIENT
![Screenshot 2025-04-28 180956](https://github.com/user-attachments/assets/8d8b7744-d5cc-49e8-a2df-77c5946d8abe)

### SERVER
![Screenshot 2025-04-28 181006](https://github.com/user-attachments/assets/bd4f3e45-c929-4856-b517-b26bc8a6e48f)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
