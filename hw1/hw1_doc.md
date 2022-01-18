# Run the homework
From the main directory use `kathara lstart`.
To stop use `kathara lclean`
# Try the network
To try that all is ok, ping the address of some node.
## TCP connection
To setup a tcp connection on port 8080 and write the result in tcp.pcap, use the command `nc -l -p 8080` on pc2 and `nc 10.30.10.50 8080` on s2 where 
`10.30.10.50` is the address of pc2 (could be different). So in r2 terminal run `tcpdump -w shared/tcp.pcap` to write on file teh connection. Write "hi_tcp" in pc2 and check that you can see the message in s2. 
## UDP connection
To setup a udp connection on port 9000 and write the result in udp.pcap, use the command `nc -l -p 9000 -u` on s2 and `nc  -u 10.0.3.94 9000` on pc2 where `10.0.3.94` is the address of s2. So in r2 terminal run `tcpdump -w shared/udp.pcap` to write on file the connection. Write "hi_udp" in pc2 and check that you can see the message in s2. 

Open .pcap files with [Wireshark](https://www.wireshark.org/).
