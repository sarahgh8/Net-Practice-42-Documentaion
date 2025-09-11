# Net-Practice-42-Documentaion
A documentaion for the requirements of net-practice.

By `sghunmin`

## What is TCP/IP
TCP/IP is an internet protocol, basically a set of rules to transmit data, it's reliable when it comes to sending data but not fast as UDP, it's a part of the transport layer.

TCP/IP uses Three-Way handshaking, It's a precedure where two ends establish a connection to send one another a msg, in simple terms, three-way handshaking is a way to set up and prepare an enviornment to communicate with eachother.

It includes 3 steps:
1. The first host sends a syncronize msg to the other one to inform the send of a msg.
1. The other host sends a syncronize+acknowledgement signal.
1. The first host sends an acknowledgement signal.

## What is an IP address
Is a numerical label that identifies a device in a network as well as its address in the network.
```
A name indicates what we seek. An address indicates where it is. A route indicates how to get there."
```

## What is a subnet mask
A subnet mask is what represented as 0.0.0.0/24 or 255.255.255.0
is what identifies which part of the IP address represents the network address and what represents Host address, for example:
```
Suppose we have this IP address: 192.168.1.15 /24, The number 24
tells us that the first 24 bits belong to the netowrk address,
which is [192.168.1], and the rest is the Host (Device) address in the network [.15]
```
![Alt text](https://cdn-fainj.nitrocdn.com/HMhNvtGdkXCThiYKondeUNdKlFRQtHkp/assets/images/optimized/rev-50e11d1/www.auvik.com/wp-content/uploads/2024/05/AVK-2024-Subnet-Mask-Blog-Graphics_Graph-2-1024x392.jpg)

## How to calculate the number of IP knowing the SUBNET Mask
First Check the last number of the dotted subnet mask,
or the /NUMBER notation, basically it tells you how many
bits you have to get IP addresses...
```
 Saying that An IP address have 32 bits, if the subnet mask is /30 then we have 2 bits left to get a number of IP addresses, 2 bits make 4 numbers so in that case we have 4 IP addresses, and so on..
if we get the subnet mask as 255.255.255.252, then we do
256 - 252 = 4, then we have 4 IPs, 2 are usable.
``` 

### What about determining the network ID and the Broadcast
suppose we have `192.168.1.34/30` since that the subnet mask is 30, then we only have 4 IPs, the host ID is 34, we look for the nearest number to 34 that is divisible by 4, which is `32` that way we know that:
```
192.168.1.32 --> Network ID
192.168.1.33 --> usable IP
192.168.1.34 --> usable IP
192.168.1.35 --> Broadcast
```
Now we have 4 IPs and we know which are usable and which are not






### Notes:
1. Loopback IP is the localhost IP `127.0.0.1`


