#### Iteration 01
Notes from Ben Eater's youtube video on networking

1. Basic understanding of how we can different voltages through pair of wires in the ethernet cable to transmit data.
2. Referring to each state as a symbol baud is defined as the number of symbols / sec.
3. At high level optic fiber works on the same principle.
4. The sender and receiver need to have their clocks or their clock rates synchronized to transfer data correctly
5. Protocols such as Manchester coding is used to "frame" up bytes of data by repeating agreed pattern
6. Q - Big ending little endian encoding plays a part but but why is unclear +   
7. its the transition that is counted as a data.
8. Ethernet frame --> TCP/UDP frame --> IP frame-->HTTP frame
9. ARP -address resolution protocol - used to associate the IP address to the MAC(media access control) address
  - Host broadcasts the Destination IP address  which is matched by the local router (e.g. 255.255.255.0/24 means you match the 1st 24 bits)
  - router then works through DNS to get the mac address of the Destination
10. TCP connection is established
11. HTTP packets are framed within the TCP frame.  



IP Datagram header
1. Minimum 20 bytes in length
![IP Datagram Header](https://github.com/dpillai/notes/images/main/ip-datagram-header.png?raw=true)
t