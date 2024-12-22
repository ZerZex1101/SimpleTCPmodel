# tcp server side 

import socket

# tcp ipv4 - AF_INET , TCP - SOCK_stream 
 
server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM) 

# IP adress dyanmically 
print(socket.gethostname()) # hostname
print(Socket.gethostbyname(socket.gethostname())) #ip of the given host name

#bIND   SOCKET TO TUPLE ( IP , PORT ) 
server_socket.bind((socket.gethostbyname(socket.gethostname()),12345))

#PUt the socket into listening mode for any possible connection 

server_socket.listen() 

# LIsten forever to acceot any incoming connection

while True:
    # Accept every single connection and store 2 peices of information
    
    client_socket,client_Address = server_socket.accept() 
    print(type(client_socket))
    print(client_socket) 
    print(type(client_addresses)
    print(client_addresses) 

    print(f"Connected to {client_address}!\n")
  
    client_socket.send("You are connected!".encode("UTF-8"))

    server_socket.close()
    break
