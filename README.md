# firewall
Firewall configuration project demonstrating adding, testing, and removing rules to control inbound and outbound traffic for enhanced network security.


1. Open firewall configuration tool (terminal for UFW/iptables)
In Kali Linux, firewall settings are usually managed using tools like UFW (Uncomplicated Firewall) or iptables. These tools provide control over inbound and outbound network traffic by defining rules. Opening the terminal is the first step to interact with the firewall configuration.

2. List current firewall rules
Before making any changes, it is important to view the existing rules to understand the current configuration. Listing rules ensures you don’t overwrite or conflict with other rules. With UFW, ufw status shows active rules, while iptables -L displays them in detail.

3. Add a rule to block inbound traffic on a specific port (e.g., 23 for Telnet)
Firewalls filter traffic by port numbers and protocols. By adding a rule to block port 23, you prevent Telnet connections, which are insecure and prone to attacks. Blocking such ports helps harden the system against unauthorized access.

4. Test the rule by attempting to connect to that port locally or remotely
After applying a rule, testing ensures the firewall is enforcing it correctly. Trying to connect with telnet or nc (netcat) will confirm whether the port is blocked. Testing verifies that the configuration change is effective and protects the system.

5. Add a rule to allow SSH (port 22) if on Linux
SSH (port 22) is widely used for secure remote login and system administration. Allowing SSH ensures legitimate administrators can still connect to the system, even when other ports are blocked. This balances security with usability.

6. Remove the test block rule to restore the original state
Firewall changes should be reversible, especially in testing or learning environments. Removing the test rule ensures the firewall returns to its original configuration, preventing unnecessary restrictions or connectivity issues.

7. Document commands or GUI steps used
Documentation is crucial for reproducibility and troubleshooting. Recording the exact commands (e.g., ufw deny 23/tcp, ufw allow 22/tcp) provides a reference for future use and ensures clarity when sharing the procedure with others.

8. Summarize how firewall filters traffic
A firewall acts as a traffic filter, controlling data packets entering or leaving a system. It uses rules based on criteria such as IP address, port, and protocol. This helps protect against unauthorized access, restricts unwanted services, and secures communication by allowing only trusted traffic.
