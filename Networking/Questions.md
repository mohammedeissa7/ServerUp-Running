# Networking Questions

- Network troubleshooting can be a torturous process if you don’t know what you’re looking for or don’t have a strong understanding of how networking works. you need to be able to understand IP addressing, subnets, and routing. These are also big real-world concepts that allow system administrators to troubleshoot and resolve problems on their networks.



<details>
<summary>1. What command displays your current interfaces and IP address?</summary>

```
ifconfig
```
</details>
<details>
<summary>2. What does ifconfig 172.168.1.100 netmask 255.255.255.0 eth1 do?</summary>

```
This command sets the eth1 interface to have a static IP address of 172.168.1.100 with a netmask of 255.255.255.0.
```
</details>
<details>
<summary>3. What command can you use to test connectivity to another host?</summary>

```
The gateway is incorrectly set, and the subnet of the host you are trying to reach is inaccessible.
```
</details>
<details>
<summary>4. What does it mean if you ping a host and you receive the response Destination Unreachable?</summary>

```
The gateway is incorrectly set, and the subnet of the host you are trying to reach is inaccessible.
```
</details>
<details>
<summary>5. What is a gateway used for on a network?</summary>

```
A gateway is used as an entry and exit point for a subnet on a network. To contact hosts outside your subnet, you need to pass through a gateway.
```
</details>
<details>
<summary>6. How would you go about creating a static route?</summary>

```
Use the route command with the add option to create a static route.
```
</details>
<details>
<summary>7. What command can you use to monitor and troubleshoot network connections?</summary>

```
The tcpdump command is used to monitor network connections on different interfaces.
```
</details>
<details>
<summary>8. Can you name three utilities that can be used for network or DNS client troubleshooting?</summary>

```
The three utilities are: route, ping, and nslookup.
```
</details>
<details>
<summary>9. What is the /etc/hosts file used for?</summary>

```
The /etc/hosts file is a local lookup file used to map IP addresses to hostnames if a DNS server isn’t available.
```
</details>
