# TCP CLIENT SIDE 

import socket 

#Create a client side ipv4 - AF_INET , TCP - SOCK_STREAM 
client_socket = socket.socket(socket.AF_inet,socket.SOCK_STREAM) 

# CONNECT SOCKET TO A SERVER LOCATED AT GIVEN IP , PORT


client_socket.connect((socket.gethostbyname(socket.gethostname()),12345))

# RECERIVE MESSAGE FROM THE SERVER - specifiy max number of bytes to receive

message = client_socket.recv("bytes")
print(message)
print(type(message))


client_socket.close()
