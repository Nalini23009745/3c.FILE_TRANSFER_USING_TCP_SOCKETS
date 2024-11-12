# 3c.CREATION FOR FILE TRANSFER USING TCP SOCKETS
## AIM
To write a python program for creating File Transfer using TCP Sockets Links
## ALGORITHM:
1. Import the necessary python modules.
2. Create a socket connection using socket module.
3. Send the message to write into the file to the client file.
4. Open the file and then send it to the client in byte format.
5. In the client side receive the file from server and then write the content into it.
## PROGRAM
## Client:
```
import socket
s= socket.socket()
host=socket.gethostname()
port=60000
s.connect((host,port))
s.send("Hello server!".encode())
with open("received_file","wb") as f:
    while True:
        print("receiving data...")
        data=s.recv(1024)
        print("data=%s",(data))
        if not data:
            break
        f.write(data)
f.close()
print("Successfully get the file")
s.close()
print("connection closed")
```

## Server:
```
import socket
s= socket.socket()
host=socket.gethostname()
port=60000
s.connect((host,port))
s.send("Hello server!".encode())
with open("received_file","wb") as f:
    while True:
        print("receiving data...")
        data=s.recv(1024)
        print("data=%s",(data))
        if not data:
            break
        f.write(data)
f.close()
print("Successfully get the file")
s.close()
print("connection closed")
```
## OUPUT
![CN EX3C0](https://github.com/user-attachments/assets/a7406551-9241-44ee-804f-51057fcfbc86)

## RESULT
Thus, the python program for creating File Transfer using TCP Sockets Links was 
successfully created and executed.
