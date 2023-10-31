# Host system must have a physical or virtual network interface, by running `ip link` command we can see that interface.

There are multiple interfaces such as eth, veth, and lo.

### System must have a physical or virtual network interface attached to it


1. **Host System and Network Interfaces**: Your computer, or the "host system," needs to have a way to connect to the internet or other devices. It does this through something called a "network interface," which is like a doorway to the internet world. This interface can be either a physical part of your computer (like a network card or Wi-Fi adapter) or a virtual one (created by software).

2. **Using the "ip link" Command**: To understand what network interfaces your computer has, you can use a special command called "ip link." When you run this command, your computer tells you about all the different network interfaces it knows about. It's a bit like asking your computer to introduce you to all its friends.

3. **Types of Interfaces**: There are different types of these network interfaces, and some of them have names like "eth," "veth," and "lo." These names help your computer recognize and manage each of them.

   - "eth" might stand for Ethernet, which is a common way to connect to the internet using a cable.
   - "veth" could be a virtual interface, meaning it's not a physical part of your computer but created by software, often used for special purposes.
   - "lo" stands for "loopback." It's a special interface that allows your computer to talk to itself, like a phone call from you to you. It's used for various technical tasks on your computer.

So, when you run "ip link" and see these different interfaces, it's your computer showing you all its friends that help it connect to the internet and do different tasks. Understanding them can be important for managing your computer's connections and making sure everything works smoothly.

# command can be used to display the kernel ip routing table.
From the route command, we can see the route table of the host system.
![image](https://github.com/Althaf-official/DevOps/assets/105126131/1106c149-252b-4279-b381-7f82dd26cd7f)

# Which of the following is preferred device to connect two system which are on different networks?

For example, if System A is on 192.168.1.0/24 network and System B is on 192.168.2.0/24 network. 


bridge


switch


router


gateway
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

It is router, which helps us to connect two networks together like network A can be reached to the different network B with the help of a router.

Sure, let's explain it in a simple way:

Think of a router like a traffic cop for the internet. It helps connect two different neighborhoods (or networks) so that they can talk to each other.

Imagine Network A as one neighborhood and Network B as another. These neighborhoods are like separate towns, and they have their own rules.

Now, the router is like a bridge between these two towns. It knows how to get from one neighborhood to the other. So, if you want to send a message or visit someone from Network A to Network B, the router helps you do that. It makes sure your message or visit gets to the right place in the other town.

In a nutshell, a router is like the friendly guide that helps people and data travel between different neighborhoods (or networks) on the internet. It's what makes the internet work by connecting all these different places together.



# We have four app server from app01 to app04. You can access each app from jump host using command ssh app01 and similarly for other apps. Assign new IPs to each host as per details given below:


a. Assign 172.16.238.15/24 ip address to app01

b. Assign 172.16.238.16/24 ip address to app02

c. Assign 172.16.239.15/24 ip address to app03

d. Assign 172.16.239.16/24 ip address to app04

e. We also need to remove existing IPs from these apps after assigning them new IPs but do not remove them right now as it can break your connection, if you are sure you are done with required changes just click on Check button below, it will do the rest.

Warning: If changes aren't made correctly it can break your connection to the environment and you may need to reload the lab.


----------------------------------------------------------------------------------------------------------------------

Note: Please ensure to execute the commands on their respective app nodes.


For example:-

To assign new IPs for app01 , the below command need to be executed on app01.

For app01: sudo ip addr add 172.16.238.15/24 dev eth0

Please follow the same procedure for other app nodes as well:

For app02: sudo ip addr add 172.16.238.16/24 dev eth0

For app03: sudo ip addr add 172.16.239.15/24 dev eth0

For app04: sudo ip addr add 172.16.239.16/24 dev eth0
![image](https://github.com/Althaf-official/DevOps/assets/105126131/f185f5fa-b26d-4667-bee9-4d4e02dce006)




