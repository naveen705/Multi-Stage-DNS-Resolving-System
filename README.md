# Multi-Stage-DNS-Resolving-System

In this application, we implemented three C++ programs, namely Client, Proxy
Server (which will act both as client and server) and DNS Server, which
communicate with each other based on TCP sockets.
The other two files are “database.txt” and “cache.txt”. The first file contains the
mapping of DNS to IP in the server while the later is used by the proxy to maintain
the same mappings, although the size of the cache is capped to 3


## How to Run

1. Compile and run all the 3 program files by command:
	g++ dns.cpp -o dns
	g++ proxy.cpp -o proxy
	g++ client.cpp -o client

2. Open new terminal in same directory and write command:
	./dns 8000
	(here 8000 is the dns port number and can be replaced with other port number also)

3. Open another new terminal in same directory and write command:
	./proxy 9000 127.0.0.1 8000
	(9000: port number of proxy, 127.0.0.1: Loopback address(IP address), 8000: port number of DNS server)

4. Open another new terminal in same directory and write command:
	./client 127.0.0.1 9000
	(9000: port number of the proxy server)

5. To run multiple clients, open new terminal for each client and run above command.

6. Select the options:
	(1) For domain name to ip conversion
	(2) For IP to domain name conversion


NOTE: The database.txt file is read by DNS server and is updated by system admin
	  The cache.txt file is updated by the Proxy server and it's size can changed by programmer.




## Screenshots

![s1](https://user-images.githubusercontent.com/15118630/189527463-2c903dc5-5eaf-43ed-9c04-d79e9d58dce5.png)
![s2](https://user-images.githubusercontent.com/15118630/189527466-35b92649-1dca-48f5-8b34-87115d5c32b2.png)
![s3](https://user-images.githubusercontent.com/15118630/189527472-7f167647-3edb-4cf5-9571-fd2d474d3699.png)
![s4](https://user-images.githubusercontent.com/15118630/189527488-bde29fac-3f67-473a-9517-ed3b3f250166.png)
![s5](https://user-images.githubusercontent.com/15118630/189527492-60515486-8c25-43a3-af5a-0a434b5d269f.png)

