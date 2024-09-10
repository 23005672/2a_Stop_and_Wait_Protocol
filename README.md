# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
```
Developed by: RIYA P L
Reg no: 212223240141
```
## CLIENT: 
```
import socket 
s=socket.socket() 
s.listen(5) 
c,addr=s.accept() 
while True: 
    i=input("Enter a data: ") 
    c.send(i.encode()) 
    ack=c.recv(1024).decode() 
    if ack: 
        print(ack) 
        continue 
    else: 
        c.close() 
        break 
```
## SERVER: 
``` 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())
```
## OUTPUT
## CLIENT:
![Screenshot 2024-09-09 144659](https://github.com/user-attachments/assets/a77a6809-e0c3-4156-be10-9c0c5c3ce6f9)
## SERVER:
![Screenshot 2024-09-09 144732](https://github.com/user-attachments/assets/c47ef5fd-93f4-4e49-a369-fbd53aec786d)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
