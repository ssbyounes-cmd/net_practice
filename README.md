*This project has been created as part of the 42 curriculum by ychoucho.*

# NetPractice

## Description

NetPractice is an introductory networking project whose goal is to understand and practice the basics of **TCP/IP addressing**. The project provides a training interface that simulates small, non-functioning networks. For each of the 10 levels, one or more objectives must be met (e.g., making a host reach another host or a router) by correcting the unshaded configuration fields — IP addresses, subnet masks, gateways, and routing tables — until the simulated network works properly.

Through this project I practiced:
- Reading and calculating IP addresses and subnet masks.
- Determining valid host ranges and network/broadcast addresses for a given subnet.
- Configuring default gateways so devices outside the local subnet can be reached.
- Understanding how routers use routing tables to forward packets between different networks.
- Distinguishing the roles of routers and switches within a LAN.

## Instructions

1. Download and extract the project files into a folder of your choice.
2. From that folder, run the provided script:
   ```
   ./run.sh
   ```
   This launches a local web server and opens the training interface in your default browser.
3. If `run.sh` does not work, launch the server manually:
   ```
   python3 -m http.server 49242
   ```
   Then open `http://localhost:49242` in your browser (or whatever port you chose).
4. On the welcome screen, enter your intranet login in the **Training** tab and click **Start!**.
5. For each level:
   - Read the objective(s) shown at the top of the page.
   - Edit the unshaded fields (IP addresses, masks, gateways, routes) in the network diagram.
   - Click **Check again** to validate the configuration.
   - Once the level is solved, click **Get my config** to export the configuration file for that level, then click **Next level**.
6. Repeat for all 10 levels.

## Resources

Networking concepts studied for this project:

- **TCP/IP addressing** — [IBM Documentation: TCP/IP addressing](https://www.ibm.com/docs/en/aix/7.2.0?topic=protocol-tcpip-addressing)
- **Subnet masks & subnetting** — [Network Fun Times: A Complete Beginner's Guide to Subnetting](https://www.networkfuntimes.com/a-complete-beginners-guide-to-subnetting/)
- **Default gateways & routing tables** — [GeeksforGeeks: Routing Tables in Computer Network](https://www.geeksforgeeks.org/computer-networks/routing-tables-in-computer-network/)
- **Routers and switches** — [GeeksforGeeks: Difference Between Router and Switch](https://www.geeksforgeeks.org/computer-networks/difference-between-router-and-switch/)
- **OSI model / OSI layers** — [Cloudflare Learning: What Is the OSI Model?](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)

### AI usage

AI was used as a learning aid:
- To help clarify tricky **subnetting edge cases** (e.g., borderline subnet mask calculations, identifying valid host ranges vs. network/broadcast addresses).
- To help understand **what was actually happening at each level** of the training interface — e.g., how a packet moves from a host, through a routing table, to a gateway or next hop, and why a given configuration was rejected by the checker.
- To reinforce general networking concepts (subnet masks, default gateways, routers/switches, OSI layers) discussed above.
