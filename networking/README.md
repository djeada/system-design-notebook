# Networking

- [Networking](#networking)
  - [What is Networking?](#what-is-networking)
    - [Public IP](#public-ip)
    - [Private IP](#private-ip)
    - [Latency](#latency)
    - [Throughput](#throughput)
  - [Questions](#questions)

## What is Networking?

Networking is the practice of connecting computers and devices together to share data and resources. This can be done via cables (wired networking) or wireless signals. At a high level, networking involves:

- **Protocols**: Rules and conventions that govern how data is packaged and transmitted (e.g., TCP/IP).
- **Hardware**: Physical devices like routers, switches, firewalls, load balancers, etc.
- **Addressing**: Ways to identify each device in a network (e.g., IP addresses).
- **Routing**: The process of deciding how data should flow across a network from source to destination.
- **Security**: Ensuring data integrity, confidentiality, and availability (via firewalls, encryption, etc.).

In system design, networking enables different components to communicate with each other and end-users. Understanding public/private IP addresses, latency, and throughput is crucial to plan and design scalable, secure, and efficient applications or infrastructures.

### Public IP

[Wikipedia](https://en.wikipedia.org/wiki/IP_address#Public_addresses):  
"A public IP address, in common parlance, is a globally routable unicast IP address, meaning that the address is not an address reserved for use in private networks."

From a system design perspective, when you have a resource or a component that you want anyone on the internet to access—be it for direct communication (like a web server) or as a gateway for other components (like a load balancer)—you should use a public IP.

### Private IP

Whenever you **do not** want users from the internet to directly interact with a certain component or resource, you should use a private IP address. A few examples:

  - Web servers that should only accept traffic from a load balancer, rather than directly from external clients
  - Internal servers or databases that users outside the organization should not access

Private IPs, as opposed to public IPs, do **not** have to be globally unique. Each separate internal network can use the same addresses (because they are private and isolated).

### Latency

The time it takes to perform a certain task or action. In a networking context, latency often measures how long it takes for a data packet to travel from the source to the destination (and sometimes back).

### Throughput

The number of tasks or actions per unit of time. In networking, throughput often refers to how much data can be transferred between two endpoints in a given period (e.g., megabits per second, or Mbps).

## Questions

<details>
<summary>What is a public IP? In which scenarios, one should use a public IP?</summary><br><b>

A public IP is an address reachable over the internet. One should use a public IP in scenarios where external clients, services, or networks need direct or gateway-level access to a resource (e.g., a web server or load balancer).
</b></details>

<details>
<summary>What is a private IP? In which scenarios, one should use a private IP?</summary><br><b>

A private IP is an address used within an internal network, not routable over the internet. One should use a private IP when restricting direct external access, such as databases, internal services, or servers behind a load balancer.
</b></details>

<details>
<summary>What is latency?</summary><br><b>

Latency is the time delay between a request for data (or a signal) and the start of its arrival. In networking, it refers to how long it takes data to travel from source to destination.
</b></details>

<details>
<summary>What is latency of L1 cache reference vs. L2 cache reference?</summary><br><b>

- L1 cache reference latency is approximately 0.5 nanoseconds.
- L2 cache reference latency is approximately 7 nanoseconds.

So the latency of an L2 cache reference is roughly 14 times that of an L1 cache reference.
</b></details>
